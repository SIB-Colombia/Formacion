---
sort: 1
---

# Cómo importar archivos .txt o .csv en Excel

**Objetivo**

Realizar la correcta importación de datos en formato de texto plano a Excel.

**Sobre la actividad**

Existen dos formatos para el almacenamiento de archivos de texto ques son ampliamente usados para compartir datos, y que **no** corresponden al formato de **Microsoft Office Excel ®** (.xls, .xlsx, etc), estos archivos son los **delimitados por tabulaciones** y los **separados por comas**.

- **Archivos de texto delimitados por tabulaciones (.txt)**: en este formato el carácter de tabulación (tab) delimita cada campo de contenido almacenado en un archivo de texto. 
- **Archivos de valores separados por comas (.csv)**: en este formato el carácter de coma (,) o de punto y coma (;) separa cada campo de contenido almacenado.

En este laboratorio vamos la forma que [Microsoft Office Excel®](https://www.microsoft.com/es-co/microsoft-365/excel) provee para importar correctamente un archivo de formato  **.txt** o **.csv**. 

**Requerimientos** 

* Para realizar este ejercicio debe contar con Microsoft Excel.

**Archivo de trabajo**

Descargue el archivo [```Datos.zip```](https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_docs/Datos.zip). Deberá descomprimir el archivo para poder acceder a los contenidos que necesitará para realizar la guía: ```Datos.txt``` y ```Datos.csv```.

--------


## Paso 1 - Cargar datos

En el menu superior, seleccione la pestaña *Datos* > *Obtener datos externos* > *Desde texto* (Fig. 1).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_images/Fig.1_Datos-Importartexto.PNG" width=600>


<sup>_Figura 1. Selección de la fuente de datos._</sup>.

## Paso 2 - Selección del archivo

En el desplegable inferior seleccione la opción: Todos los archivos (*.*). Esto le permitira ver todos los archivos presentes en el directorio y seleccionar el adecuado (Fig. 2).

Y seleccione su archivo ```Datos.txt``` con terminación .txt y de clic en *Importar*(Fig. 2). 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_images/Fig.2_SeleccionArchivo.PNG" width=600>

<sup>_Figura 2. Selección del archivo._</sup>.


```note
Si al darle clic al botón de _Importar_, le aparecen mensajes referentes al formato de importación, de clic en _Sí_ o _Aceptar_.
```

## Paso 4 - Configuración del asistente para importar texto

Microsoft Office Excel® abrirá el ```Asistente para importar texto```, el cual cuenta con tres pasos principales.
En el primer paso, debera seleccionar el tipo de archivo y la codificación.

Seleccione ```Delimitados``` en la opción ```Tipo de los datos originales```.

Si no ve ningún tipo de carácter extraño en la vista previa, puede dejar seleccionada la opción por defecto en Windows ```Windows ANSI``` o ```Mancintosh``` para MacOS.

Si ve algun caracter extraño donde deben ir tíldes o ñ's principalmente, haga clic en la sección ```Origen del archivo:``` y en el desplegable seleccione la codificación correcta de los datos. La codificación más común es ```Unicode (UTF-8)```, luego de seleccionada debe revisar la Vista previa de los datos para revisar que no hayan más carácteres extraños (Fig. 3). 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_images/Fig.3_SeleccionCodificacion.PNG" width=600>

<sup>_Figura 3. Configuración del asistente para importar texto._</sup>.

En caso de persistir el problema, debe probar más configuraciones hasta encontrar la adecuada.

## Paso 5 - Configuración del los delimitadores

En el segundo paso del ```Asistente para importar texto``` debe escoger el tipo de separadore de sus datos. 

Para importar el archivo ```Datos.txt``` seleccione la opción ```Tabulación``` y revise en la vista previa que se separen las columnas adecudamente, luego de clic en ```Siguiente >``` (Fig. 4). 

Adicionalmente, debe revisar la opción Calificador de texto, para este ejercicio lo va a dejar configurado automáticamente con comillas dobles (").


```tip
Normalmente para los archivos .CSV el separador es una Coma, pero tambien pueden estar separados por Punto y coma si tiene los datos en español. Para archivos .TXT puede ser cualquier valor.
```

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_images/Fig.4_SeleccionSeparador.PNG" width=600>

<sup>_Figura 4. Configuración del asistente para importar texto paso 2._</sup>.

## Paso 6 - Configuración del formato de los datos

En el tercer paso del ```Asistente para importar texto```, en la Vista previa debe hacer clic sobre la primer columna de su conjunto de datos, luego presione la tecla ```Shift``` y sin soltarla arrastre la barra de deslizamiento hasta el límite derecho donde observará la última columna del conjunto de datos, de clic sobre esta columna y suelte la tecla ```Shift```. Esto le permite seleccionar todas las columnas del conjunto de datos.

Finalmente seleccione ```Texto``` en la opción ```Formato de los datos en columnas``` y haga clic en ```Finalizar``` (Fig. 5). 

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_images/Fig.5_SeleccionSitio.PNG" width=300>

<sup>_Figura 5. Configuración del asistente para importar texto paso 3._</sup>.


## Paso 7 - Importar datos

Se abrira una nueva ventana que le solicita indicar el lugar donde va a importar los datos, por defecto se importan en la primera hoja, fila 1, columna A. (Fig. 6). La recomendación es importar los datos en este lugar, pero puede seleccionar otra hoja o posición.
De clic en ```Aceptar``` para terminar el proceso de importación.


<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_images/Fig.6_SeleccionTexto.PNG" width=600>

<sup>_Figura 6. Configuración del asistente para importar texto paso 3._</sup>.

## Paso 8 - Importación de los datos en formato .csv

Repita este laboratorio usando los datos ```.csv```, la única diferencia es en el paso 5 donde debe seleccionar como separador la opción ```,``` (Fig. 8).

<img src="https://raw.githubusercontent.com/SIB-Colombia/Formacion/master/LAB/otros/_images/Fig.7_SeleccionSeparadorCSV.PNG" width=600>

<sup>_Figura 8. Selección de separador por Coma para los archivos de .csv._</sup>


****
**¡Felicitaciones!** :raised_hands:
Terminó la importar los datos correctamente a Excel.

****

**Atribución y uso de los laboratorios**

![](https://licensebuttons.net/l/by/3.0/88x31.png)

La licencia [CC-BY](https://creativecommons.org/licenses/by/4.0/) te permite usar, redistribuir y construir sobre estos contenidos libremente. :open_hands: Queremos que compartas estos laboratorios y que juntos logremos datos sobre biodiversidad de mejor calidad.

**Citación sugerida**

> Plata C., Ortíz R., Marentes E. (2021). Laboratorio de datos, Ciclo de formación. Consultado a través del SiB Colombia. Disponible en https://sib-colombia.github.io/Formacion/
> 
