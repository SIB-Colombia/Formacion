---
sort: 2
---

# Estandarización usando las extensiones Darwin Core


**Objetivo**

Conocer y utilizar las extensiones del estándar Darwin Core (DwC) siguiendo unas buenas prácticas de documentación. 


**Sobre la actividad**

Utilizar 3 de las extensiones más comunes del estándar DwC para la incorporación de información sobre rasgos funcionales, recursos multimedia, y datos sobre distribución de especies. Para esto se proporcionarán conjuntos de datos de prueba y planillas de publicación enfocadas en el uso de las extensiones DwC.


**Requerimientos**

Contar con un programa para procesar archivos de texto como Excel.

**Archivo de trabajo**

- *Ejercicio de Rasgos funcionales* 

    - [Ejercicio1_Registrosbiologicos_Estructurado.xls](https://drive.google.com/uc?id=1KslrtjZAwFbOWsQJ9NdBi2BLBbxNoVJo&authuser=0&export=download)
    - [Ejercicio1_MedidasyHechos_porEstructurar.xls](https://drive.google.com/uc?id=1fHWfwjQ8s_4j12uHHleUw4JFyIRoeq0V&authuser=0&export=download)
    - [Plantilla Medidas o hechos (_Measurement or Facts_)](https://drive.google.com/uc?export=download&id=1s05MAYDixYt6wPp9V8de8qrCHxuOOw-o) 


- *Ejercicio de Distribución de especies*

    - [Ejercicio2_ListadeEspecies_Estructurado.xls](https://drive.google.com/uc?id=1YoBeJIxmH5LdVNWglcyeFcuxJT83MryO&authuser=0&export=download)
    - [Ejercicio2_DistribucionEspecies_porEstructurar.xls](https://drive.google.com/uc?id=1FRUsnhRglZ11eRQnn2mL0XCQp1W3WicZ&authuser=0&export=download)
    - [Plantilla Distribución de especies (_Species Distribution_)](https://drive.google.com/uc?export=download&id=1kqyGIkeP6KdR0-hz7CbGvriQuSitWqwp)

- *Ejercicio de Multimedia*

    - [Ejercicio3_Registrosbiologicos_Estructurado.xls](https://drive.google.com/uc?id=1wm7ZvwBqywuROZ-xqTmx00dsAZUY_oQO&authuser=0&export=download)
    - [Ejercicio3_Multimedia_porEstructurar.xls](https://drive.google.com/uc?id=1ghJuuEc9TDBvwu0vaWAuuu1d113nNpa7&authuser=0&export=download)
    - [Plantilla Multimedia Simple (_Simple Multimedia_)](https://drive.google.com/uc?export=download&id=1Bfdgnl-KXwvLHs8H-bSe8yBXVyD8qrx8)

## Ejercicio 1 - Rasgos funcionales


### Paso 1 - Caso de estudio
A partir de las notas de campo de algunos especímenes depositados de la colección de la Universidad de Ciencias Naturales, que se encuentra publicada a través del SiB Colombia como un conjunto de datos de Registros Biológicos, se decide incorporar información sobre los rasgos funcionales de los especímenes. Usted cuenta con los datos de la colección debidamente estructurados en DwC y  una tabla -sin estructurar- relacionando a partir del número de catálogo rasgos funcionales para Aves y Reptiles. Su misión es estructurar los datos de los rasgos funcionales utilizando  la extensión  Medidas o hechos (_Measurement or Facts_)  para que estos puedan incluirse en la publicación de la colección.

### Paso 2 - Exploración de la plantilla
 
Descargue y abra la plantilla de la extensión de Medidas o Hechos (_Measurement or Facts_), encontrará 4 pestañas:

- **Instrucciones**: Contiene la guía de uso y los puntos a tener en cuenta antes de iniciar la documentación de la extensión.
- **Plantilla**: Contiene la tabla con los elementos DwC para documentar la extensión.
- **Definiciones**: Contiene las definiciones para cada uno de los elementos del estándar DwC, recomendaciones de documentación y ejemplos.

#### 2.1. Pestaña Instrucciones

Lea las instrucciones de esta primera pestaña para familiarizarse con el contenido y alcance de la misma. Encontrará una sección titulada Elementos obligatorios según el tipo de los datos (Fig. 1). De acuerdo a la lectura del Paso 1 y los datos de ejemplo ```Ejercicio1_MedidasyHechos_porEstructurar.xls``` identifique cuales son los elementos obligatorios para el uso de la extensión y téngalos en cuenta para el paso 3 . 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig1_Extensiones_Elementosobligatorios.png" width=800>

<sup>_Figura 1. Elementos obligatorios de la extensión para Registros Biológicos como Core de la publicación._</sup>


#### 2.2. Plantilla
Explore los elementos de la extensión en la pestaña de plantilla, encontrará algunos ejemplos pre-documentados en gris para facilitar la interpretación y alcance de los elementos. Puede mantener estos ejemplos durante el ejercicio como referencia o eliminarlos antes de usar la plantilla, estos marcan un punto de partida pero no representan todas las posibilidades de la extensión ya que las medidas pueden ser tan variadas como fuentes de datos.

#### 2.3. Definiciones 
Explore la definición de los elementos de la extensión. Puede hacer clic en los elementos de la plantilla, esto lo llevará a la definición del elemento junto a algunos ejemplos de documentación, o puede revisarlas 

### Paso 3 - Mapeo de los datos

Una vez haya explorado los elementos de la extensión e identificado los elementos obligatorios, revise detenidamente el archivo ```Ejercicio1_MedidasyHechos_porEstructurar.xls```e identifique los elementos de la extensión que le permitirán estructurar las medidas para su publicación. A esta actividad la llamamos mapeo de datos. Revise la definición de los elementos y sus ejemplos para estar seguro sobre la correspondencia del mapeo. 

#### 3.1. Identificar el tipo de medidas o hechos
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

#### 3.2. Mapeo de elementos 
De acuerdo al paso anterior ahora deberá mapear las medidas en los elementos de la extensión. Para esta extensión puede duplicar  los elementos  tantas veces como lo necesite. Por ejemplo, puede duplicar los elementos _measurementType_, _measurementValue_, _measurementUnit_ y _measurementDeterminatedBy_  para documentar las medidas de la Altura de percha y la Longitud rostro cloacal (Fig 2). Haga lo mismo para las medidas faltantes.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig2_Extensiones_mapeo.png" width=800>

<sup>_Figura 2. Mapeo de la Medida 1 (Altura de la percha) y la Medida 2 (Longitud Rostro Cloacal) duplicando los elementos de la plantilla._</sup>


#### 3.3. Estructurar el elemento occurrenceID
Para cualquier extensión es necesario contar con un identificador (ID) para poder enlazar la extensión con los datos, en este caso un occurrenceID ya que los datos corresponden a  registros biológicos (```Ejercicio1_Registrosbiologicos_Estructurado.xls```). Por lo tanto debe asegurarse que el _occurrenceID_ de la extensión de Medidas o hechos coincida exactamente con el del conjunto de datos estructurado, haga los ajustes necesarios en el _occurrenceID_ para que coincida (Fig  3).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig3_Extensiones_occurrenceID.png" width=400>

<sup>_Figura 3. Diferencia entre el occurrenceID del conjunto de datos de registros biológicos y el elemento mapeado a occurrenceID en la extensión._</sup>
 

### Paso 4 - Ajustar los datos

#### 4.1. Ajustar según definiciones y ejemplos
Una vez estén todos los datos del archivo ```Ejercicio1_MedidasyHechos_porEstructurar.xls```  en la plantilla de la extensión, ajuste los datos de acuerdo a las definiciones del estándar para cada elemento mapeado (Fig. 4).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig4_Extensiones_ajustados.png" width=800>

<sup>_Figura 4. Datos ajustados según las definiciones y los vocabularios controlados sugeridos._</sup>

#### 4.2. Eliminar los elementos vacíos y filas de ejemplo
Elimine en la plantilla de Medidas o hechos (Measurement or Facts)  las columnas de los elementos DwC que quedaron vacíos, para la publicación solo debe mantener los elementos que hayan sido documentados (Figura 5). En este punto también puede eliminar  los ejemplos -resaltados en gris-, recuerde que estos ejemplos son una ayuda para el mapeo de los elementos en la plantilla pero no son necesarios para el resultado final en la publicación. 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig5_Extensiones_eliminar.png" width=400>

<sup>_Figura 5. Detalle de como eliminar los elementos vacíos. Clic derecho en la columna > Eliminar._</sup>

### Paso 5 - Verificación del resultado
Compare el siguiente [archivo estandarizado](https://drive.google.com/uc?id=1E6_oUh53Du3wTIGilKeyvwQZWbwjR_Wv&authuser=0&export=download) con el archivo que trabajó en el ejercicio y verifique en qué acertó y que puede mejorar. ¿Logró completar más información en la plantilla?

Tenga en cuenta que existen **dos** (2) formas válidas de documentar esta extensión. Una es agregar los elementos DwC tantas veces como sea necesario - como se hizo en el ejercicio anterior. Otra forma es agregar una fila para cada medida, esto es posible ya que cada fila se puede relacionar al espécimen por medio del identificador, en este caso el occurrenceID (Figura 6). 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig6_Extensiones_tiposmapeo.png" width=800>

<sup>_Figura 6. Segundo mecanismo de documentación de la extensión de medidas y hechos en forma de filas, sin duplicar elementos DwC._</sup>

En el archivo descargado verá las dos formas de estructurar la extensión.

## Ejercicio 2.  - Distribución de especies

### Paso 1 - Caso de estudio
Está participando en un proyecto cuyo objeto es realizar una lista de especies de las aves en la reserva del Pantano de Martos en el municipio de Guatavita (Código Divipola: 25326) para definir su estrategia de conservación. El investigador principal ha revisado los datos publicados a través del SiB Colombia y la literatura histórica con información del municipio para consolidar una lista de especies estructurada en el estándar DwC. Adicionalmente usted consolidó los datos de la distribución de las especies con sus estados de amenaza, estos nuevos datos deben ser incorporados dentro de la publicación de la lista haciendo uso de la extensión Distribución de Especies (_Species Distribution_). Su misión es estructurar los datos de  distribución de especies utilizando  la extensión.


### Paso 2 - Exploración de la plantilla
Descargue y abra la plantilla de la extensión de Distribución de especies (Species Distribution). Encontrará 4 pestañas:
* Instrucciones: Contiene la guía de uso y los puntos a tener en cuenta antes de iniciar la documentación de la extensión.
* Plantilla: Contiene la tabla con los elementos DwC para documentar la extensión.
* Definiciones: Contiene las definiciones para cada uno de los elementos del estándar DwC, recomendaciones de documentación y ejemplos.
* Vocabulario: Contiene los vocabularios controlados para algunos de los elementos DwC.

En la pestaña de instrucciones encontrará adicionalmente una sección titulada _Elementos obligatorios_ según el tipo de los datos. Para esta extensión el único elemento obligatorio es el _taxonID_ el cual tendrá que obtenerse a partir del archivo ```Ejercicio2_ListadeEspecies_Estructurado.xls``` como se indica en el siguiente paso. 

Explore los elementos de la extensión en la pestaña de plantilla haciendo clic en en los elementos para acceder a las definiciones y vocabularios controlados (cuando corresponda). En la plantilla encontrará algunos ejemplos pre-documentados en gris para facilitar la interpretación y alcance de los elementos. Puede mantener estos ejemplos durante el ejercicio como referencia o eliminarlos antes de usar la plantilla, estos marcan un punto de partida pero no representan todas las posibilidades de la extensión ya que dependerá del alcance temático y geográfico de cada lista de especies.

### Paso 3 - Mapeo de los datos

Revise detenidamente el nombre y contenido de cada columna del archivo ```Ejercicio2_DistribucionEspecies_porEstructurar.xls``` e identifique a cuál elemento de la extensión corresponde.  Revise la definición de los elementos y sus ejemplos para estar seguro sobre la correspondencia del mapeo. (Fig 7)

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig7_Extensiones_sd_mapeo.png" width=800>

<sup>_Figura 7. Mapeo de datos de distribución en la plantilla de Distribución de especies (_Species Distribution_)._</sup>

Para cualquier extensión es necesario contar con un identificador (ID) para poder enlazar la extensión con los datos, en este caso un _taxonID_ ya que los datos corresponden a una lista de especies. Para ello, a partir del nombre científico en ```Ejercicio2_DistribucionEspecies_porEstructurar.xls```identifique el taxonID en el archivo ```Ejercicio2_ListadeEspecies_Estructurado.xls``` y complételo en el elemento taxonID de la plantilla de la extensión (Fig 8).  

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig8_Extensiones_sd_taxonID.png" width=800>

<sup>_Figura 8. Documentación del taxonID  en la plantilla de Distribución de especies a partir de la lista de especies._</sup>


### Paso 4 - Ajustar los datos

#### 4.1. Ajustar según definiciones y ejemplos
Una vez estén todos los datos del archivo ```Ejercicio2_DistribucionEspecies_porEstructurar.xls``` en la plantilla de la extensión, ajuste los datos de acuerdo a las definiciones y vocabularios controlados del estándar para cada elemento mapeado. 

#### 4.2 Completar la información geográfica
En el caso de uso se le proporcionó el ID de la geografía superior según Divipola. Documente los elementos countryCode y locationID de acuerdo a esta información y la definición del elemento. (Fig 9).


<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig9_Extensiones_sd_ajustados.png" width=800>

<sup>_Figura 9. Estandarización de elementos de acuerdo a las definiciones del estándar Darwin Core._</sup>


####  4.3. Eliminar los elementos vacíos y filas de ejemplo
Elimine en la plantilla de Distribución de especies (Species Distribution)   las columnas de los elementos DwC que quedaron vacíos, para la publicación solo debe mantener los elementos que hayan sido documentados (Figura 5). En este punto también puede eliminar  los ejemplos -resaltados en gris-, recuerde que estos ejemplos son una ayuda para el mapeo de los elementos en la plantilla pero no son necesarios para el resultado final en la publicación. 

### Paso 5 - Verificación del resultado
Compare el siguiente archivo estandarizado según las definiciones del estándar con el archivo que trabajó en el laboratorio y verifique en qué acertó y que puede mejorar. ¿Logró completar más información en la plantilla?

[**Descargue el archivo estandarizado**](https://drive.google.com/uc?id=1Kk5UjFbWbLM-12W8L1cmNd58mrDXK-Jz&authuser=0&export=download)


## Ejercicio 3. - Recursos multimedia

### Paso 1 - Aplicar lo aprendido
A partir de los anteriores ejercicios habrá notado que las extensiones funcionan de forma similar. En este ejercicio deberá realizar la estructuración de la extensión Multimedia Simple (_Simple Multimedia_) a partir de los aprendido en los ejercicios anteriores. 

Para este ejercicio se le proporciona un archivo estructurado en DwC (```Ejercicio3_Registrosbiologicos_Estructurado.xls```) con los datos de una colección de microorganismos a cuyas cepas se le desea asociar imágenes de referencia. En el archivo **Ejercicio3_Multimedia_porEstructurar.xls** encontrarla los enlaces de dichas imágenes y deberá estructurarlas usando la extensión Simple Multimedia (_Multimedia Simple_).

 
### Paso 2 - Verificación del resultado
Compare el siguiente archivo estandarizado según las definiciones del estándar con el archivo que trabajó en el laboratorio y verifique en qué acertó y que puede mejorar. ¿Logró completar más información en la plantilla?


**[Descargue el archivo estandarizado](https://drive.google.com/uc?id=1pODwB1jELAvpTa9CvujyOd6vcFyA0Nld&authuser=0&export=download)**


## Ejercicio 4 - Datos propios

Si tiene datos propios que desee publicar, estandarícelos siguiendo los pasos de esta guía. Recuerde usar la plantilla de acuerdo al tipo y origen de los datos.

En este ejercicio notará que las imágenes se encuentran en un repositorio. Si a futuro  desea  publicar imágenes asociadas a un registro biológico le recomendamos algunos de los siguientes repositorios según se adapte a sus necesidades:

* Wikimedia Commons
    * fotografías ilimitadas
    * Sobre las galerías: https://commons.wikimedia.org/wiki/Commons:Galleries
    * Ejemplo galería: https://commons.wikimedia.org/wiki/London
* Internet Archive
    * fotografías ilimitadas
    * Sobre las colecciones: https://help.archive.org/hc/en-us/articles/360017502272-How-to-request-a-collection-
    * Ejemplo colecciones: https://archive.org/details/brooklynmuseum
* flickr
    * Opción de almacenamiento gratuito
    * Limitado a 1000 fotografías
    * Ejemplo: https://www.flickr.com/photos/98788120@N02/
* SmugMug
    * El almacenamiento está sujeto a pago, puede consultar aquí los planes disponibles
    * Almacenamiento ilimitado en cualquier plan.




****
**¡Felicitaciones!** :raised_hands:
Ha aprendido a estructurar datos haciendo uso de las extensiones estándar Darwin Core.

****

**Atribución y uso de los laboratorios**

![](https://licensebuttons.net/l/by/3.0/88x31.png)

La licencia [CC-BY](https://creativecommons.org/licenses/by/4.0/) te permite usar, redistribuir y construir sobre estos contenidos libremente. :open_hands: Queremos que compartas estos laboratorios y que juntos logremos datos sobre biodiversidad de mejor calidad.

**Citación sugerida**

> Plata C., Ortíz R., Marentes E. (2021). Laboratorio de datos, Ciclo de formación. Consultado a través del SiB Colombia. Disponible en https://sib-colombia.github.io/Formacion/

****

**Fuentes:**

* _Datos y caso de uso del Ejercicio 2 basado en_: 
Asociación Bogotana de Ornitología (2011). Aves del Pantano de Martos, Guatavita, Cundinamarca, 94 especies aportadas por Ruiz-Ovalle, J. (Coordinador de Proyecto), Camargo, P. (Investigador Principal, Proveedor de Contenido, Proveedor de Metadatos y Publicador), En línea, https://doi.org/10.15472/7p2n83)

* _Datos y caso de uso del Ejercicio 3 basado en_:
Alvarado Fernández A M, Rodríguez Gómez E R, Palacios Calderón L M, Trespalacios Rangel A A, Ballesteros Ballesteros J A (2021): Colección de Microorganismos-Pontificia Universidad Javeriana. v1.7. Pontificia Universidad Javeriana. Dataset/Occurrence. https://doi.org/10.15472/ppbz1y
****
