# Procesamiento del Lenguaje Natural, con Python

* Autor: Ricardo Moya García, PhD
* Fecha última actualización: 24-11-2021


<hr>

En este proyecto de GitHhub podrás encontrar parte del material que utilizo para impartir las clases de Procesamiento
 de Lenguaje Natural con Python.


El contenido compartido es el siguiente: 


#### Tema 1: Introducción

- [00_Introduccion_NLP.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/00_Introduccion_NLP.ipynb)
- [01_NLTK_Introduccion.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/01_NLTK_Introduccion.ipynb)

#### Tema 2: NLP - Conceptos y Preprocesamiento de texto

* Conceptos: Corpus, Bag of Words (BoW), Tokenización, N-Grammas, Stemming, Lematización, Stop-Words, Parts of 
Speech, Named Entity Recognition (NER)

- [02_NLP_Conceptos_NLTK.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/02_NLP_Conceptos_NLTK.ipynb)
- [03_NLP_Conceptos_spaCy.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/03_NLP_Conceptos_spaCy.ipynb)

* Normalización de textos: Preprocesamiento

- [04_Preprocesamiento_de_textos_Normalizacion.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/04_Preprocesamiento_de_textos_Normalizacion.ipynb)
- [05_Bag_of_Words_BoW.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/05_Bag_of_Words_BoW.ipynb)

#### Tema 3: Analisis Automático de texto subjetivo (Clasificación de textos)

* Introducción: Clasificación de textos con Naive Bayes

- [07_Clasificacion_textos_Naive_Bayes.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/07_Clasificacion_textos_Naive_Bayes.ipynb)
- [08_NLTK_Clasificacion_Textos_Naive_Bayes.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/08_NLTK_Clasificacion_Textos_Naive_Bayes.ipynb)

* Clasificación de textos: Algoritmos de aprendizaje para la clasificación

- [09_Scikit_Clasificacion_Textos.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/09_Scikit_Clasificacion_Textos.ipynb)
- [11_NLTK_Scikit_Clasificacion_Textos.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/11_NLTK_Scikit_Clasificacion_Textos.ipynb)
- [13_PoC_Tendencias_Politicas_Twitter_Generacion_Exportacion_Modelos.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/13_PoC_Tendencias_Politicas_Twitter_Generacion_Exportacion_Modelos.ipynb)
- [14_PoC_Tendencias_Politicas_Twitter_Prediccion.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/14_PoC_Tendencias_Politicas_Twitter_Prediccion.ipynb)

* Clasificación de textos: Redes Neuronales

- [15_Keras_MLP_Clasificacion_Textos.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/15_TensorFlow_Keras_MLP_Clasificacion_Textos.ipynb)
- [16_Keras_MLP_Tendencias_Politicas_Twitter.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/16_TensorFlow_Keras_MLP_Tendencias_Politicas_Twitter.ipynb)
- [17_Keras_LSTM_Tendencias_Politicas_Twitter.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/17_TensorFlow_Keras_LSTM_Tendencias_Politicas_Twitter.ipynb)

#### Tema 4: Topic Modeling (Clustering)

* LSI: Latent Semantic Index

- [18_Topic_Modeling.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/18_Topic_Modeling.ipynb)
- [19_LSI_Ejemplo_Basico_Topic_Modeling.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/19_LSI_Ejemplo_Basico_Topic_Modeling.ipynb)

* LDA: Latent Dirichlet Allocation

- [20_LDA_Ejemplo_Basico_Topic_Modeling.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/20_LDA_Ejemplo_Basico_Topic_Modeling.ipynb)
- [21_Topic_Modeling_noticias.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/21_Topic_Modeling_noticias.ipynb)
- [22_Topic_Modeling_Tweets_Politica.ipynb](https://github.com/RicardoMoya/NLP_with_Python/blob/master/22_Topic_Modeling_Tweets_Politica.ipynb)


<hr>


## Instalación del entorno

Para ejecutar los scripts y notebooks de este proyecto es necesario tener creado un entorno virtual con conda 
(también puede ser con un virtualenv), en el que a parte de tener instaladas las librerías que te instala anaconda 
por defecto al crear el entorno (numpy, scipy, pandas, matplotlib, scikit, etc) hay que instalar una serie de 
librerías específicas que se indican en el fichero requirements.txt.

A continuación se muestran los pasos a seguir para crear el entorno virtual con conda por medio de una consola:

`Nota: estos mismos pasos pueden realizarse también por medio del Anaconda Navigator.`

<hr>

## Instalación Entorno Virtual Conda - DeepLearning

* Pasos para la creación de un Virtualenv con conda e instalación de las librerías necesarias

1.- Creación del entorno virtual "*Python37_NLP*" con un python 3.7
```
>> conda create -n Python37_NLP python=3.7 anaconda
```

2.- Activar el entorno virtual

```
>> conda activate Python37_NLP
```

3.- Instalar librerías especificadas en el fichero requirements.txt:

```
>> pip install -r requirements.txt
```

* En caso de tener algún problema con la instalación de alguna de las librerías, proceder a instalar la librería 
  manualmente de la siguiente manera:
  
```
>> pip install nombre_libreria==VERSION
```
  

#### Bonus Track Anaconda

A continuación se muestran algunas acciones extra:

1.- Desinstalar librerías con conda y pip respectivamente:
```
>> pip uninstall nombre_libreria
```
2.- Desactivar el entorno virtual (previamente tiene que estar activado)
```
>> conda deactivate
```
3.- Eliminar entorno virtual (llamado "Python37_NLP")
```
>> conda remove -n Python37_NLP -all
```
