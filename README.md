# Análisis del Sector de Telecomunicaciones en Argentina

Este repositorio contiene un análisis sobre el comportamiento del sector de telecomunicaciones en Argentina, 
específicamente del acceso a internet en ese país.
El objetivo principal de este análisis es brindar información clave para mejorar la calidad de los servicios y 
detectar oportunidades de crecimiento en el mercado. Para lograrlo, se llevará a cabo un Análisis Exploratorio de 
Datos (EDA) y se creará un Dashboard interactivo para presentar los resultados de manera visual y accesible.

## Estructura del Repositorio

- **Limpieza de datos**: Archivo en el que se realiza el preprocesamiento de los datasets para su posterior uso.
El archivo puede encontrarse [aquí](https://github.com/hernandroz/telecomunicaciones_project/blob/main/limpieza_datos.ipynb).
- **EDA**: Notebook con el Análisis Exploratorio de Datos. Puede encontrarse [aquí](https://github.com/hernandroz/telecomunicaciones_project/blob/main/internet_eda.ipynb).
- **Dashboard**: [Carpeta](https://github.com/hernandroz/telecomunicaciones_project/tree/main/dashboard) con los archivos del Dashboard interactivo.
- **Datasets**: Archivos csv utilizados en el análisis. Todos se obtuvieron de: https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/
- **Readme**: Es el actual archivo en el que se explica todo el trabajo de forma general.

## Análisis

### 1. Análisis Exploratorio de Datos

Para comenzar, es importante aclarar que en Argentina los términos "provincia", "partido" y "localidad" se refieren a subdivisiones
territoriales de dicho país.

Con los datos disponibles, se pudo identificar a las provincias que tienen más hogares con acceso a internet:

![](https://github.com/hernandroz/telecomunicaciones_project/blob/main/imagenes_readme/top10pr.png?raw=true)

Además, se pudo observar que existe un enorme sesgo respecto a la velocidad de internet de 5 mbps:

![](https://github.com/hernandroz/telecomunicaciones_project/blob/main/imagenes_readme/histog_conec_5mbps.png?raw=true)

Por otra parte, se identificó a los partidos con mayor cantidad de conexiones 4G:

![](https://github.com/hernandroz/telecomunicaciones_project/blob/main/imagenes_readme/top10part_con4g.png?raw=true)
 
 Algo importante a remarcar es que, usando las coordenadas de las ubicaciones con acceso a internet, pudimos establecer
 un diagramama de dispersión en el que es notorio la semejanza con el territorio geográfico de Argentina, y que además permite ver
 en qué zonas existe un mayor acceso a internet para la población, y en qué zonas existe uno menor:

 ![](https://github.com/hernandroz/telecomunicaciones_project/blob/main/imagenes_readme/longitudvslatitud_hue.png?raw=true)

 (La variable 'link' se refiere a un código geográfico proporcionado por el Instituto Nacional de Estadística y Censos -INDEC- de Argentina)

Para terminar, surgió la pregunta: ¿Cuáles son las localidades que poseen mayor velocidad de internet (100 mbps)? Y esto fue respondido mediante el
siguiente gráfico de barras:

![](https://github.com/hernandroz/telecomunicaciones_project/blob/main/imagenes_readme/top10_local100mbps.png?raw=true)

Todo esto fue lo más importante a remarcar, pero para más detalles puede revisarse el notebook completo del EDA [aquí](https://github.com/hernandroz/telecomunicaciones_project/blob/main/internet_eda.ipynb).

### 2. Establecimiento de KPIs

 - **Por cada provincia, la variación porcentual del acceso a internet de cada 100 hogares, de un trimestre respecto al siguiente trimestre**: Usando la información (de cada provincia) sobre la
   cantidad de accesos a internet por cada 100 hogares, de cada trimestre, se puede evaluar si dicho número aumentó o disminuyó al pasar de un trimestre a otro, usando porcentajes.


   Por ejemplo, supongamos lo siguiente:
   - En el 1er trimestre del 2018, en la provincia San Luis hubo un número de 40.4 conexiones a internet por cada 100 hogares, pero luego de grandes esfuerzos por parte del gobierno argentino,
     al siguiente trimestre ahora había 60.6 conexiones a internet por cada 100 hogares. Entonces hubo un aumento de 50% al pasar de un trimestre a otro (40.4 + 50% 40.4 = 60.6).


    Así que en este caso la medida resultante mediante nuestro KPI sería: +50%
     
- **Variación porcentual de ingresos económicos, de un año respecto a otro**: Referente a las empresas que proporcionaban el acceso a internet a los hogares.
- **Variación porcentual de velocidad de internet, de un año respecto a otro**: En unidades mbps

### 3. Dashboard interactivo

Mediante un dashboard interactivo creado en Power BI se pudo explorar de manera gráfica diversas métricas y observar los objetivos planteados para cada uno de nuestros KPIs:

![](https://github.com/hernandroz/telecomunicaciones_project/blob/main/dashboard/telecom_dashboard_a.png?raw=true)

Se puede acceder al archivo del dashboard interactivo [aquí](https://github.com/hernandroz/telecomunicaciones_project/blob/main/dashboard/telecom_dashboard_a.pbix).

## Contribuciones

Siéntase libre de contribuir con mejoras, correcciones o sugerencias. Si encuentra algún problema, por favor, abra un "Issue" en este repositorio o intente contactarme.

## Licencia

Proyecto desarrollado por Hernán Hernández Rodríguez - Data Scientist
