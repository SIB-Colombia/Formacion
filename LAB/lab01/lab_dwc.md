---
sort: 1
---

# Estandarización de datos en Darwin Core


**Objetivo**

Estructurar un conjunto de datos bajo el estándar [*Darwin Core (DwC)*](https://dwc.tdwg.org/terms/) haciendo uso de las recomendaciones de documentación y vocabularios controlados.

**Sobre la actividad**

En la actividad se le proporcionará con un conjunto de datos de prueba que debe estructurar al estándar *DwC* haciendo uso de la plantilla de publicación de registros biológicos del SiB Colombia. El conjunto de datos tiene problemas de completitud y calidad que deben ser resueltos para que se ajuste a las definiciones del estándar y a los elementos mínimos requeridos.

**Requerimientos** 
* Para realizar este ejercicio debes contar con un programa procesador de archivos de texto como Excel.


**Archivo de trabajo**
* Descargue el archivo [```Datos_Caso1_20reg.xls```](https://www.gbif.org/tools/data-validator.) para realizar el laboratorio.
* Descargue la última versión de la [plantilla de publicación ](https://sites.google.com/humboldt.org.co/wikisib/publicar/plantillas?authuser=0)de registros biológicos.

--------
 
## Paso 1 - Caso de estudio 
Lea detenidamente el Caso de estudio, acá encontrará información relevante para completar el conjunto de datos a publicar.

*Tenga presente que este es un caso de uso basado en una historia ficticia construido solo para propósitos educativos.*


>La ‘Universidad de Ciencias Naturales’ (UCN) es reconocida en el país como una institución de referencia para la investigación sobre biodiversidad. El  Departamento de Biología Animal mantiene el Museo de Historia Natural (Registro Nacional de Colecciones Biologicas: 123), en donde la Colección Zoológica se encuentra bien representada con cerca de 700 especímenes recolectados y algunos datos de observaciones en campo a lo largo de todo el territorio nacional, desde mediados del siglo 20 hasta la actualidad.

>En la actualidad, su cuidado se encuentra a cargo del profesor de Sistemática Animal, Juan Travolta; quien realiza tareas curatoriales, investigativas y de docencia. Profesores del departamento y algunos estudiantes colaboran  casionalmente con la identificación de las muestras y toma de datos. El Coordinador del Departamento de Biología Animal (convencido de los beneficios y bondades que brinda la publicación de los datos a través del SiB Colombia) desea que se publiquen en línea los datos sobre Aves de la **colección  ornitológica (MH-ORNIT)**, Anfibios y Reptiles de la **colección de herpetología (MH-HERP)**, además de algunos Mamíferos (MH-MAM). Esto permitirá ampliar la visibilidad de las colecciones biológicas de la Universidad y disponer estos datos de manera abierta para que sean consultados o usados en diferentes campos de investigación y lleguen incluso a ser empleados por tomadores de decisiones a nivel regional o nacional.

>Su misión a lo largo de esta *práctica* consiste en estructurar los datos del Museo siguiendo los lineamientos del estándar Darwin Core (DwC).


## Paso 2 - Identifique los elementos obligatorios 
Ingrese a la plantilla de publicación, donde encontrará 4 pestañas:

* Instrucciones: Contiene la guía de uso y los puntos a tener en cuenta antes de iniciar la documentación de los registros biológicos.
* Plantilla: Contiene la tabla con los elementos DwC para documentar los registros biológicos 
* Definiciones: Contiene las definiciones para cada uno de los elementos del estándar DwC, recomendaciones de documentación y ejemplos.
* Vocabulario: Contiene los vocabularios controlados para algunos de los elementos DwC.

En la pestaña de instrucciones encontrará adicionalmente una sección titulada *Elementos obligatorios según el origen de los datos* (Fig. 1). De acuerdo a la lectura del **Paso 1** identifique cuales son los elementos obligatorios para el caso de estudio.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig1_Estandarizacion_datosobligatorios.png" width=1000>

*Figura 1. Instrucciones de la plantilla DwC. Elementos obligatorios según el origen de los datos.*

## Paso 3 - Cree los elementos obligatorios 
Abra el archivo de trabajo ```Datos_Caso1_20reg.xls``` y cree los elementos obligatorios faltantes a partir de la información que encuenta en el caso de estudio y en los mismos datos.

 
> **Pista**: Debe crear un identificador único del registro biológico (*occurenceID*) a partir del código de la institucion (*institutionCode*), código de la colección (*collectionCode*) y número de catálogo (*catalogNumber*). Revise la definición del elemento occurrenceID en la pestaña plantilla para saber como construirlo.

>**Ejemplo**:
*occurrenceID*: UCN:MH-ORNIT:46-2300MI2008AV0954


## Paso 4 - Mapeo de datos 
Una vez haya creado los elementos obligatorios, revise detenidamente el nombre y contenido de cada columna del archivo ```Datos_Caso1_20reg.xls``` e identifique a cuál elemento DwC de la plantilla de publicación corresponde. A esta actividad la llamamos **mapeo de datos**. Cuando identifique a cual elemento corresponde, copie y pegue el contenido en la plantilla, como se muestra en la siguiente imagen (Fig. 2).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig2_Estandarizacion_mapeo.png" width=1000>

*Figura 2. Mapeo de datos en la plantilla DwC.*

## Paso 5 - Eliminar elementos vacíos 
Elimine en la plantilla de registros biológicos los elementos DwC que quedaron vacíos, recuerde que para la publicación solo debe mantener los elementos que hayan sido documentados.

Al finalizar su plantilla se debe ver similar a la siguiente imagen (Fig. 3):

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig3_Estandarizacion_mapeofinal.png" width=1000>

*Figura 3. Resultado final del mapeo de datos y eliminación de elementos vacíos.*


## Paso 6 - Ajustar datos  

Una vez esten todos los datos del archivo ```Datos_Caso1_20reg.xls``` en la plantilla de publicación, proceda a realizar los ajustes de calidad en los datos de acuerdo a las definiciones y vocabularios controlados del estándar para cada elemento mapeado.


<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab01/_images/Fig4_Estandarizacion_EstructuraPlantilla.png" width=1000>

*Figura 4. Estructura de la plantilla de publicación.*

## Paso 7 - Verificación de resultados 

Descargue el siguiente archivo estandarizado según las definiciones del estándar, compárelo con su archivo y verifique en que acertó y que fallas presenta.¿Logró completar mas información en la plantilla?.

* Descargue el archivo ```Datos_Caso1_20reg_estandarizado.xls```

## Paso 8 - Datos propios

**¿Cómo lo harías con tus propios datos?**
Si tienes datos propios que desees estandarizar en DwC, estandarizalos siguiendo los pasos de esta guía. Recuerda usar la plantilla que correponda según tu tipo de datos (Registros biológicos, Eventos, Listas de especies). 

Para registros biológicos siempre documenta los elementos obligatorios según el origen de tu publicación (**Paso 3**).

****

**¡Felicitaciones!** :raised_hands:
Su conjunto de datos ha sido estandarizado en DwC.
