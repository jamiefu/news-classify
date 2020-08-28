========
Usage
========

The best model for topic classification is the quadsemble model, which incorporates a combination of 
the TF-IDF, TF-IDF Bigrams, distilBERT, and Doc2Vec embeddings. 

To use one it to classify a piece of text, simply do the following: 

.. code-block:: python

    >>> from mitnewsclassify import quadsemble

    >>> quadsemble.gettags("Republicans proceeded with the third night of their national convention, but many Americans — particularly those in the path of Hurricane Laura — were focused on more immediate concerns.")
    ['elections', 'presidents and presidency (us)', 'presidential elections (us)', 'hurricanes and tropical storms', 'presidential election of 2004']
    
If you are interested in using these models for your own further finetuning
or modeling, you can individually access the model features through ``getfeatures`` on the 
TF-IDF, TF-IDF Bigrams, Doc2Vec, GPT-2, and distilBERT models. 