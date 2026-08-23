================================================================================
ANÁLISIS EXPLORATORIO DE DATOS DE DATASET
"weekly_route_operations.csv"
=============================

DESCRIPCIÓN

Este proyecto corresponde al desarrollo de un Análisis Exploratorio de Datos aplicado al dataset "weekly_route_operations.csv", el cual contiene información relacionada con operaciones logísticas y transporte marítimo. El análisis contempla la exploración de variables, evaluación de la calidad de los datos, identificación de valores atípicos, análisis de correlación y preparación del conjunto de datos para etapas posteriores de modelamiento.

CARACTERÍSTICAS PRINCIPALES

* Análisis exploratorio de variables numéricas y categóricas.
* Evaluación de la calidad del conjunto de datos mediante detección de valores faltantes y datos atípicos.
* Análisis de correlación entre la variable objetivo y las variables predictoras mediante el coeficiente de correlación de Pearson.

REQUISITOS PREVIOS / DEPENDENCIAS

Para ejecutar correctamente el proyecto se requiere:

* R versión 4.6 o superior.
* RStudio.
* Archivo de datos: weekly_route_operations.csv.
* Librerías utilizadas:

  * tidyverse
  * visdat
  * dlookr
  * flextable
  * qqplotr
  * ggpmisc
  * VIM
  * mice
  * gridExtra
  * corrplot
  * factoextra
  * dplyr
  * Hmisc
  * ggplot2
  * tidyr
  * moments
  * gt

INSTALACIÓN Y CONFIGURACIÓN

1. Instalar R y RStudio.
2. Copiar el archivo "weekly_route_operations.csv" en el directorio de trabajo del proyecto.
3. Instalar las librerías requeridas mediante install.packages().
4. Ejecutar el script de análisis en RStudio siguiendo el orden de las secciones desarrolladas.

INSTRUCCIONES DE USO

1. Abrir el proyecto en RStudio.
2. Ejecutar las instrucciones correspondientes a la carga de librerías.
3. Importar el archivo "weekly_route_operations.csv".
4. Ejecutar secuencialmente cada bloque de código correspondiente al análisis exploratorio.
5. Los gráficos y tablas generados serán almacenados automáticamente en el directorio de trabajo para su posterior incorporación al informe y a la presentación.

ESTRUCTURA DE ARCHIVOS

weekly_route_operations.csv
Conjunto de datos utilizado para el análisis.

Script de análisis (.R / .Rmd)
Contiene el código utilizado para realizar el análisis exploratorio de datos.

Presentación PowerPoint
Presentación utilizada para exponer los principales resultados del análisis.

METODOLOGÍA

El análisis se desarrolló siguiendo las etapas de un proceso de Exploratory Data Analysis (EDA):

* Carga e inspección inicial del conjunto de datos.
* Identificación del tipo de cada variable.
* Obtención de estadísticas descriptivas.
* Análisis gráfico de variables categóricas y numéricas.
* Evaluación de normalidad mediante gráficos y pruebas estadísticas.
* Identificación de valores atípicos utilizando diagramas de caja y el criterio del rango intercuartílico (IQR).
* Evaluación de la existencia de datos faltantes mediante funciones de diagnóstico y visualización.
* Construcción de una matriz de correlación utilizando el coeficiente de Pearson y evaluación de la significancia estadística mediante valores p.
* Interpretación de los resultados para preparar el conjunto de datos para futuros modelos de minería de datos.

AUTORES Y CRÉDITOS

Trabajo desarrollado por el equipo del curso de Minería de Datos.

Integrantes:

* Camila Rodríguez 
* Macarena Caballero
* Roberto Castillo
* Sebastián Gahona
* Daniel Cáceres


Docente:

* Claudia Pérez

Institución:

* Universidad Andrés Bello

LICENCIA Y DERECHOS DE USO

Este proyecto fue desarrollado con fines exclusivamente académicos para la asignatura de Minería de Datos. El conjunto de datos y el código fuente se utilizarán únicamente con propósitos educativos y de evaluación.
