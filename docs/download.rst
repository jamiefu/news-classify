========
Download
========

The Download class is a supplement to all the models, and is intrinsically called upon by each model if the model files have not been downloaded onto the user's storage. Should there be any problems during the intrinsic calls, the user can call the download class explicitly to get the same desired outcome.

gettags
-----------------

*class* mitnewsclassify.download.download(model=None)

Downloads the model files for a given model.

**Parameters**
    * model (``string``) - The model to be downloaded onto the user's storage. 
    * Default value is None and all models will be downloaded. 
    * Use ``tfidf`` for the TF-IDF model, ``tfidf_bi`` for the TF-IDF Bigrams model, 
      ``doc2vec`` for the Doc2Vec model, ``gpt2`` for the GPT2 model, 
      ``distilbert`` for the DistilBERT model, ``ensemble`` for the Ensemble model, 
      ``trisemble`` for the trisemble model and ``quadsemble`` for the quadsemble model.

**Example**

.. code-block:: python

    >>> from mitnewsclassify import download

    >>> download.download('tfidf')