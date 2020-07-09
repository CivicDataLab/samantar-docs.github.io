Machine Translation
-------------------
-------------------

Introduction
************

Machine translation system converts Documents in Source Language to Documents in Target Language.

Methodology
***********

Background
^^^^^^^^^^

Machine translation is a three step process:

Step 0: Find lots of example source language sentences and corresponding human translations into target language. This is called bilingual parallel corpora or Bitext.

Step 1: Apply a learning algorithm to parallel corpora and build an approximate model of human translation.

Step 2: Apply learned model to new source language text and obtain translations in target language.

* Machine Translation Model

The translation must be semantically adequate, which means that all of the meaning in the source language in the sentence/document should carry over to the target language. So there should be no meaning lost. And the other thing is whatever meaning rendered in the target language, is fluent in that language. So words shouldn't be in some random order.
To appreciate how Machine Translation has evolved through the years, we’ll touch upon a few history aspects of it.

There were three popular approaches before SMT and NMT:

- Rule based - you write a bunch of rules that take specific parts of the source language and translate them to specific parts of the target language.

- Interlingual translations - here we basically take the source language text and you reduce it to language independent formalism and then you generate the target language text from that formalism.

- Transfer Based - So what if we do something in the middle. where we do some bit of analysis and write some sort of rules to transfer from that analytic form to the target language analytic form.

All three approaches no longer exist. Except for Rule Based on a few hybrid systems.

Process
#######

Samoses
^^^^^^^

PCL is a Domain Specific Language to construct non-recurrent software pipelines. We are using PCL to build pipeline for the Statistical Machine Translation.

`Samoses <https://github.com/CivicDataLab/Samoses>`_ provides the pipeline for training and serving machine translation model. One has to just plug the dataset and the rest of the process in building a Machine translation system is taken care by Samoses.

Experiments were carried out with English-Hindi using NYU and IIT-B datasets. Results can be found at http://moses.samantar.in/ .

Summary
#######

A statistical machine translation model is built using Moses. A pipeline to train and serve the Machine translation model has been laid using PCL in Samoses.


Please feel free to write us at ``mailto:info@civicdatalab.in``, if you have any questions or concerns, we are happy to help!
