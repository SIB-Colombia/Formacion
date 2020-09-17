---
sort: 2
---

# Validador de datos

#### *Data Validator* GBIF

**Objetivo**
Detectar posibles problemas en  la estructura y contenido de su conjunto de datos, y mejorar la calidad de los mismos para ser publicados a través del SiB Colombia, GBIF y/o OBIS.

**Sobre la Herramienta**
El [validador de datos](https://www.gbif.org/es/tools/data-validator/) es un servicio de [GBIF](https://www.gbif.org) que permite evaluar de manera automática la completitud y algunos aspectos de la calidad de un conjunto de datos estructurado en el estándar [Darwin Core (DwC)](https://dwc.tdwg.org/terms/), el validador genera un informe sobre la sintaxis y la calidad de los datos que le permitirá detectar posibles problemas en sus datos antes de publicarlos. Si se valida un [DwC-A](https://www.gbif.org/darwin-core) el validador también evalua la completitud y estructura de los metadatos en el estándar [EML](https://www.gbif.org/sites/default/files/gbif_resource/resource-80640/gbif_metadata_profile_guide_en_v1.pdf).

**Enlace** 
https://www.gbif.org/es/tools/data-validator/

**Requerimientos** 
* La primera fila del conjunto de datos a validar debe tener el nombre de los elementos DwC en inglés.

* El conjunto de datos debe tener la columna del ID de tipo de datos que corresponda, ```occurenceID ```(registros biológicos), ```eventID``` (eventos de muestreo)o ```taxonID``` (listas de especies). La columna debe estar documentada para todas las filas y los ID's deben ser únicos.

* El validador admite archivos con los siguientes formatos:
  * Formato Excel (.xls,.xlsx)
  * Formato CSV.
  * Archivos Darwin Core comprimidos (DwC-A)

**Archivo de trabajo**
Descargue el archivo [```datos_Estructurados.xls```](https://www.gbif.org/tools/data-validator.) para realizar el laboratorio

----

 ## Laboratorio
 
### Paso 1

Cree una cuenta de usuario en [GBIF](https://www.gbif.org) o, si ya está registrado, ingrese con sus credenciales al [validador de datos.](https://www.gbif.org/es/tools/data-validator/)

[Fig1_dataValidator.png]
###### Figura 1.

### Paso 2
Cargue el archivo *```datos_Estructurados.xls```*  al validador; (1) haciendo clic en SELECT FILE y seleccionando el archivo o (2) arrastrando el archivo desde una carpeta y soltandolo en el ícono *Drop here*. 

> **Advertencia**, es indispensable que el elemento *occurrenceID* este documentado para que el DataValidator reconozca el archivo

El validador le indicará si el conjunto de datos tiene la estructura adecuada para ser publicado  a través del SiB Colombia, GBIF y OBIS, o si es necesario realizar ajustes. El informe de validación contiene la siguiente información:


* Un indicador semaforizado (rojo y verde) que indica si puede el conjunto de datos puede ser indexado (Fig. 2 A).
* Resumen del tipo de conjunto de datos (Fig. 2 B).
* Alertas de validación que indican **potenciales** problemas en la estructuración y calidad del conjunto de datos (Fig. 2 C).

[paso2-1_dataValidator.jpg]
###### Figura 2.


* Número de registros (filas) interpretados con éxito (Fig. 3 A).
* Reporte del porcentaje de documentación de cada uno de los elementos del estándar DwC utilizados en el conjunto de datos (Fig. 3 B), sección **Frecuencia del término**.

[paso2-2_dataValidator.jpg]
###### Figura 3.

### Paso 3

Revise detalladamente el resultado de la validación 

#### 3.1. ¿Su conjunto de datos puede ser indexado? 

Revise el encabezado del reporte, si aparece en rojo significa que no puede ser indexado (Fig. 4A), si aparece en verde significa que si lo peude indexar (Fig. 4B).Si el conjunto no puede ser indexado revise el mensaje de alerta de la herramienta (Fig. 4C).

[Fig.4A-B_dataValidator.jpg]
###### Figura 4.

Los casos más frecuentes por los cuales un archivo no puede ser indexado son:

a. Mensaje *Registro no identificado de forma única*, indica que los ID's documentados en el elemento DwC  *occurrenceID* (*taxonID, eventID*,según el tipo de datos) NO son únicos

> En la sección **Problemas de validación**  encontrará los ID’s que están duplicados.

Realice los ajustes necesarios y vuelva  a correr la validación, en esta ocasión el validador le indicará que el conjunto de datos se puede indexar (Fig. 4B).

b. Mensaje *No se encontró o determinó un rowType* indica que algunas de las columnas obligatorias para realizar la validación no se encuentran en el conjunto de datos, por ejemplo occurrenceID, taxonID, o eventID, según el tipo de datos. 


#### 3.2. Revise los **Problemas de validación**

Dirijase a la sección **Problemas de validación** y revise cada una de las alertas. Para cada una de las alertas, el validador indica el número de registros a revisar (Fig. 5).

[Fig.5_dataValidator.png]
###### Figura 5. 

Haga clic sobre las flechas de cada una de las alertas para obtener un desglose de los registros que deben ser revisados y/o ajustados (Fig. 6). 

[Fig.6_dataValidator.png]
###### Figura 6.


Para interpretar las alertas de validación utilice el botón de ayuda, y obtendrá una breve explicación.

[Fig.7_dataValidator.png]
###### Figura 7.


#### A continuación se explican las alertas más frecuentes:

* Alertas de color **ROJO** - Indican un error estructura que no permite la indexación del recurso y debe ser corregido.

* Alertas de color **AMARILLO** - Indican potenciales errores, deben ser revisadas con detalle para determinar si se debe o no hacer una corrección en los datos.

* Alertas de color **GRIS** - Indican el proceso de interpretación realizado por el validador, no necesariamente requiere que se realicen ajustes en los datos.
---

**Alerta**: Base del registro inválida

**Problema**: la base del registro  (basisOfRecord) no cumple con los requerimientos del estándar.

**Solución 1**: revise que todos los registros (filas) tengan este elemento documentado.

**Solución 2**: documente el elemento siguiendo el vocabulario controlado en inglés, ```HumanObservation, PreservedSpecimen, LivingSpecimen, MachineObservation, MaterialSample FossilSpecimen.```

[reference link]
-

**Alerta**: ‘Coordinate invalid’

**Problema**: coordenadas inválidas, las coordenadas documentadas no se encuentran estandarizadas en coordenadas decimales y/o las coordenadas originales no se pueden interpretar.

**Solución**: asegúrese que los elementos darwin core ‘decimalLatitude’, ‘decimalLatitude’  estén documentados con las coordenadas en formato decimal y/o que las coordenadas originales ‘verbatimCoordinates’ hayan sido digitalizadas adecuadamente. 

[reference link]

#### Alerta - Se presume latitud negativa
**Problema**: posible error en la latitud, se documentó como latitud sur pero posiblemente corresponda a  latitud norte (en coordenadas decimales se indica con un signo menos antes de la latitud).  

**Solución**: asegúrese que los elementos darwin core *decimalLatitude*, *decimalLatitude*  estén documentados con las coordenadas en formato decimal y/o que las coordenadas originales *verbatimCoordinates*, *verbatimLatitud*, *verbatimLongitude* hayan sido digitalizadas adecuadamente. 

[reference link]
###### Figura

**Alerta**: Coincidencia Taxón - Taxonomía superior

**Problema**: el nombre científico fue validado a un nivel taxonómico superior al documentado, por ejemplo si el nombre científico corresponde a una especie (género + epíteto específico) significa que el validador solo pudo interpretar el género más no el epíteto específico.

**Solución 1.**: revise que el nombre científico no contenga calificadores de la identificación  (cf., aff.) u otros calificadores como *sp.*  
**Solución 2.**: que el nombre científico esté escrito correctamente.

> Es posible que algunos nombres válidos y correctamente escritos sean marcados con esta alerta si es que estos no se encuentran en el [árbol taxonómico de GBIF](https://www.gbif.org/dataset/d7dddbf4-2cf0-4f39-9b2a-bb099caae36c). Esto es común en el caso de especíes endémicas o recientemente descritas. En tal caso ignore la alerta.

[reference link]

**Alerta**: Coincidencia aproximada del taxón

**Problema**: hay una coincidencia parcial del nombre cíentífico y el [árbol taxonómico de GBIF](https://www.gbif.org/dataset/d7dddbf4-2cf0-4f39-9b2a-bb099caae36c), por lo general esta alerta se genera cuando hay errores de tipeo  menores en el nombre científico.

**Solución**: asegúrese que el nombre científico esté escrito correctamente.


[reference link]

**Alerta**: Fecha registrada inválida

**Problema**: el formato de la fecha no cumple con el formato ISO 8601: ```AAAA-MM-DD; AAAA-MM; AAAA; AAAA-MM-DD/AAAA-MM-DD```

**Solución**: estandarice las fechas al formato ISO 8601


[reference link]

**Alerta**: Datum geodésico WGS84 asumido

**Problema**: el datum geodésico no fue documentado, pero el validador lo identificó como WGS84.

**Solución 1**: documentar el elemento DwC  ```geodeticDatum``` como WGS84,

**Solución 2**: si las coordenadas tienen un datum diferente a WGS84 documentelo para evitar que este sea asumido.

[reference link]

### Paso 4
Después de revisar todas las alertas de validación y ajustar los datos de acuerdo a estas cargue nuevamente el conjunto de datos en el validador para confirmar el estado de calidad de los datos.

### Paso 5

Si realizó el laboratorio con un conjunto de datos propio, revise en la sección **Frecuencia del término** el reporte del porcentaje de documentación de los elementos de su conjunto de datos.

Según el origen se sus datos (colecciones biológicas, permisos de recolección, datos marinos, eventos de muestreo) compruebe que los elementos obligatorios, e idealmente los recomendados, esten documentados el 100%. Para ello utilice la de referencia la ultima [plantilla DwC Registros biológicos](https://sites.google.com/humboldt.org.co/wikisib/publicar/plantillas?authuser=0)


**¡Felicitaciones!** 
Su conjunto de datos ha sido estructurado adecuadamente.
