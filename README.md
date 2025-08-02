# Alura-Latam-Telecom-X
Challenge Telecom X Alura Latam
OBJETIVO DE ANÁLISIS
El análisis de TelecomX se llevó a cabo con el objetivo principal de entender y dar a conocer las causas de la alta evasión de clientes que está experimentando la empresa, lo cual representa pérdidas monetarias significativas. Para este análisis, se realizó un proceso de limpieza y procesamiento de datos utilizando las librerías Pandas y Numpy. Esto incluyó:

• Importar datos con read_json().

• Verificar el dataset con head() e identificar columnas con valores JSON.

• Normalizar columnas JSON y concatenarlas al dataframe original, eliminando las columnas JSON originales.

• Analizar el dataframe final con info() para verificar la cantidad de entradas, columnas y tipos de datos.

• Buscar valores únicos con unique().

• Identificar y manejar 11 valores en blanco en la columna "Charges.total", reemplazándolos por cero, asumiendo que corresponden a nuevos clientes sin pagos aún.

• Cambiar el tipo de dato de la columna "Charges.Total" de "object" a "float".

• Transformar a minúsculas todas las columnas tipo string y reemplazar los valores "yes" y "no" por "1" y "0" respectivamente en todo el dataset.

• Calcular la columna "Cuentas diarias" dividiendo "Charges.Monthly" entre 30. Los hallazgos clave del análisis exploratorio de datos y las conclusiones incluyen:

• Alta tasa de evasión general: El 25.7% del total de clientes (1869 de 7267) se ha dado de baja.

• El género no es un factor determinante: La diferencia en la evasión entre hombres y mujeres es mínima (0.5%), sugiriendo que las estrategias de retención no deberían enfocarse en este aspecto.

• Medio de pago "Electronic check": Es el mayor contribuyente a la evasión, con un 57.3% de los evasores utilizándolo. Los medios de pago automáticos (Bank transfer y Credit card) y Mailed check presentan tasas de evasión significativamente menores (13.8%, 12.4% y 16.4% respectivamente). Los medios de pago automáticos son los que menos evasión presentan.

• Tipo de contrato "Month to month": Es el principal generador de evasión, con un 88.55% de los evasores teniendo este tipo de contrato. Los contratos a largo plazo (Two year y One year) muestran tasas de evasión muy bajas (2.56% y 8.88% respectivamente).

• Evasión en los primeros meses de contrato: La mayoría de los clientes que cancelaron el servicio lo hicieron durante los primeros meses de contrato, indicando un periodo crítico de "churn" temprano. La tasa de evasión disminuye a medida que los clientes permanecen más tiempo en la empresa.

• Concentración de evasión en rangos de gasto bajos: Un gran número de usuarios que cancelaron el servicio se encontraban en los rangos de gasto más bajos (cercanos a 0). Esto podría deberse a la promoción de planes con costo inicial bajo seguidos de ajustes abruptos de precio, o a deficiencias en la post-venta. Con base en estas conclusiones, se proponen las siguientes recomendaciones estratégicas para TelecomX_LATAM:

• Priorizar la contratación de planes a largo plazo: Se debe reestructurar la oferta para incentivar fuertemente planes de uno o dos años, ofreciendo descuentos de fidelidad, beneficios adicionales o precios especiales, y reduciendo drásticamente los incentivos para planes mes a mes debido a su alto riesgo de evasión.

• Promover activamente los medios de pago con baja tasa de evasión: Se recomienda desincentivar el "Electronic Check" y fomentar el uso de "Bank Transfer (automatic)" o "Credit Card (automatic)" para nuevos clientes mediante campañas con beneficios. También se debería considerar campañas para migrar a clientes actuales que usan "Electronic Check".

• Fortalecer la retención temprana de clientes: Diseñar e implementar un programa de bienvenida y seguimiento intensivo durante los primeros meses, incluyendo un onboarding robusto, comunicación proactiva para verificar satisfacción, resolver dudas, y ofrecer promociones de retención temprana. Además, se debe monitorear el uso para detectar patrones que predigan la evasión.

• Investigar el comportamiento de gasto y la percepción de valor: Realizar un estudio más profundo sobre los clientes con bajo gasto que cancelaron el servicio versus los que se quedaron, mediante encuestas de salida, análisis de procesos de post-venta (soporte técnico, atención al cliente, quejas) y evaluar si la estrategia de precios iniciales genera expectativas no cumplidas.

