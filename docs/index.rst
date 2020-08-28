.. MIT News Classify documentation master file, created by
   sphinx-quickstart on Mon Aug 24 19:00:14 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to MIT News Classify's documentation!
=============================================

MIT News Classify is a package containing several natural language processing (NLP) and ML-based models
that have been finetuned on the NYT Annotated Corpus and its predefined news tags.
It was developed in Summer 2020 as a topic classification tool using NLP with the Tegmark Group at MIT. 
Some of its models have been integrated into the Tegmark Group's other projects, such as `Improve The News
<improvethenews.org>`_. We have now released it as a package for public use, to aid you in all of your 
news classification needs!

See Installation and Usage to get started! 
For a full list of models and their documention, see the documentation under Package Reference.

.. toctree::
   :maxdepth: 2
   :caption: Quickstart
   
   installation
   usage

.. toctree::
   :maxdepth: 1
   :caption: The Good Stuff
   
   models/quadsemble
   models/trisemble
   models/ensemble

.. toctree::
   :maxdepth: 1
   :caption: Other Models & Package Reference

   models/tf-idf
   models/tf-idf_bi
   models/doc2vec
   models/gpt2
   models/distilbert
   
   download
   aliases

.. toctree::
   :maxdepth: 1
   :caption: More Information
   
   authors
   faq
