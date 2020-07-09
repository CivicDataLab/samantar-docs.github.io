Corpus Linguistics
-----------------------
-----------------------

Introduction
************

Corpus linguistics is the study of language as expressed in corpora of "real world" text. We started with analysing language complexity in Budget Speeches (from 1947 till date). Results can be found in the above repository.

Methodology
***********

This section explains the setup and the process.

Setup
#####

The setup for Language Analysis for Budget Speech (LABS) is provided `here <https://github.com/CivicDataLab/labs>`_.

To install `complang` check the setup guide `here <https://github.com/CivicDataLab/complang>`_

Process
#######

LABS was built to analyse the language complexity in Union Budget speeches over the years. It uses `complang`, a python package, that has different linguistic and complex network measures to measure language complexity.


It also comes with the crawler code for scraping budget speeches.

complang
^^^^^^^^

The explaination of each of the measure used is provided in the docstrings of their respective functions (here in the `measures <https://github.com/CivicDataLab/complang/tree/master/measures>`_).

Below are the Vocabulary measures used:

- Type-token ratio
- Guiraud_r Index
- Herdan_c Index
- Dugast_k measure
- Maas_a2 measure
- Dugast_u measure
- Tuldava measure
- Brunet_w measure
- CTTR measure
- Summer_s score
- Sichel_s measure
- Michea_m measure
- Honore_h score
- Herdan_vm measure
- Entropy
- Yule_k measure
- Simpson_d measure
- HDD
- MTLD

Below are the list of Dependency measures used:

- Average dependency distance
- Average closeness centrality
- Average closeness outdegree
- Average dependents per word
- Average longest shortest path
- Average sentence length
- Average length of characters in a sentence
- Average length of syllables in a sentence
- Average punctuations per sentence

Below are the list of Constituent measures used:

- T units
- Complex T units
- Clauses
- Dependent Clauses
- NPS
- VPS
- Coordinate phrases
- Constituents
- Constituents w/o leaves
- Height


Summary
*******

Corpus lingustics was applied to Union budget speeches to analyse the language complexity. The results of the experiments can be found `here <https://github.com/CivicDataLab/LABS/tree/master/experiments>`_ . Complang is being used as a submodule that contains all of the linguistic measures and few of the complex networks measures.


Please feel free to write us at ``mailto:info@civicdatalab.in``, if you have any questions or concerns, we are happy to help!
