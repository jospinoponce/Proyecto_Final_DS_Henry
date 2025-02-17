# <h1>Pj_05-003 Desarrollo de un MVP para evaluar la viabilidad de la incorporación de vehículos eléctricos en el servicio de taxis en la ciudad de Nueva York. </h1> 

## **HENRY BOOTCAMP | Proyecto Final**
<hr>

*El presente proyecto se desarrolla como el proyecto final del Bootcamp de Data Science de [Soy Henry](https://www.soyhenry.com/). Busca analizar la situación del mercado de taxis en New York a través del MVP de una aplicación web.  https://www.youtube.com/watch?v=ewDlLPiMFlo&feature=youtu.be*  

# 1. Introducción

Se lleva a cabo un análisis del sector de transporte público en los taxis amarillos de la ciudad de Nueva York con el fin de evaluar la viabilidad de invertir en tecnologías sostenibles como la implementación de flotas de vehículos eléctricos. Se analizan datos en NYC de los sonidos registrados por el tráfico, la contaminación en el aire, el movimiento de vehículos por zona y los viajes que realizan los taxis en la ciudad para  los 5 Boroughs (distritos) de New York: **Manhattan, Brooklyn, Queens, The Bronx & Staten Island**.<br>

Se integra un modelo de Machine Learning  para estimar tendencias a futuro de los principales indicadores,  un Dashboard para la visualización de los datos y resultados obtenidos en una aplicación en Streamlit denominada [Dataxi](https://lucianolarrea-pf-ds-home-f5yrsh.streamlit.app/). <br>

El proyecto se ejecuta bajo metodología ágil Scrum y se desarrolla en cuatro etapas.<br>
**Etapa 1:** Recopilación de los datos, **Etapa 2:** Creación de base de datos, **Etapa 3:** Análisis Económico, KPIs y **Etapa 4:** Modelo ML. <br>

La gestión del proyecto se desarrolla en:<br>
*Actividades [Task:](https://trello.com/b/BBq6OTiJ/proyecto-final) Cronograma [Gant:](https://docs.google.com/spreadsheets/d/10gupD91IRV9KfblHfoy6fAw1rV6vu_gw6LNHp0itnfo/edit#gid=1709744959)*

<hr>

# 2. Objetivos

- Identificar patrones y tendencias en los movimientos de taxis en NYC (2010-2022).<br>
- Investigar la relación entre el movimiento de los taxis y la calidad del aire y la contaminación sonora en NYC, para determinar alguna  correlación existente. <br>
- Realizar un análisis de las ganancias económicas del sector. <br>
- Desarrollar un Modelo de ML para estimar comportamientos futuros del sector de transporte de taxi en NYC.<br>

<hr>

# 3. Desarrollo

<img src="src/esquema.png" />

## 3.1 Recursos implementados

- **Gestión del proyecto:** Google meet, Trello.<br>
- **EDA, ETL, SQL BD:** Python, Beautiful Soup, Pandas, Matplotlib,  Seaborn, PySpark, SQLAlchemy , Azure SQL.<br> 
- **Business Intelligence & Machine Learning:** SQLAlchemy, Plotly, PowerBI, Scikit-learn, Streamlit.<br> 
- **Cloud:** Azure (Azure Data Factory, Azure Blob Storage, Azure Synapse Analytics) <br>

## 3.2 Obtencción de los Datos

Los datos se extraen de fuentes oficiales que proporciona  New York.  [**Taxi & Limousine Commission**](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) y de los datos abiertos de la ciudad [**Open_Data_NYC**](https://data.cityofnewyork.us/).<br> 

*El **Diccionario de los datos** puede consultarse en [data_dict](https://github.com/jospinoponce/Proyecto_Final_DS_Henry/blob/main/data_dict.md).*

<hr>

# 4. ETL/EDA

Se desarrolla un sistema que extrae datos de manera automática de [**Taxi & Limousine Commission**](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) los transforma y los carga por medio de un pipeline a una base de datos SQL en la nube de Azure.<br>

Al realizar el análisis exploratorio de los datos, se determina que:

- La crisis covid-19 afectó las actividades del sector en 2020.
- La facturación promedio por día y por vehiculo ha disminuido.
- Las zonas donde el precio (USD) de los viajes es más costoso son el aeropuerto EWR y Staten island. 
- Los sectores que más viajes registran son el aeropuerto EWR y Manhattan.
- El borough con la peor calidad de aire, mayor contaminación por ruido y mayor volumen de tráfico vehicular es Manhattan. 

 *Los aspectos más importantes de este proceso se pueden consultar en: [ETL](https://github.com/jospinoponce/Proyecto_Final_DS_Henry/tree/main/1.ETL) y el [EDA](https://github.com/jospinoponce/Proyecto_Final_DS_Henry/tree/main/2.EDA).*<br>

<hr>

# 5. Resultados

Se genera un informe de los impactos ambientales positivos que lleva la implementación de determinada cantidad de vehículos eléctricos para la ciudad.
[4.REPORTS](/4.REPORTS). <br>

En el presente video muestra el resultado final del proyecto [Resultado Final](https://youtu.be/ewDlLPiMFlo).

## 5.1 KPIs 

-  Porcentaje de la cantidad de viajes proyectada.<br>
-  Porcentaje de la cuota del mercado proyectado.<br>
-  Ingresos brutos por día/mes.<br>
-  Porcentaje de disminución de contaminante (PM 2,5) en el aire por implementar vehículos eléctricos.<br>
-  Reducción porcentual de contaminación acústica por implementar vehículos eléctricos. <br>

## 5.2 Modelo Machine Learning 

Se desarrolla un modelo de forecasting para establecer proyecciones de las tendencias y patrones que presenta el sector de taxis con la data histórica extraída. El modelo ML puede ser consultado en [3.ML](/3.ML). 

Se genera un análisis económico con las proyecciones realizadas al sector y puede consultarse en: [4.REPORTS](/4.REPORTS). <br>

## 5.3 App

Se desarrolla un MVP para una app que contiene tanto el modelo ML como un dashboard de visualización de datos en Power Bi embebidos para generar métricas y los KPIs establecidos en función al número de vehículos eléctricos que el usuario seleccione.<br>

El nombre de la app es **Dataxi** y puede ser consultada en: [Dataxi](https://lucianolarrea-pf-ds-home-f5yrsh.streamlit.app/)<br>

<img src="src/portada_1.gif" />

**Dataxi** le genera al usuario un .pdf descargable con el resumen de las metricas generadas y algunas recomendaciones de inversión que pueden incrementar el rendimiento del capital invertido en un 32%. 

<img src="src/pdf.png" width="350" height="160"/>

Se puede visualizar un ejemplo de este reporte con la implementación de una flota de 1000 taxis eléctricos en:[1000_taxis.pdf](/4.REPORTS/3.Informe_Final.pdf) 

<hr>

# 6. Conclusiones

El sector de taxis amarillos viene en decrecimiento pre-COVID. La recuperación post-COVID mostró indicadores al alza, pero algunos volvieron a caer debido a la expansión de servcios como Uber. Sin cambios fundamentales, se pronostica una posible crisis  del mercado de taxis para mediados de 2024. Invertir en el mercado a la baja puede ser riesgoso pero ofrece oportunidades para destacarse en servicio, sustentabilidad e innovación teniendo cuenta el impacto ambiental positivo que generan los vehículos eléctricos.



<hr>

*Developed by*

<a href="https://www.linkedin.com/in/franco-jonas-myburg-6095b8255/"><img alt="Franco" title="Connect with Franco" src="https://img.shields.io/badge/Franco Myburg-0077B5?style=flat&logo=Linkedin&logoColor=white"></a> **DATA ENGINEER**

<a href="https://www.linkedin.com/in/ivannagvdc/"><img alt="Ivanna" title="Connect with Ivanna" src="https://img.shields.io/badge/Ivanna Villa-0077B5?style=flat&logo=Linkedin&logoColor=white"></a> **DATA ANALYST**

<a href="https://www.linkedin.com/in/jospinoponce/"><img alt="Jaime" title="Connect with Jaime" src="https://img.shields.io/badge/Jaime Ospino-0077B5?style=flat&logo=Linkedin&logoColor=white"></a> **DATA ENGINEER**

<a href="https://www.linkedin.com/in/takticflow/"><img alt="Luciano" title="Connect with Luciano" src="https://img.shields.io/badge/Luciano Larrea-0077B5?style=flat&logo=Linkedin&logoColor=white"></a> **PROJECT MANAGER & DATA SCIENTIST**

<a href="https://www.linkedin.com/in/royquillca/"><img alt="Roy" title="Connect with Roy" src="https://img.shields.io/badge/Roy Quillca-0077B5?style=flat&logo=Linkedin&logoColor=white"></a> **DATA ENGINEER**




