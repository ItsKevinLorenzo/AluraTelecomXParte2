# AluraTelecomXParte2

# Análisis y Predicción de Churn en TelecomX

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar los factores que influyen en la cancelación (churn) de clientes en una empresa de telecomunicaciones ficticia (TelecomX) y desarrollar modelos predictivos para identificar a los clientes en riesgo de irse. El análisis busca proporcionar información valiosa para implementar estrategias de retención efectivas.

## Proceso de Análisis y Modelado

El proyecto siguió los siguientes pasos:

1.  **Extracción y Carga de Datos:** Los datos de clientes fueron cargados desde un archivo CSV.
2.  **Limpieza y Preprocesamiento de Datos:**
    *   Se eliminaron columnas irrelevantes (`customerID`).
    *   Se manejaron valores faltantes en la columna `account.Charges.Total` imputándolos con la mediana.
    *   Se codificaron las variables categóricas utilizando One-Hot Encoding.
3.  **Análisis Exploratorio de Datos (EDA):**
    *   Se calculó la proporción de clientes con Churn para evaluar el desbalance de clases.
    *   Se realizó un análisis de correlación para identificar relaciones entre variables y con la variable objetivo.
    *   Se investigó la relación de variables clave (Tipo de Contrato, Gasto Total) con el Churn mediante visualizaciones.
4.  **Balanceo de Clases:** Se aplicó la técnica SMOTE (Synthetic Minority Oversampling Technique) en el conjunto de entrenamiento para abordar el desbalance de clases y mejorar el rendimiento de los modelos en la predicción de la clase minoritaria (Churn).
5.  **Normalización/Estandarización de Datos:** Se estandarizaron las características numéricas utilizando StandardScaler, un paso necesario para modelos basados en distancia como Regresión Logística y KNN.
6.  **División de Datos:** El conjunto de datos se dividió en conjuntos de entrenamiento y prueba (80/20) para evaluar el rendimiento de los modelos en datos no vistos.
7.  **Creación y Evaluación de Modelos Predictivos:** Se entrenaron y evaluaron varios modelos de machine learning para predecir el Churn:
    *   Regresión Logística
    *   KNN (K-Nearest Neighbors)
    *   Random Forest
    *   Árbol de Decisión
    Se evaluó el rendimiento de cada modelo utilizando métricas como Exactitud (Accuracy), Precisión (Precision), Recall, F1-Score y ROC AUC Score, además de visualizar la matriz de confusión.
8.  **Análisis de Importancia de Variables:** Se analizaron las variables más relevantes para la predicción de Churn utilizando la importancia de características para Random Forest, los coeficientes para Regresión Logística y la importancia por permutación para KNN.

## Factores Clave que Influyen en la Cancelación

El análisis de los datos y los modelos reveló varios factores importantes asociados con una mayor probabilidad de que un cliente cancele el servicio:

*   **Tipo de Contrato Mes a Mes:** Los clientes con contratos de corta duración son significativamente más propensos a cancelar.
*   **Antigüedad del Cliente Baja:** Los clientes nuevos o con poca antigüedad representan un mayor riesgo de Churn.
*   **Servicio de Internet de Fibra Óptica:** Sorprendentemente, tener fibra óptica se asoció con una mayor probabilidad de Churn, lo que podría indicar problemas de calidad o expectativas no cumplidas.
*   **Método de Pago Electrónico:** Los clientes que pagan electrónicamente también mostraron una mayor propensión a cancelar.
*   **Altos Cargos Mensuales:** Un gasto mensual más elevado está relacionado con una mayor probabilidad de Churn.
*   **Falta de Servicios Adicionales de Internet (Seguridad, Soporte):** Los clientes que no tienen servicios como seguridad en línea o soporte técnico son más propensos a cancelar.
*   **Facturación Sin Papel:** Los clientes con facturación electrónica también mostraron una correlación positiva con el Churn.

## Estrategias de Retención Propuestas

Basado en los factores identificados, se proponen las siguientes estrategias para reducir la tasa de cancelación:

*   **Incentivar Contratos a Largo Plazo:** Ofrecer descuentos o beneficios adicionales para que los clientes se cambien de contratos mes a mes a planes anuales o bianuales.
*   **Mejorar la Experiencia del Cliente Nuevo:** Implementar programas de "onboarding" efectivos y seguimiento proactivo en los primeros meses para asegurar la satisfacción y resolver problemas rápidamente.
*   **Abordar Problemas con el Servicio de Fibra y Pago Electrónico:** Investigar las causas subyacentes del Churn en estos segmentos y mejorar la calidad del servicio de fibra, así como optimizar la experiencia de pago electrónico.
*   **Revisar Estructuras de Precios:** Ofrecer opciones de planes más flexibles o descuentos por paquetes a clientes con altos cargos mensuales.
*   **Promocionar Servicios de Valor Agregado:** Destacar los beneficios de los servicios de seguridad, soporte y protección de dispositivos como una forma de aumentar la lealtad del cliente.
*   **Comunicación Dirigida:** Segmentar a los clientes en riesgo (identificados por el modelo predictivo) y dirigirse a ellos con ofertas personalizadas o soporte adicional.

## Conclusiones

El análisis y los modelos desarrollados proporcionan una comprensión clara de los principales impulsores del Churn en TelecomX. Al enfocarse en los clientes con contratos mes a mes, baja antigüedad, servicio de fibra, pago electrónico y altos cargos mensuales, y al promover servicios de valor agregado, la empresa puede implementar estrategias de retención más efectivas y reducir la pérdida de clientes.
