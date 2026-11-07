# Pregunta de Negocio

## ¿Qué segmentos de viviendas pueden identificarse dentro del mercado inmobiliario a partir de variables como el precio, los metros cuadrados, el número de habitaciones y el número de baños?

### Integrantes

- Jhonny Arley Tobón Acevedo
- Javier Martínez Ceballos

# Funcionamiento del Algoritmo K-Means

El algoritmo K-Means es una técnica de aprendizaje no supervisado utilizada para segmentar datos en grupos o clusters con características similares. Su objetivo principal es agrupar los registros de tal forma que los elementos pertenecientes a un mismo grupo sean lo más parecidos posible entre sí y, al mismo tiempo, diferentes de los elementos de otros grupos.

A continuación, se explica el funcionamiento del algoritmo paso a paso:

## Paso 1. Selección del número de clusters (K)

Inicialmente se debe definir la cantidad de grupos que se desea obtener. Este valor se representa mediante la letra **K**.

En este proyecto se utilizó el Método del Codo para determinar el número óptimo de clusters antes de entrenar el modelo.

## Paso 2. Selección de los centroides iniciales

El algoritmo selecciona de forma aleatoria K puntos iniciales llamados **centroides**, los cuales representan el centro de cada grupo.

Estos centroides actúan como referencia para comenzar el proceso de agrupamiento.

## Paso 3. Asignación de los registros a un cluster

Cada vivienda es comparada con los centroides existentes y se asigna al cluster cuyo centroide se encuentre más cercano.

Para realizar esta comparación, K-Means utiliza la distancia entre cada vivienda y los centroides disponibles.

## Paso 4. Recalcular los centroides

Una vez asignadas todas las viviendas a un grupo, el algoritmo calcula nuevamente el centro de cada cluster utilizando el promedio de los registros que pertenecen a dicho grupo.

Estos nuevos centroides representan de forma más precisa las características promedio de cada segmento.

## Paso 5. Repetición del proceso

Después de recalcular los centroides, el algoritmo vuelve a asignar las viviendas a los grupos más cercanos.

Posteriormente recalcula nuevamente los centroides y repite el procedimiento varias veces.

## Paso 6. Convergencia del modelo

El proceso finaliza cuando los centroides dejan de cambiar significativamente o cuando las viviendas permanecen asignadas al mismo cluster.

En este punto se considera que el modelo ha encontrado la mejor segmentación posible para los datos analizados.

# Aplicación en el Dataset de Viviendas

Para la segmentación de las viviendas se utilizaron las variables:

- Precio
- Metros cuadrados
- Habitaciones
- Baños

Estas variables permitieron identificar grupos de inmuebles con características similares dentro del mercado inmobiliario.

Como resultado, el modelo generó segmentos diferenciados que representan distintos perfiles de vivienda, facilitando el análisis del comportamiento del mercado y la identificación de inmuebles económicos, intermedios y premium.
