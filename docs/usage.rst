========
Usage
========

There are several models released in the package, including TF-IDF, TF-IDF bigrams, 
GPT-2, and more to come soon. 

To use one of the models to classify a piece of text, simply import it::

	from mitnewsclassify import tfidf
    from mitnewsclassify import tfidf_bi
    from mitnewsclassify import gpt2

From there we can get the hidden features or the a set of classified tags
for a piece of text we provide it. 

To get the hidden features from TF-IDF, for example::
    text = "This is a sample piece of text."
    features = tfidf.getfeatures(text)

To get the classified tags from TF-IDF::
    text = "This is a sample piece of text."
    tags = tfidf.gettags(text)

