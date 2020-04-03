# Procesamiento del Lenguaje Natural, con Python

* Autor: Ricardo Moya García, PhD
* Fecha última actualización: 03-04-2020


<hr>

En este proyecto de GitHhub podrás encontrar parte del material que utilizo para impartir las clases de Procesamiento
 de Lenguaje Natural con Python.


El contenido compartido es el siguiente: 


#### Tema 1: Introducción

    * Notebooks:
        - 00_Introduccion_NLP.ipynb
        - 01_NLTK_Introduccion.ipynb

#### Tema 2: NLP - Conceptos y Preprocesamiento de texto

* Conceptos: Corpus, Bag of Words (BoW), Tokenización, N-Grammas, Stemming, Lematización, Stop-Words, Parts of 
Speech, Named Entity Recognition (NER)


    * Notebooks:
        - 02_NLP_Conceptos_NLTK.ipyn
        - 03_NLP_Conceptos_spaCy.ipynb

* Normalización de textos: Preprocesamiento


        * Notebooks:
            - 04_Preprocesamiento_de_textos_Normalizacion.ipynb
            - 05_Bag_of_Words_BoW.ipynb


#### Tema 3: Analisis Automático de texto subjetivo (Clasificación de textos)

* Introducción: Clasificación de textos con Naive Bayes


        * Notebooks:
            - 07_Clasificacion_textos_Naive_Bayes.ipynb
            - 08_NLTK_Clasificacion_Textos_Naive_Bayes.ipynb

* Clasificación de textos: Algoritmos de aprendizaje para la clasificación


        * Notebooks:
            - 09_Scikit_Clasificacion_Textos.ipynb
            - 11_NLTK_Scikit_Clasificacion_Textos.ipynb
            - 13_PoC_Tendencias_Politicas_Twitter_Generacion_Exportacion_Modelos.ipynb
            - 14_PoC_Tendencias_Politicas_Twitter_Prediccion.ipynb

* Clasificación de textos: Redes Neuronales


        * Notebooks:
            - 15_Keras_MLP_Clasificacion_Textos.ipynb
            - 16_Keras_MLP_Tendencias_Politicas_Twitter.ipynb
            - 17_Keras_LSTM_Tendencias_Politicas_Twitter.ipynb

#### Tema 4: Topic Modeling (Clustering)

* LSI: Latent Semantic Index


        * Notebooks:
            - 18_Topic_Modeling.ipynb
            - 19_LSI_Ejemplo_Basico_Topic_Modeling.ipynb

* LDA: Latent Dirichlet Allocation


        * Notebooks:
            - 20_LDA_Ejemplo_Basico_Topic_Modeling.ipynb
            - 21_Topic_Modeling_noticias.ipynb
            - 22_Topic_Modeling_Tweets_Politica.ipynb


<hr>


## Instalación del entorno

Para ejecutar los scripts y notebooks de este proyecto es necesario tener creado un entorno virtual con conda 
(también puede ser con un virtualenv), en el que a parte de tener instaladas las librerías que te instala anaconda 
por defecto al crear el entorno (numpy, scipy, pandas, matplotlib, scikit, etc) hay que instalar una serie de 
librerías específicas que se indican en el fichero requirements.txt.

A continuación se muestran los pasos a seguir para crear el entorno virtual con conda por medio de una consola:

`Nota: estos mismos pasos pueden realizarse también por medio del Anaconda Navigator.`

1.- Crear un entorno virtual con un python 3.6 llamado "python36_NLP"

```
>> conda create -n python36_NLP python=3.6 anaconda
```
2.- Activar el entorno virtual

En primer lugar podemos listar todos los entornos que tenemos con:
```
>> conda env list
```
Luego activamos el entorno de la siguiente manera
```
>> conda activate python36_NLP
```
3.- Instalar librerias (con conda):

Para instalar las librerias de forma manual podemos hacerlo:
```
>> conda install -n python36_NLP nombre_libreria==VERSION
```
O también (en caso de que esa librería no este en el repositorio de conda) lo podemos hacer con pip de la siguiente 
manera, teniendo activado el entorno virtual:
```
>> pip install nombre_libreria==VERSION
```
Por ejemplo para instalar la librería de NLTK lo podríamos hacer de alguna de estas 2 formas:
```
>> conda install -n python36_NLP NLTK==3.4.0
Ó
>> pip install -n NLTK==3.4.0
```
Como instalar las librerías de 1 en 1 es un "rollo", podemos instalar todas las librerías que tengamos definidas en 
un fichero de "requirements.txt" de la siguiente manera (solo para Linux o MAC):
```
>> conda install --yes --file requirements.txt
```
De esta manera instala todas las librerías (con sus correspondientes versiones) que hay en cada una de las lineas del
 fichero.
 
Esta manera de intalar esta librerías tiene un inconveniente y es que si una de esas librería no esta disponible en 
el repositorio de conda no la instala y da un error. Para ello podemos realizar la instalación de la siguiente 
manera; haciendo que, si no esta la librería disponible en la paquetería de conda lo instale con pip (esto es válido 
solo para sistemas Linux o MAC):
```
>> while read requirement; do conda install --yes $requirement || pip install $requirement; done < requirements.txt
```

Para hacer esto mismo en sistemas Windows hay que hacerlo de la siguiente manera:
```
>> FOR /F "delims=~" %f in (requirements.txt) DO conda install --yes "%f" || pip install "%f"
```
`Nota: no aseguro 100% que este último comando funcione para todas las versiones de windows`

#### Bonus Track Anaconda

A continuación se muestran algunas acciones extra:

1.- Desinstalar librerías con conda y pip respectivamente:
```
>> conda uninstall -n python36_NLP nombre_libreria
>> pip uninstall nombre_libreria
```
2.- Desactivar el entorno virtual (previamente tiene que estar activado)
```
>> conda deactivate
```
3.- Eliminar entorno virtual (llamado "python36_NLP")
```
>> conda remove -n python36_NLP -all
```