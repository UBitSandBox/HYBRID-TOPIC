# HYBRID-REST-TOPIC
Here we provide a similarity-based search engine based on approximate k-NN search over document embeddings. k-NN ability and indexing documents along with their vector reprsentation is provided by [**OpenDistro for ElasticSearch**](https://opendistro.github.io/for-elasticsearch/) and document embedding is extrapolated from individual words embeddings obtained from pre-trained and aligned [**FastText**](https://fasttext.cc/docs/en/aligned-vectors.html) dictionaries in french, german, english and italian. Typical use of our solution : recommendation and suggestion based on a reference document or natural language queries.

# Requirements
Python 3 and the following modules should be installed :
- django
- djangorestframework
- spacy (the 4 language models should also be downloaded)
- numpy
- scikit-learn

Also you should have dictionaries with word embeddings  
We used the aligned pre-trained vectors dictionaries from FastText [1, 2]  
You can found them here : https://fasttext.cc/docs/en/aligned-vectors.html

---

#### References for fastText aligned dictionaries 
<a id="1">[1]</a> 
Joulin, A., Bojanowski, P., Mikolov, T., Jégou, H., & Grave, E. (2018). 
Loss in Translation: Learning Bilingual Word Mapping with a Retrieval Criterion. 
In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing.

<a id="2">[2]</a> 
Bojanowski, P., Grave, E., Joulin, A., & Mikolov, T. (2017). 
Enriching Word Vectors with Subword Information.
Transactions of the Association for Computational Linguistics, 5, 135–146.

---

# Installation
...work in progress...
# How to use it ?
...work in progress...
