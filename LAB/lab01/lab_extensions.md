---
sort: 2
---

# Practica de estructuración de extensiones Darwin Core


**Objetivo**

Conocer y utilizar las extensiones del estándar Darwin Core (DwC) siguiendo unas buenas prácticas de documentación. 


**Sobre la actividad**

Utilizar 3 de las extensiones más comunes del estándar DwC para la incorporación de información sobre rasgos funcionales, recursos multimedia, y datos sobre distribución de especies. Para esto se proporcionarán conjuntos de datos de prueba y planillas de publicación enfocadas en el uso de las extensiones DwC.


**Requerimientos**

Contar con un programa para procesar archivos de texto como Excel.

**Archivo de trabajo**

- *Ejercicio de Rasgos funcionales* 

[Ejercicio1_Registrosbiologicos_Estructurado.xls](https://drive.google.com/uc?id=1KslrtjZAwFbOWsQJ9NdBi2BLBbxNoVJo&authuser=0&export=download)
[Ejercicio1_MedidasyHechos_porEstructurar.xls](https://drive.google.com/uc?id=1fHWfwjQ8s_4j12uHHleUw4JFyIRoeq0V&authuser=0&export=download)

- *Ejercicio de Distribución de especies*

Ejercicio2_ListadeEspecies_Estructurado.xls
Ejercicio2_DistribucionEspecies_porEstructurar.xls

- *Ejercicio de Multimedia*

Ejercicio3_Registrosbiologicos_Estructurado.xls
Ejercicio3_Multimedia_porEstructurar.xls

- *Plantillas*

[Medidas o hechos (_Measurement or Facts_)](https://drive.google.com/uc?export=download&id=1s05MAYDixYt6wPp9V8de8qrCHxuOOw-o) 
Distribución de especies (_Species Distribution_)
[Multimedia Simple (_Simple Multimedia_)](https://drive.google.com/uc?export=download&id=1Bfdgnl-KXwvLHs8H-bSe8yBXVyD8qrx8)

## Ejercicio 1 - Rasgos funcionales


### Paso 1 - Caso de estudio
A partir de las notas de campo de algunos especímenes depositados de la colección de la Universidad de Ciencias Naturales, que se encuentra publicada a través del SiB Colombia como un conjunto de datos de Registros Biológicos, se decide incorporar información sobre los rasgos funcionales de los especímenes. Usted cuenta con los datos de la colección debidamente estructurados en DwC y  una tabla -sin estructurar- relacionando a partir del número de catálogo rasgos funcionales para Aves y Reptiles. Su misión es estructurar los datos de los rasgos funcionales utilizando  la extensión  Medidas o hechos (_Measurement or Facts_)  para que estos puedan incluirse en la publicación de la colección.

### Paso 2 - Exploración de la plantilla
 
Descargue y abra la plantilla de la extensión de Medidas o Hechos (_Measurement or Facts_). Encontrará 4 pestañas:
Instrucciones: Contiene la guía de uso y los puntos a tener en cuenta antes de iniciar la documentación de la extensión.
Plantilla: Contiene la tabla con los elementos DwC para documentar la extensión.
Definiciones: Contiene las definiciones para cada uno de los elementos del estándar DwC, recomendaciones de documentación y ejemplos.

#### 2.1 Pestaña Instrucciones

Lea las instrucciones de esta primera pestaña para familiarizarse con el contenido y alcance de la misma. Encontrará una sección titulada Elementos obligatorios según el tipo de los datos (Fig. 1). De acuerdo a la lectura del Paso 1 y los datos de ejemplo (**Ejercicio1_MedidasyHechos_porEstructurar.xls**) identifique cuales son los elementos obligatorios para el uso de la extensión y téngalos en cuenta para el paso 3 . 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/LAB/lab01/_images/Fig1_Extensiones_Elementosobligatorios.png" width=600>
Figura 1. Elementos obligatorios de la extensión para Registros Biológicos como Core de la publicación.


#### 2.2 Plantilla
Explore los elementos de la extensión en la pestaña de plantilla, encontrará algunos ejemplos pre-documentados en gris para facilitar la interpretación y alcance de los elementos. Puede mantener estos ejemplos durante el ejercicio como referencia o eliminarlos antes de usar la plantilla, estos marcan un punto de partida pero no representan todas las posibilidades de la extensión ya que las medidas pueden ser tan variadas como fuentes de datos.

#### 2.3 Definiciones 
Explore la definición de los elementos de la extensión. Puede hacer clic en los elementos de la plantilla, esto lo llevará a la definición del elemento junto a algunos ejemplos de documentación, o puede revisarlas 

### Paso 3 - Mapeo de los datos

Una vez haya explorado los elementos de la extensión e identificado los elementos obligatorios, revise detenidamente el archivo **Ejercicio1_MedidasyHechos_porEstructurar.xls** e identifique los elementos de la extensión que le permitirán estructurar las medidas para su publicación. A esta actividad la llamamos mapeo de datos. Revise la definición de los elementos y sus ejemplos para estar seguro sobre la correspondencia del mapeo. 

#### 3.1 Identificar el tipo de medidas o hechos
Identifique el tipo medidas teniendo en cuenta que se pueden dividir en dos categorías:

* **Cuantitativas**: Una medida cuantificable que cuenta con una unidad de medida, por lo que se asocia como mínimo a los elementos measurementType, measurementeValue y measurementeUnit.
 _Ejemplo_:
    - _measurementType_: Largo del pico
    - _measurementeValue_: 20
    - _measurementUnit_: mm

* **Cualitativas** (hechos): son variables categóricas que guardan algún tipo de lógica, pero que no están asociadas directamente a una unidad de medida, por lo que se asociará como mínimo a los elementos measurementeType y measurementValue. 
_Ejemplo_:
    - _measurementType_: Color pico
    - _measurementeValue_: Amarillo 

#### 3.2 Mapeo de elementos 
De acuerdo al paso anterior ahora deberá mapear las medidas en los elementos de la extensión. Para esta extensión puede duplicar  los elementos  tantas veces como lo necesite. Por ejemplo, puede duplicar los elementos _measurementType_, _measurementValue_, _measurementUnit_ y _measurementDeterminatedBy_  para documentar las medidas de la Altura de percha y la Longitud rostro cloacal (Fig 2). Haga lo mismo para las medidas faltantes.


Figura 2. Mapeo de la Medida 1 (Altura de la percha) y la Medida 2 (Longitud Rostro Cloacal) duplicando los elementos de la plantilla.


#### 3.3. Estructurar el elemento occurrenceID
Para cualquier extensión es necesario contar con un identificador (ID) para poder enlazar la extensión con los datos, en este caso un occurrenceID ya que los datos corresponden a  registros biológicos (**Ejercicio1_Registrosbiologicos_Estructurado.xls**). Por lo tanto debe asegurarse que el _occurrenceID_ de la extensión de Medidas o hechos coincida exactamente con el del conjunto de datos estructurado, haga los ajustes necesarios en el _occurrenceID_ para que coincida. (Fig  3)


Figura 3. Diferencia entre el occurrenceID del conjunto de datos de registros biológicos y el elemento mapeado a occurrenceID en la extensión.
 
#### 3.4 Eliminar filas de ejemplo
Una vez finalice el mapeo debe eliminar los ejemplos (**resaltados en gris**). Recuerde que estos ejemplos son una ayuda para el mapeo de los elementos en la plantilla pero no son necesarios para el resultado final en la publicación. 


### Paso 4 - Ajustar formato de los datos

#### 4.1. Ajustar según definiciones y ejemplos
Una vez estén todos los datos del archivo **Ejercicio1_MedidasyHechos_porEstructurar.xls**  en la plantilla de la extensión, ajuste los datos de acuerdo a las definiciones del estándar para cada elemento mapeado (Fig. 4).

Figura 4. Datos ajustados según las definiciones y los vocabularios controlados sugeridos.

#### 4.2. Eliminar los elementos vacíos
Elimine en la plantilla de Medidas o hechos (_Measurement or Facts_)  los elementos DwC que quedaron vacíos, para la publicación solo debe mantener los elementos que hayan sido documentados. (figura 5).

Figura 5. Detalle de como eliminar los elementos vacíos. Clic derecho en la columna > Eliminar.

### Paso 5 - Verificación del resultado
Compare el siguiente archivo estandarizado con el archivo que trabajó en el laboratorio y verifique en qué acertó y que puede mejorar. ¿Logró completar más información en la plantilla?

Tenga en cuenta que existen dos (2) formas válidas de documentar esta extensión. Una es agregar los elementos DwC tantas veces como sea necesario - como se hizo en el ejercicio anterior. Otra forma es agregar una fila para cada medida, esto es posible ya que cada fila se puede relacionar al espécimen por medio del identificador, en este caso occurrenceID (Figura 6). 

Figura 6. Segundo mecanismo de documentación de la extensión de medidas y hechos en forma de filas, sin duplicar elementos DwC.

En el archivo descargado verá las dos formas de estructurar la extensión.

**[Descargue el archivo estandarizado](https://drive.google.com/uc?id=1E6_oUh53Du3wTIGilKeyvwQZWbwjR_Wv&authuser=0&export=download)**



