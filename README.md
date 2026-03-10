# Desafio_4_ML

# Predicción de Evasión de Clientes (Churn) - Telecom X

Este proyecto aplica técnicas de Data Science y Machine Learning para identificar los factores que impulsan la cancelación de servicios en una empresa de telecomunicaciones. El objetivo es proporcionar una herramienta predictiva que permita a la empresa anticiparse a la fuga de clientes.

# Propósito del Proyecto
Fase 1 (ETL/EDA): 
Extracción de datos desde una API JSON, limpieza profunda (manejo de nulos, corrección de tipos de datos) y análisis exploratorio para detectar patrones visuales de evasión.
Fase 2 (Machine Learning): Construcción de un pipeline de modelado que incluye codificación de variables, balanceo de clases con SMOTE, entrenamiento de modelos de clasificación y evaluación de métricas de negocio.

# Estructura del ProyectoPlaintextTelecomX-Churn-Analysis/
├── 📄 TelecomX_Churn_Analysis.ipynb   # Notebook con el proceso completo (ETL, EDA y ML)

├── 📊 TelecomX_Data_Final.csv         # Dataset procesado y estandarizado

└── 📝 README.md                       # Documentación del proyecto y hallazgos

# Hallazgos del Análisis Exploratorio (EDA)

Tras procesar los datos, identificamos que:
- Los clientes con contratos "Month-to-month" tienen una tasa de deserción significativamente más alta.Existe una correlación directa entre los cargos mensuales elevados y la probabilidad de abandono.
- El uso de Fibra Óptica es el predictor individual más fuerte de cancelación según la matriz de correlación.🤖 Modelado y ResultadosSe evaluaron dos modelos principales para predecir el Churn:Regresión Logística: (Requiere normalización de datos).Random Forest: (Robusto ante diferentes escalas).
- Métricas Obtenidas:ModeloExactitud (Accuracy)Recall (Clase 1.0)F1-ScoreRegresión Logística78%64%0.61Random Forest78%56%0.5

Se seleccionó la Regresión Logística como el modelo final debido a su capacidad superior para detectar clientes que realmente van a cancelar (Recall), permitiendo una intervención proactiva más efectiva.

# Conclusiones y Recomendaciones

Dado que la Fibra Óptica es el factor de mayor peso en la cancelación, se recomienda auditar la calidad del servicio y el precio en este segmento.
Implementar alertas de riesgo para clientes con contratos mensuales y cargos superiores a $70 USD.
Ofrecer beneficios exclusivos a quienes migren de planes mensuales a contratos anuales.

# Cómo ejecutar el proyecto
Clona el repositorio: git clone https://github.com/tu-usuario/TelecomX-Churn-Analysis.git
Abre el archivo .ipynb en Google Colab.Asegúrate de ejecutar las celdas en orden secuencial para garantizar que las variables se carguen correctamente en memoria.
