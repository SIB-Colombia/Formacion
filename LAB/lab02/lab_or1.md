---
sort: 1
---

# Open Refine :gem:


**Objetivo**

Utilizar _Open Refine_ para manejar, validar y limpiar de manera eficiente datos sobre biodiversidad, asegurando una mejor calidad para su publicación.

**Sobre la Herramienta**

[_Open Refine_](https://openrefine.org/) es un software creado con el objetivo de pulir datos crudos hasta convertirlos en diamantes :gem:, activos valiosos en la era del _BigData_ .


Este sofware permite visualizar y manipular datos tabulares facilitando mejorar la calidad general de un conjunto de datos. Tiene la apariencia de un software tradicional de hoja de cálculo -similar a Excel, pero funciona como una base de datos. Esto significa que _OpenRefine_ no es adecuado para adicionar nuevas filas de datos, pero **es extremadamente poderoso cuando se trata de explorar, limpiar y vincular datos**. 

_Open Refine_ se instala localmente por lo cuál funciona como una aplicación web personal y de acceso privado, al que se accede desde un navegador web.

**Requerimientos** 

1. Navegador Chrome o Mozilla Firefox instalado, y configurado como navegador predeterminado.

``` warning
No utilice Internet Explorer para este laboratorio ya que Open Refine no funciona bien con este navegador web.
```

**Archivo de trabajo**

Descargue el archivo [```datos_Estructurados.xlsx```](https://github.com/SIB-Colombia/Formacion/raw/master/LAB/lab02/_docs/datos_Estructurados.xlsx)


--------

## Instalación 


> Asegúrese de que su navegador predeterminado sea Chrome o Mozilla


### Instalación en Windows
1. Descargue [Open Refine versión 3.4.1 + Java para Windows](https://github.com/OpenRefine/OpenRefine/releases/download/3.4.1/openrefine-win-with-java-3.4.1.zip).
2. Descomprima el archivo descargado y copie la carpeta resultante en el disco local (C:/)
3. Abra la carpeta y haga doble clic en openrefine.exe.
4. Aparecerá una ventana de comando (que no debe cerrar) e inmediatamente después su navegador web mostrará una nueva ventana con la aplicación.


### Instalación en Mac
1. Descargue [Open Refine versión 3.4.1 + Java para Mac](https://github.com/OpenRefine/OpenRefine/releases/download/3.4.1/openrefine-mac-3.4.1.dmg).
2. Haga doble clic sobre el archivo de descarga y arrastre el icono en la carpeta Aplicaciónes.
4. Haga doble clic en él icono y su navegador web mostrará una nueva ventana con la aplicación.
5. Si al dar doble clic no abre _Open Refine_ en el navegador,  escriba la siguiente dirección en el buscador: [http://127.0.0.1:3333/](http://127.0.0.1:3333/)

## Crear un proyecto

Puede cargar datos con diferentes formatos y extensiones: TSV, CSV, SV, Excel (.xls y .xlsx), JSON, XML, RDF as XML y datos de Google Docs.


**1. Abrir un nuevo proyecto**

Abra _Open Refine_** y diríjase a la pestaña ```_Create Project_```. Para cargar el archivo siga la ruta ```_Get data from > This Computer_```, y haga clic en ```_Choose Files_``` (Fig. 1).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig1_OR_cargar.png" width=800>

_Figura 1. Creación de un proyecto en Open Refine_

**2. Selección del archivo**

Seleccione el archivo ```Datos_Estructurado.xlsx``` que descargó al incio del laboratorio y haga clic en _```Next```_ (Fig. 1).


> Puede subir varios archivos a la vez, el software unirá los archivos basados en los encabezados de las columnas.
> 

**3. Configuración del archivo**

Tras seleccionar el archivo aparecerá un panel de configuración, este le permite especificar el tipo de archivo que cargó y configurar la manera en la que los datos son leídos (Fig. 2). 

_Open Refine_ hace una interpreteación automática del tipo de archivo, codificación del texto y filas de encabezado, entre otros. El conjunto de datos de ejemplo de este laboratorio es intepretado de manera correcta y no necesita ajustes adicionales. 

```warning
Si sube sus propios datos o utiliza otro formatos debe fijarse en la vista previa del archivo y ajustar la configuración de lectura (Fig. 2).
````

 - **A.** Tipo de archivo, permite configurar el tipo de la fuente de datos
 - **B.** Hojas a importar, si carga uno o varios archivos con multiples hojas, puede seleccionar que hojas desea importar y cuales no.
 - **C.** Seleccion de filas, permite seleccionar la fila que se convertira en el encabezado de las columnas, ignorar filas, entre otros.
 - **D.** Carga de filas en blanco, permite especificar si seran cargadas y como serán cargadas. 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig2._OR_config.png">

_Figura 2. Opciones para configurar la lectura y carga de los datos para un archivo Excel (.xls y .xlsx)_


**4. Personalización del proyecto y carga del archivo**

Cambie el nombre del proyecto, en la esquina superior derecha verá un cuadro de texto en el que  puede cambiar el nombre del proyecto, nómbrelo ```Datos_OR``` y haga clic en el botón ```Create Project``` (Fig. 3). Opcionalmente puede añadir _Tags_ (etiquetas) para poder organizar y filtrar los proyectos en la aplicación.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig3._OR_renombrar.png" width=800>

_Figura 3. Cambiar el nombre del proyecto._


Espere a que cargue el archivo, esto puede tomar un tiempo dependiendo del tamaño del mismo.

## _Faceting_

Es un método para filtrar los datos en conjuntos más pequeños facilitando la validación y limpieza de los datos, puede hacerse para texto, números y fechas.

### Correcciones masivas

**1. Crear un _Text Facet_**

Diríjase a la columna _```class```_, haga clic en el menú de la columna y siga la ruta _```Facet >Text Facet```_ (Fig. 4).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig4_OR_facet.png" width=400>

_Figura 4. Creación de un ```Text Facet```._

**2. Organizar el _Text Facet_**

El _Text Facet_ creado aparecerá a la izquierda de la aplicación, verá una ventana con el nombre de la columna y el _Facet_ que acaba de crear (Fig. 5). Haga clic en _count_ para organizar las clases de la más a la menos abundante y en _name_ para organizarlas en orden alfabético.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig5_OR_facet2.png" width=400>

_Figura 5. Vista del Text Facet y las opciones para organizar las opciones de texto de la columna._

**3. Corrección de los datos**

Corrija las inconsistencias en los nombres de las clases ```Aves``` y ```Mammalia```. Para esto acerque el cursor al valor que desea corregir y haga clic en *Edit*, luego en el cuadro de texto que aparece corrija el error y haga clic en _Apply_ (Fig. 6). Todos los valores serán corregidos de manera automática y las celdas se transformarán de forma masiva.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig6_OR_classCorrect.png" width=400>

_Figura 6. Correción masiva de la columna ```class``` usando un Text Facet._

Realice el mismo proceso con la columna _```basisOfRecord```_ y _```sex```_  ajustandolas al vocabulario controlado de cada elemento (Refierase al [laboratorio de estandarización](https://sib-colombia.github.io/Formacion/LAB/lab01/lab_dwc.html))(Fig. 7).


<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig7_OR_otrosCorrect.png" width=400>

_Figura 7. Correción masiva de las columnas ```basisOfRecord``` y ```sex``` usando un Text Facet._


Al finalizar este ejercicio diríjase en el menú lateral y seleccione la opción Remove All (Fig. 8). Así removerá todos los Facets y Filtros que tenga en uso.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig8_OR_remover.png" width=400>

_Figura 8. Remover todos los facets y filtros activos_


### Limpieza de espacios en blanco

Diríjase a la columna _```individualCount```_, haga clic en el menú  de la columna y realice un _```Text Facet```_.
A su izquierda aparecerá la ventana con el nombre de la columna y el Facet que se realizó (Fig. 9).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig9_OR_individual.png" width=400>

_Figura 9. Vista del Text Facet y las diferentes formas de docuemntación del elemento ```individualCount```._

Aunque a simple vista los datos se encuentran sin errores, al realizar este procedimiento vemos que el programa ha detectado espacios extra y por eso nos muestra cuatro opciones diferentes para el valor ```1```.
Corrija las inconsistencias desde el menú de la columna _```individualCount```_, siguiendo la ruta _```Edit Cells > Common transforms > Trim leading and trailing whitespace```_, verá un mensaje de notificación que le indicará en cuantas celdas se eliminaron espacuios (Fig. 10).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig10_OR_trimSpaces.png" width=600>

_Figura 10. Transformación de la columna para eliminar dobles espacios y espacios al final del texto._

Observe la ventana del _Facet_ de _```individualCount```_, notará que ahora solo existe una opción y que los espacios fueron eliminados.

Al finalizar este ejercicio diríjase al menú lateral y seleccione la opción _```Remove All```_. Así removerá todos los _Facets_ y Filtros que tenga en uso.

### Deteción de duplicados

Diríjase a la columna _```catalogNumber```_, haga clic en el menú de la columna y siga la ruta _```Facet > Customized facets > Duplicates facet```_, a su izquierda verá la ventana del _Facet_(Fig. 11).


Podemos ver que el programa ha detectado valores únicos _```false```_ y valores duplicados _```true```_ (Fig. 12).Haga clic en true y verá los registros. De esta manera se pueden detectar los duplicados para un análisis posterior. En este caso corrija el registro de ```Feb 2001``` por ```46-2300MI2008AV0248``` tanto en _```catalogNumber```_ como en _```occurrenceID```_; como se puede observar en la imagen a continuación.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig12_OR_fixDuplicates.png" width=600>

_Figura 12. Revisión de los registros duplicados y corrección de los identificadores._

Al finalizar este ejercicio diríjase al menú lateral y seleccione la opción _```Remove All```_. Así removerá todos los _Facets_ y Filtros que tenga en uso.

## Filtros

### Corección combinando filtros y funciones

**1. Corrección elmento _```scientificName```_**

Diríjase a la columna _```scientificName```_, haga clic en el menú de la columna  y luego en _```Text filter```_, aparecerá la ventana del Filtro.
Escriba en el campo de texto ```sp.``` y realice un _```Text Facet```_ en _```scientificName```_ para visualizar los registros con este valor.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig13_OR_sp.png" width=400>

_Figura 13. Aplicación de un filtro de texto a la columna```scientificName```e identificación de nombres científicos a corregir._


Este tipo de identificación parcial no debe documentarse en el elemento _```scientificName```_, para ello se emplea el elemento _DwC_ _```verbatimTaxonRank```_.

Realice un _```Text Facet```_ en _```verbatimTaxonRank```_ y edite masivamente reemplazando las celdas vacías (_blank_) con ```sp.```, haga clic en _Apply_ (Fig. 14).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig14_OR_sp2.png" width=400>

_Figura 14. Documentación masiva del elemento ```verbatimTaxonRank``` ._


Diríjase nuevamente al menú de la columna de _```scientificName```_ y siga la ruta _```Edit cells > Transform```_, luego ingrese la fórmula  _```value.replace(" sp.","")```_ (Fig. 15). Haga clic en _OK_ y aparecerá un mensaje de confirmación de que los cambios se han realizado.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig15_OR_replace.png" width=800>

_Figura 15. Transformación masiva de los datos usando comando ```value.replace()``` del lenguaje GREL de Open Refine._

Empleando este comando _```value.replace```_ se puede sustituir cualquier valor de una columna poniendo dentro de un paréntesis inicialmente el valor a buscar (ej. " sp."), entre comillas [ “ ] y luego separado por una coma [ , ] el valor de reemplazo - en este caso ninguno por lo cual se ponen unas comillas vacías [""].

**2. Corrección elmentos _```recordedBy```  ```identifiedBy```_**

Corrija las columnas _```recordedBy```_ e _```identifiedBy```_ y, empleando la misma función _```value.replace```_ del punto anterior, reemplace en cada una el carácter de separación entre los nombres ["; "] por el que acepta el estándar Darwin Core actualmente para este elemento [" | "] (Refierase al [laboratorio de estandarización](https://sib-colombia.github.io/Formacion/LAB/lab01/lab_dwc.html)).

Al finalizar este ejercicio diríjase al menú lateral y seleccione la opción _```Remove All```_. Así removerá todos los _Facets_ y Filtros que tenga en uso.

### Filtros con expresiones regulares

**1. Corrección elmento _```family```_** 

Diríjase a la columna _```family```_  y realice un _```Text Facet```_. Haga clic en el menú de la columna y luego en _```Text filter```_. Aparecerá la ventana del Filtro.
Marque la casilla _regular expression_. Escriba en el campo de texto la expresión regular  ```.*(?:(?!ae).).$``` esta expresión permite excluir todas las palabras de la columna que no terminan en ```ae```, correspondiente a las últimas letras de la declinación en latín para la categoría taxonómica de familia (*idae*, *ceae*) (Fig, 16).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig16_OR_regulasExp.png" width=400>

_Figura 16. Uso de expresiones regulares en GREL para filtrar la columna ```family``` ._

Podrá observar como los registros que no corresponden a familias han sido filtrados, usted puede editarlos haciendo uso de las opciones aprendidas en pasos previos. En este caso particular reemplace ```Bolitoglossa```, que corresponde a un Género, por ```Plethodontidae```,la Familia a la que pertenece el nombre científico (Fig. 16).

> Para conocer más de las expresiones regulares diríjase a la [documentación de _Open Refine_](https://github.com/OpenRefine/OpenRefine/wiki/Understanding-Regular-Expressions).

Al finalizar este ejercicio diríjase en el menú lateral y seleccione la opción Remove All. Así removerá todos los Facets y Filtros que tenga en uso.

**2. Corrección elmentos _```scientificName```_ _```identificationQualifier```_** 

Diríjase a la columna _```scientificName```_, haga clic en el menú de la columna  y luego en _Text filter_, aparecerá la ventana del Filtro. Marque la casilla _regular expression_. Escriba en el campo de texto la expresión regular  ```[.]``` y realice un _T```ext Facet```_ para visualizar los registros con este  elemento(Fig. 17).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig17_OR_qualifier.png" width=400>

_Figura 17. Uso de expresiones regulares en GREL para filtrar y corregir las columnas ```scientificName``` ```identificationQualifier```._

Podrá observar los registros que cumplen con el criterio de la expresión regular. El elemento _```identificationQualifier```_ está diseñado para almacenar este tipo de información y por su parte el elemento _```scientificName```_ debe encontrarse sin calificadores.

Para hacer el ajuste realice un _```Text Facet```_ en el elemento _```identificationQualifier```_ para editar masivamente, de manera que en los blank se documente “cf. sowelli” y se borre en el _```scientificName```_ (Fig. 17).

Finalmente estos registros deben quedar documentados con el género Carollia en _```scientificName```_ y en _```identificationQualifier```_ el valor ```cf. sowelli``` (Fig. 18).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig18_OR_qualifierFix.png" width=400>

_Figura 18. Documentación corregida y correcta de los elementos ```scientificName``` ```identificationQualifier```._

Al finalizar este ejercicio diríjase al menú lateral y seleccione la opción _```Remove All```_. Así removerá todos los _Facets_ y Filtros que tenga en uso.
## Conjuntos

Diríjase a la columna _```recordedBy```_, haga clic en el menú de la columna y luego en _```Text facet```_, aparecerá la ventana del Facet con más de 200 opciones  (_choices_) diferentes (Fig. 19).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig19_OR_cluster1.png" width=400>

_Figura 19. Facet y opciones del elemento ```recordedBy```._


En la parte superior derecha verá el botón _Cluster_ haga clic (Fig. 19), aparecerá la ventana de _Cluster &  Edit_ para la columna _recordedBy_ (Fig. 20).

Podrá ver la siguiente información:

- ***Cluster size***: La cantidad versiones del dato que el algoritmo identifica como similares.
- ***Row count:*** El número de registros por cluster.
- ***Values in cluster:*** Los valores seleccionados por el algoritmo para esa agrupación y el número de registros por valor.
- ***Merge?:*** En este cuadro se selecciona si los valores se fusionan en el valor que propone el algoritmo por defecto o el documentado por el usuario. 
- ***New cell value:*** En este campo de texto se puede escribir un valor completamente nuevo para el _cluster_. También se puede hacer clic en cualquier valor para asignarlo como valor por defecto.

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig20_OR_cluster2.png" width=800>

_Figura 20. Detalle de la ventana ventana de Cluster &  Edit para hacer realizar clusters y las opciones de configuración disponibles._


Vaya a _```Keying Function```_, seleccione _```ngram-fingerprint```_ y en _```Ngram Size```_ escriba ```1``` (Fig. 20).

> Para conocer más acerca de los algoritmos diríjase a la [documentación de _Open Refine_](https://github.com/OpenRefine/OpenRefine/wiki/Understanding-Regular-Expressions).

- Para el primer cluster asigne un valor nuevo, para esto vaya al cuadro de texto de _```New cell value```_ y escriba ```David H | Arango A | Bedoya J``` (dejando espacios sencillos). Luego haga check en el cuadro de _```Merge?```_ para ese _cluster_ (Fig. 20).

- Para el segundo _cluster_ haga clic en ```Vargas I``` (la primera opción: sin espacios adicionales), automáticamente el valor en _```New cell value```_ cambiará y la casilla _```Merge?```_ se chequeará (Fig. 20).

- Con los restantes evalúe si se deben o no agrupar dependiendo de las opciones disponibles y escoja en tal caso si selecciona o no la casilla.

Una vez escoja las entradas que desee fusionar vaya a _```Merge Selected & close```_ para agrupar los valores y volver a la ventana principal. 


Observe que la cantidad de opciones de datos disminuyó y que la primera entrada de nombres ha cambiado, es decir la información se simplificó y organizó correctamente gracias a este proceso.

Al finalizar este ejercicio diríjase al menú lateral y seleccione la opción _```Remove All```_. Así removerá todos los _Facets_ y Filtros que tenga en uso.

## Uso avanzado

:wrench: 🔨 :hammer: Este parte del laboratorio estará disponible a partir del **Viernes 02 de Octubre del 2020**
