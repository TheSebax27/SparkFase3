# SparkFase3
Trabajo de la universidad enfocado en el uso de spark y python

Este proyecto emplea Apache Spark y Kafka en Python para analizar y predecir la calidad del vino a partir de sus características químicas. Inicialmente, Spark carga un conjunto de datos sobre vinos, y se realiza una limpieza y transformación de los datos para asegurar su integridad. A continuación, el modelo se entrena con un algoritmo de Bosques Aleatorios que permite clasificar la calidad del vino en función de sus propiedades químicas. Este modelo entrenado se guarda para usarse posteriormente en un flujo de datos en tiempo real.

Para simular un flujo constante de datos, se configura un productor en Kafka que genera datos en tiempo real sobre las características del vino. Kafka envía estos datos al tópico configurado, produciendo nuevos datos a intervalos regulares. Esta simulación emula un entorno de datos en tiempo real, en el que los mensajes llegan como si fueran observaciones continuas sobre diferentes vinos.

En paralelo, una aplicación en Spark Streaming escucha y consume los datos que llegan a través de Kafka. Spark aplica el modelo de clasificación previamente entrenado para predecir la calidad de cada nuevo dato entrante en tiempo real, mostrando los resultados de manera inmediata en la consola. De esta forma, el sistema combina el procesamiento en lotes (batch) y en tiempo real, logrando una solución completa para evaluar y clasificar la calidad del vino de manera eficiente y continua.
