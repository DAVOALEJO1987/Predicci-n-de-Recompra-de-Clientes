# Taller Predicción de Recompra de Clientes
## Resumen
Se presenta un estudio que aborda la aplicación de una red neuronal multicapa (MLP) para anticipar la probabilidad de recompra en clientes, partiendo de un conjunto de datos estructurado con variables representativas del comportamiento de compra. Se persigue identificar las características más determinantes en la recompra, así como fundamentar estrategias comerciales orientadas a la fidelización y maximización del ciclo de vida del cliente.

![image](https://github.com/user-attachments/assets/6232e897-3b51-49ae-b17a-2d65e3d0e4e6)

## Metodología aplicada
El conjunto de datos empleado está compuesto por las variables: días desde la última compra, total de compras, monto promedio, uso de cupón, tiempo de navegación, número de visitas y la variable objetivo de recompra. 

![image](https://github.com/user-attachments/assets/981d6eaa-e354-4e6f-abcf-b722133b3e01)
 
La secuencia metodológica comprende una exploración descriptiva y visual del dataset, normalización de las variables numéricas, segmentación en conjuntos de entrenamiento y prueba, y posterior construcción y entrenamiento de un modelo MLP configurado con dos capas ocultas de 16 y 8 neuronas respectivamente, utilizando la función de activación ReLU y una capa de salida con activación sigmoide.
El ajuste de hiperparámetros se mantuvo en valores estándar, reservando un 30% de los datos para validación, y se utilizaron 50 épocas de entrenamiento con batch size de 16.
## Análisis de variables y su impacto
El análisis exploratorio, soportado por visualizaciones estadísticas y la matriz de correlación, evidenció que el número de visitas emerge como la variable con mayor incidencia en la recompra. Se observó que clientes con mayor frecuencia de visitas presentaban probabilidades significativamente superiores de realizar una nueva compra. Asimismo, el total de compras y el tiempo de navegación exhibieron tendencias positivas, aunque con menor impacto relativo. 
Variables como días desde la última compra y monto promedio, en contraste, mostraron patrones más heterogéneos.

![image](https://github.com/user-attachments/assets/1b4da7bc-e811-41f2-ab43-4da0d55d9f94)

# Insights principales
## 1. Desempeño del Modelo 
El modelo entrenado mostró un rendimiento robusto, alcanzando una exactitud global del 94%. Los valores de precisión, recall y F1-score por clase se resumen en la siguiente tabla:

![image](https://github.com/user-attachments/assets/53d3fa64-2917-4ee1-9667-b0e26996c561)

![image](https://github.com/user-attachments/assets/acddbcce-d619-475a-a114-552b2b05734c)

![image](https://github.com/user-attachments/assets/95f064a0-c9c8-4efb-aabd-851afc4551b2)

![image](https://github.com/user-attachments/assets/8b91aeff-57a9-4431-aeec-40e33f1667ec)

El análisis de la matriz de confusión confirma la alta capacidad del modelo para distinguir entre quienes recompra y quienes no, si bien se identificaron algunos falsos negativos, principalmente en la clase de no recompra.

## 2. Validación con nuevos perfiles de clientes
Para evaluar la capacidad de generalización, se introdujeron dos perfiles hipotéticos de clientes:

![image](https://github.com/user-attachments/assets/07771a86-693b-46ac-aef6-4ffd681a7edd)

El primer perfil, caracterizado por una alta interacción reciente y frecuente, fue identificado como altamente propenso a recomprar, mientras que el segundo, con baja actividad y pocas visitas, fue clasificado con probabilidad nula de recompra. Esta validación respalda la consistencia y utilidad práctica del modelo en la segmentación de clientes.

![image](https://github.com/user-attachments/assets/a9979f9d-dd60-4e3c-b5d6-1775edb2acef)

## 3. Potenciales ajustes al modelo
No se realizaron ajustes avanzados a la arquitectura original, manteniéndose la configuración propuesta inicialmente. Sin embargo, para futuros desarrollos se sugiere explorar una mayor profundidad de la red (más capas ocultas o mayor número de neuronas), el ajuste fino de parámetros de aprendizaje, la implementación de técnicas de regularización como Dropout y la aplicación de validación cruzada para asegurar estabilidad y robustez en distintos subconjuntos de datos. Dichas optimizaciones podrían reflejarse en un incremento de las métricas de desempeño y una mejor adaptación ante cambios en la base de clientes.

## 4. Recomendaciones para el área de marketing
Los resultados obtenidos sugieren que la frecuencia de visitas y la interacción constante son factores clave para promover la recompra. Se recomienda implementar estrategias orientadas a incentivar el retorno del cliente mediante campañas personalizadas, programas de fidelidad, y el uso estratégico de cupones o incentivos en puntos de contacto clave. Además, es aconsejable prestar especial atención a clientes con largos periodos de inactividad, identificando oportunidades para reactivación a través de comunicaciones segmentadas y ofertas personalizadas.
La aplicación de redes neuronales multicapa para la predicción de recompra aporta un enfoque riguroso y adaptable, capaz de generar valor tangible en la gestión comercial. La identificación de variables clave y la validación con nuevos perfiles de clientes refuerzan el potencial de esta tecnología como herramienta de soporte a la toma de decisiones en áreas de marketing y retención de clientes.

![image](https://github.com/user-attachments/assets/4f49ba37-1fcd-43dd-96b4-bebf8f6a4e63)
