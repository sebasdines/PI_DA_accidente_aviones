<p align='center'>
<img src ="src/portada.jpg">
<p>

<h1 align='center'>
 <b>PROYECTO INDIVIDUAL</b>

 <b>Data Analitycs</b>
</h1>
 
# <h1 align="center">**`Accidentes Aereos`**</h1>



### **Contexto**

Recibo un [cunjunto de datos](https://github.com/sebasdines/PI_DA_accidente_aviones/blob/main/src/AccidentesAviones.csv) formado por registros de accidentes aereos comprendidos entre 1908 y 2021.

<p align='center'>
<img src ="src/logo.png">
<p>
<h1 align="center">Organización de Aviación Civil Internacional (OACI)</h1>


 Este organismo de la Organización de las Naciones Unidas, nos pide investigar en profundidad los accidentes producidos desde inicios del siglo XX. Como objetivo principal debemos obtener un análisis de datos relacionado a esto, junto a un dashboard que complemente los análisis con sus visualizaciones. 

### **ETL**

Realizo un breve ETL en `Python` y su libreia `Pandas`, con el fin de normalizar datos, renombrar columnas para su mejor interpretación, se eliminan columnas irrelevantes y con muchos nulos, se crea una columna Country para la localizacion y filtrado de los accidentes.

### **EDA**

Para el Análisis Exploratorio de Datos, Visualizo el DF, el nombre de las columnas, el tamaño del DF y la informacion de las columnas.

Trato nulos, sumo los nulos de cada columna y obtengo el porcentaje de nulos.
Compruebo la existencia de duplicados.

Redacto un descripcion de cada columna:

#### **Diccionario de Datos**

* Fecha - Fecha del accidente
* Hora - Hora local, en 24 h. en el formato hh:mm
* Ubicación - Lugar del accidente
* Operador - Línea aérea u operador de la aeronave
* Vuelo: número de vuelo asignado por el operador de la aeronave
* Ruta: ruta completa o parcial volada antes del accidente.
* Tipo - Tipo de aeronave
* Registro - Registro OACI de la aeronave
* cn/In - Número de construcción o de serie / Número de línea o de fuselaje
* Total a bordo - Total de personas a bordo
* Pasajeros a bordo - Pasajeros a bordo
* Tripulación a bordo - Tripulación a bordo
* Total de víctimas mortales - Total de víctimas mortales
* Muertes de Pasajeros - Muertes de Pasajeros
* Muertes de la tripulación - Muertes de la tripulación
* Tierra - Total de muertos en tierra
* Resumen: breve descripción del accidente y causa, si se conoce.

Realizo tratemiento de Outliers en las columnas con valores numéricos, utilizando el 'zscore', obtenemos como resultado la ausencia de Outliers

Visualizamos tambien una descripción estadística de las columnas numericas.

### **Visualización de datos**

Con la ayuda de las librerias `Matplotlib` y `Seaborn` realizo visualizaciones de:

* Total de accidentes por año.
* Recuento de Aeronaves Militares y de Pasajeros.
* Recuento de sobrevivientes y fallecidos de la tripulación y de pasajeros.
* Operadores con mas accidentes en un Top 15
* Tipo de aeronave con mas accidentes en Top 15
* Paises con mas accidentes en Top 15


## **Importación de datos y modelado en Power BI**

Realizo la importación del .csv en `Power BI`, configuro el conjunto de datos, creo la tabla Calendario y la relaciono con accidentes_aviones.

`Dashboard`

Con los datos ya definidos confeciono el Dashboard:

* Aplicando filtros de Año, País y Tipo de Aeronave se logra localizar en el mapa el lugar del accidente.

* Se logra observar el recuento y la Tasa de sobrevivientes, asi como tambien la suma de personas abordo y sobrevivientes realizando el filtrado por Década, Año y País.

* También podemos obtener el numero de fallecidos discriminados por tripulación y pasajeros, filtrado por Año y País donde ocurrio el siniestro.

`KPI 1`

* Se solicita evaluar la disminución de la Tasa de fatalidad de la tripulación en los últimos 10 años en comparación con la decada anterior.
Se seleciona un período de 10 años y se compara con el período de 10 años anterior mostrando la tasa de crecimiento o de disminución, una tabla con la variación año a año y un grafico de columnas(accidentes por año) y lineas (tasa actual y tasa del período anterior)

`KPI 2`

* Implemento la tasa de fatalidad de pasajeros en accidentes en EEUU comparado con el periodo anterior en decadas, ej 1940 vs 1950.
Selecionando una decada en un filtro de mosaico, realiza la comparacion con la decada anterior mostrando la tasa de variación, una tabla año a año, un gráfico de áreas mostrando dicha variación y un mapa de localización que distingue los diferentes rangos diferenciados por color.

## **Autor**
### **Sebastian Di Nesta**
### **dinestasebas@gmail.com**
### [Github](https://github.com/sebasdines/PI_DA_accidente_aviones)
### [LinkedIn](https://www.linkedin.com/in/sebasti%C3%A1n-di-nesta-3241b1156/)




