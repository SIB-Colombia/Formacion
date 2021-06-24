---
sort: 7
---

# Visualización Coordenadas

**Objetivo**

Visualizar y validar las coordenadas con un proceso de espacialización sobre un mapa base en línea.

**Sobre la herramienta**

La herramienta [OBIS Plotter](http://iobis.github.io/plotter/), desarrollada por [OBIS](https://obis.org/) (Sistema de información de biodiversidad oceánico), permite la visualización de los datos sobre un mapa para verificar la correcta espacialización de los datos.
En este ejercicio usted deberá convertir las coordenadas al formato grados decimales haciendo uso de esta herramienta.


**Enlace**

_OBIS Plotter_: [iobis.github.io/plotter/](http://iobis.github.io/plotter/)

**Requerimientos** 

* Para realizar este ejercicio debe contar con un programa procesador de archivos de texto como Excel.
* La herramienta solo admite archivos en formato de texto delimitado (.CSV, .txt) o copiados directamente de Excel.
* Los datos deben estar estandarizados en formtado DwC y contar con latitud y longitud.

**Archivo de trabajo**

Descargue el archivo [```datos_geografia.xlsx```](https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_docs/datos_geografia.xlsx) 

--------

## Paso 1 - Ingreso a OBIS Plotter
Ingrese a la herramienta en línea [OBIS Plotter](http://iobis.github.io/plotter/). Encontrará unos datos precargados de prueba. Puede dar clic al botón *```PLOT```* y explorar el resultado (Fig. 1).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig.1_valCoordenadas.JPG" width=500>

<sup>*Figura 1. Página principal de la herramienta OBIS Plotter*.</sup>

Después de explorar el resultado, borre los datos de prueba presentes en *```Source data```*, para esto ubique el cursor dentro de la caja y seleccione todo con el comando **(Ctrl + A)**, enseguida presione la tecla Suprimir **(Supr)** o borrar **(Backspace)**. 


## Paso 2 - Carga de datos
Abra en Excel el archivo ```datos_geografia.xlsx``` y detalle la información que contiene. Copie todos los datos del archivo, dando clic en la esquina superior izquierda para seleccionar todas las filas y columnas, luego copielos con  **(Ctrl+C)** (Fig. 2).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig.2_valCoordenadas.jpg" width=500>

<sup>*Figura 2. Resultado de la herramienta con los datos del archivo Excel*.</sup>

Pegue **(Ctrl+V)** los datos en la sección *```Source data```* de la herramienta. En la sección *```Separator```* deje la opción por defecto *tab* y de clic en *```Plot```* para ver los puntos desplegados en el mapa (Fig. 3).
<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig.3_valCoordenadas.jpg" width=500>

<sup>*Figura 3. Resultado de la herramienta con los datos del archivo Excel*.</sup>

## Paso 3 - Visualización de resultados
En la sección *```Field of interest```*, de clic sobre el desplegable *```Select field```* y podrá ver los elementos Darwin Core cargados en el *Source data* (Fig. 4). La herramienta asigna colores según el contenido del elemento. 
<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig.4_valCoordenadas.jpg" width=500>

<sup>*Figura 4. Selección del departamento (stateProvince) en Field of interest*.</sup>

Seleccione el elemento *stateProvince* en la sección ```Field of interest```. Verá los registros con el departamento documentado.  Ahora Intente identificar cuáles registros tienen inconsistencias en las coordenadas o la geografía superior dando clic sobre los puntos y evaluando su coherencia respecto a la ubicación en el mapa (Fig. 5).  Tenga en cuenta que si los puntos tienen los mismos colores, es porque el contenido para el elemento seleccionado es el mismo (Fig. 5).
<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig.5_valCoordenadas.jpg" width=500>

<sup>*Figura 5. Registros mostrando la información por departamento*</sup>

Identifique los errores presenten en este conjunto de datos, para ello puede guiarse por los resultados del mapa. Como verá hay puntos que coincidieron con Perú y otros con el área marítima. Los datos que coinciden con Perú tienen un error en las coordenadas. **¿Sabe cuál es?** 

>Nota
Los registros en áreas marítimas corresponden a registros sin coordenadas a los cuales la herramienta asigna la coordenada 0,0.

## Paso 4 - Corrección de errores
Corrija el error en el documento de Excel, para esto cambie el hemisferio en el elemento *```decimalLatitude```* quitando el signo negativo a las coordenadas que tienen hemisferio Sur (S). 
Para esto, haga un filtro en excel en el  elemento *```verbatimLatitude```*, buscando los registros que coinciden con el hemisferio Sur “S” (Fig. 6).
<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig.6_valCoordenadas.jpg" width=400>

<sup>*Figura 6. Filtro para buscar los registros del hemisferio Sur*</sup>

Luego dirijase al elemento *```decimalLatitude```* y después de aplicar el filtro anterior encontrará las latitudes que tienen un signo negativo. Cámbielo a positivo seleccionando las celdas de *```decimalLatitude```* y use la función **Buscar y Reemplazar (CTRL+L)** de Excel, llenando la ventana emergente y cambiando "-" por "" (Fig. 7).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/lab02/_images/Fig.7_valCoordenadas.jpg" width=800>

<sup>*Figura 7. Ventana emergente para reemplazar y eliminar el signo "-"*</sup>

:warning: Si al realizar este útlimo paso observa que cambia la configuración de la celda y la coordenada se convierte en un número entero separado por miles, es probable que deba cambiar la configuración de las opciones avanzadas de Excel para que reconozca el punto como separador decimal.

**Reto...**
¿Puede identificar otro error en los registros? 

:vertical_traffic_light: Pista: Con el elemento *```stateProvince```* seleccionado en *```Field of interest```* revise detalladamente los registros presentes al sur de Antioquia. 

## Paso 5 - Datos propios
Si tiene datos propios que desee publicar utilice la herramienta para validar las coordenadas e identificar errores siguiendo los pasos de este laboratorio.

****
**¡Felicitaciones!** :raised_hands:
Terminó la visualización y validación de coordenadas del conjunto de datos.

****

**Atribución y uso de los laboratorios**

![](https://licensebuttons.net/l/by/3.0/88x31.png)

La licencia [CC-BY](https://creativecommons.org/licenses/by/4.0/) te permite usar, redistribuir y construir sobre estos contenidos libremente. :open_hands: Queremos que compartas estos laboratorios y que juntos logremos datos sobre biodiversidad de mejor calidad.

**Citación sugerida**

> Plata C., Ortíz R., Marentes E. (2021). Laboratorio de datos, Ciclo de formación. Consultado a través del SiB Colombia. Disponible en https://sib-colombia.github.io/Formacion/
> 
