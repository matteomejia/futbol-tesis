# Definición de un conjunto de datos óptimo para la predicción de resultados de partidos de fútbol

## Introducción

Este repositorio contiene los archivos necesarios para reproducir los resultados obtenidos por la tesis de (Francisco Mejía, 2022). Los datos utilizados en este experimento provienen de la base de datos recopilada por [Hugo Mathien](https://www.kaggle.com/datasets/hugomathien/soccer).

## Requisitos

Para poder ejecutar el código contenido en este repositorio es necesario instalar las siguientes dependencias:

* Python 3 (versión >=3.8,<3.12)
* [Poetry](https://python-poetry.org/)

Las siguientes librerías fueron utilizadas en el desarrollo del proyecto:

* Numpy
* Pandas
* Seaborn
* Matplotlib
* Scikit-learn

Las librerías se pueden instalar con el comando ```poetry install```.

## Contenido

En este repositorio se encuentran los siguientes archivos:

* Carpeta **data**: incluye los archivos .csv de diferentes puntos en la experimentación.
* Carpeta **datasets**: incluye los cinco datasets candidatos utilizados en la experimentación.
* Carpeta **notebooks**: incluye los Jupyter notebooks donde se codificó el proceso de experimentación.

Por cuestión de tamaño, la base de datos original no fue incluida en el repositorio. El archivo ```dataset_initial.csv``` incluye los datos iniciales ya extraídos y procesados de la base de datos.

## Uso

Para reproducir los resultados obtenidos en la tesis basta con ejecutar el código de los siguientes notebooks en orden:

1. **preprocess.ipynb**: genera el dataset inicial a partir de los datos de la fuente y los guarda en el archivo ```dataset_initial.csv```. El repositorio ya cuenta con este archivo.
2. **discretize.ipynb**: discretiza los datos de ```dataset_initial.csv``` que no hayan sido previamente procesados y los guarda en el archivo ```dataset_encoded.csv```. El repositorio ya cuenta con este archivo.
3. **generate_candidates.ipynb**: toma los datos de ```dataset_encoded.csv``` y genera los cinco datasets candidatos de la carpeta **datasets**. El repositorio ya cuenta con estos archivos.
4. **experiments.ipynb**: utiliza los datasets generados para realizar el entrenamiento y la validación de resultados con las técnicas de predicción seleccionadas. La imágenes se pueden obtener de este notebook.