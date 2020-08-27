.. MIT News Classify documentation master file, created by
   sphinx-quickstart on Mon Aug 24 19:00:14 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to MIT News Classify's documentation!
=============================================

MIT News Classify is a package containing several natural language processing (NLP) and ML-based models
that have been finetuned on the NYT Annotated Corpus and its predefined news tags.
It was developed in Summer 2020 as a tool for topic classification using NLP with the Tegmark Group at MIT. 
Some of its models have been integrated into the Tegmark Group's other projects, such as `Improve The News
<improvethenews.org>`_.

For a full list of models and their documention, see :ref:`Models <models>`.

.. toctree::
   :maxdepth: 2
   :caption: Get Started
   
   installation
   usage

.. toctree::
   :maxdepth: 2
   :caption: Package Reference
   
   models/tf-idf
   models/tf-idf_bi
   models/doc2vec
   models/gpt2
   models/ensemble

.. toctree::
   :maxdepth: 2
   :caption: More Information
   
   authors
   faq
