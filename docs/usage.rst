========
Usage
========

There are several models released in the package, including TF-IDF, TF-IDF bigrams, doc2vec, 
GPT-2, and a heavyweight ensemble model that uses all four of these models. 

To use one of the models to classify a piece of text, simply import it:

.. code-block:: python

    from mitnewsclassify import tfidf
    from mitnewsclassify import tfidf_bi
    from mitnewsclassify import doc2vec
    from mitnewsclassify import gpt2

From there we can get the a set of classified tags for a piece of text we provide it. 
The functions ``gettags`` and ``getfeatures`` exist for each of the models in this package. 

To get the classified tags from TF-IDF:

.. code-block:: python

    text = "This is a sample piece of text."
    tags = tfidf.gettags(text)

If you are interested in using these models for your own further finetuning
or modeling, you can also obtain the hidden features, as shown below with TF-IDF:

.. code-block:: python

    text = "This is a sample piece of text."
    features = tfidf.getfeatures(text)