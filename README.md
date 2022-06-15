# Modelo-CNN-pre-entrenado-
Modelo de Autoencoder CNN pre-entrenado. Se presenta un modelo de 4 capas convolucionales preentrenado con espectrogramas de ballenas barbadas.
Para utilizar este modelo, es conveniente descargar todos los archivos y unirlos en una carpeta.

A continuación, se detallan algunos datos que podrían ser de ineterés:

### DIMENSIÓN DE LOS DATOS DE ENTRADA. 
Los datos a ingresa tienen la siguiente dimensión: (6043, 128, 196, 1)

### ARQUITECTURA ESPECÍFICA DE LA RED 
Esta arquitectura posee una sección de codificación basada en redes convolucionales, en la que se realiza una sección de extracción de características y una capa flatten densamente conectadad para obtener una matriz representativa o código generador. A partir de ese codigo generador y replicando a la inversa el proceso de codificación se intenta replicar el espectograma de entrada.
La arquitectura propuesta posee en la etapa de extracción de características 4 capas. En todas las etapas la función de activación es tipo RELU y el padding, asociado a la etapa de filtrado, se reacomoda de forma automática para que a la salida de la etapa de filtrado, el tamaño de las filas y columnas sea un número entero. Se agrega una capa de BachNormalization,como capa Pooling. Se agrega una capa Flatten para obtener un vector de datos representativo.
- 1º capa:  32 Filtros de 3x3x1. El Stride será de 1 y el padding se acomoda.
- 2º capa:  64 Filtros de 3x3x1. El Stride será de 2 y el padding se acomoda.
- 3º capa:  64 Filtros de 3x3x1. El Stride será de 2 y el padding se acomoda.
- 4º capa:  64 Filtros de 3x3x1. El Stride será de 1 y el padding se acomoda.

### DATOS DE ENTRENAMIENTO 
LEARNING_RATE = 0.0005;
BATCH_SIZE = 70;
EPOCHS = 60;
porcentaje_validacion=0.2.
