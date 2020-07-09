Machine Translation
-------------------
-------------------

Introduction
************

Machine translation system converts Documents in Source Language to Documents in Target Language.

Methodology
***********

It's a three step process:

Step 0: Find lots of example source language sentences and corresponding human translations into target language. This is called bilingual parallel corpora or Bitext.

Step 1: Apply a learning algorithm to parallel corpora and build an approximate model of human translation.

Step 2: Apply learned model to new source language text and obtain translations in target language.


Bilingual Parallel Corpora

Started out with English-Hindi parallel corpora, the NYU and IIT Datasets.


Machine Translation Model

The translation must be semantically adequate, which means that all of the meaning in the source language in the sentence/document should carry over to the target language. So there should be no meaning lost. And the other thing is whatever meaning rendered in the target language, is fluent in that language. So words shouldn't be in some random order.
To appreciate how Machine Translation has evolved through the years, we’ll touch upon a few history aspects of it.
There were three popular approaches before SMT and NMT:

Rule based - you write a bunch of rules that take specific parts of the source language and translate them to specific parts of the target language.
Interlingual translations - here we basically take the source language text and you reduce it to language independent formalism and then you generate the target language text from that formalism.

Transfer Based - So what if we do something in the middle. where we do some bit of analysis and write some sort of rules to transfer from that analytic form to the target language analytic form.

All three approaches no longer exist. Except for Rule Based on a few hybrid systems.

We started with Statistical Machine Translation for English -> Hindi using Moses
We built the pipeline using Pipeline Creation Language (PCL) which is a Domain Specific Language. Samoses
The results of the experiments can be found in this portal here
For more info, check these slides that were used as a part of a knowledge sharing session.

Tech
****

Moses - Written in Python, Perl and a bit of C

MGiza for word alignment - C++

KenLM as Language Model - C++
