# HYBRID-REST-TOPIC

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/c22e79c94f3749deaf16c6ed705affe2)](https://app.codacy.com/gh/UBitSandBox/HYBRID-REST-TOPIC?utm_source=github.com&utm_medium=referral&utm_content=UBitSandBox/HYBRID-REST-TOPIC&utm_campaign=Badge_Grade_Dashboard)

Here we provide a similarity-based search engine based on approximate k-NN search over document embeddings. k-NN ability and indexing documents along with their vector reprsentation is provided by [**OpenDistro for ElasticSearch**](https://opendistro.github.io/for-elasticsearch/) and document embedding is using the [**Universal Sentence Encoder - multilingual**](https://tfhub.dev/google/universal-sentence-encoder-multilingual/3) model. 
The process of generating vector representations of documents is handled by a simple REST API built with the [**Django REST framework**](https://www.django-rest-framework.org/)  
Typical use-case of our solution : recommendation and suggestion based on a reference document or natural language queries.

This REST API is to use with [this Index Manager](https://github.com/Shiaroku/HYBRID-REST-TOPIC-INDEX-MANAGER)  

# Requirements
Python 3.x and the following modules should be installed :
- django
- djangorestframework
- spacy
  - *xx_use_md* from [spacy-universal-sentence-encoder-tfhub](https://spacy.io/universe/project/spacy-universal-sentence-encoder)  
`pip install https://github.com/MartinoMensio/spacy-universal-sentence-encoder-tfhub/releases/download/xx_use_md-0.2.3/xx_use_md-0.2.3.tar.gz#xx_use_md-0.2.3`
- numpy
- scikit-learn

---

# Installation

## Install required modules
On a Terminal type the following command:

<pre>
pip install django
pip install djangorestframework
pip install djangorestframework-simplejwt
pip install spacy
pip install https://github.com/MartinoMensio/spacy-universal-sentence-encoder-tfhub/releases/download/xx_use_md-0.2.3/xx_use_md-0.2.3.tar.gz#xx_use_md-0.2.3
pip install numpy
pip install scikit-learn
pip install python-dotenv
</pre>

## Configuration (PyCharm)
Open the Run/Debug Configurations editor ans create a new Python configuration according to the following:

| Parameter          |      Value                                     |
|--------------------|------------------------------------------------|
| Script path        | ...../HYBRID-REST-TOPIC/vectoREST/manage.py    |
| Parameters         | runserver                                      |
| Python interpreter | Choose the last version of Python3             |
| Working directory  | ...../HYBRID-REST-TOPIC/vectoREST              |

## Configuration
At the root of the project, create a file .env and copy the environment variables from the .env.example file.

Fill the environment variables with the appropriate values.

## Run server

### In Terminal : 
<pre>
python3 /vectoREST/manage.py runserver
</pre>

### In PyCharm
Just click on the Run button


# How to use it ?

Valid keywords for the 'method' argument in the config are :

### Not using clustering

- 'None'
- 'weighted'

### Using clustering

- 'spectral'
- 'k-means'
- 'agglomerative'

If using clustering, 'n_clusters' should be given as an integer corresponding to the number of clusters to identify, I recommend you keep it under 5.
Remember that if using clusters, **you should provide documents at least n_clusters sentences long.**


[See the POST/GET requests documentation for Authentification, Configuration, Vector generation ...](https://documenter.getpostman.com/view/5913280/T17JAnWN)
