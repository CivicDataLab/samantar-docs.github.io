Text Annotation Platform
------------------------
------------------------

Introduction
************

Text annotation is performed to convert raw text data to its structured form. The annotation platform is called `Cheyyali <https://cheyyali.samantar.in/>`_.

The platform allows users to label data and provides annotation features for sequence labeling, text classification and sequence-to-sequence tasks. The platform is built specifically for teams to work collaboratively, by having different workflows and moderation layers.

The platform has an optimised interface, by providing --

* Keyboard Shortcuts
* Full Unicode Support
* Support for Subword and phrase annotations

Cheyyali is currently been used to annotate entities and relations in Indian Court judgements as part of a collaboration with HAQ.

Methodology
***********

Tech
****

Cheyyali is a fork of `Doccano <https://github.com/doccano/doccano>`_.

To interpret legal documents and have it in a format that's consumable by Cheyyali, `lglint <https://github.com/CivicDataLab/lglint>`_ was created. lglint is written in Python.
