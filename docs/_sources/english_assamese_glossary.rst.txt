English and Assamese Glossary
-----------------------------
-----------------------------

Introduction
************

The web portals that hosts the Administrative glossary terms in English and Assamese were built as a part of the collobaration with the Assam State Finance Department.

The portals can be accessed through the below links:


- `English to Assamese Glossary <http://13.234.34.21:8082/i6aygim2/>`_

- `Assamese to English Glossary`


We took the physical copy of the Administrative glossary and scanned it into a digital document. Performed a few image processing tasks to clean up the document and parsed it using Optical Character Recognition(OCR). Using the resultant machine readable document, a portal was built.

Methodology
***********

This section explains the setup and process.

Setup
#####

The dictionary is a fork of `Lexonomy <https://github.com/CivicDataLab/lexonomy>`_. Written in Python and Javascript.


Process
#######

The physical copy of the English-Assamese Administrative terms glossary, that consists of more than 10,000 terms, was digitized using the standard scanner. The glossary consists of words or group of words that are commonly used in public administrative documents.

The scanned version of the glossary can be found `here <https://drive.google.com/file/d/1BiQQwnyMI_DZPQHmu6y60OsMP0eOQSw5/view?usp=sharing>`_ in the PDF format.

Few image processing techniques are used to clean the above document. Optical Character Recognition is performed on the cleaned document, for extracting Assamese and English characters.

The machine readable corresponding English and Assamese word(s) are fed into the dictionary portal.

Platform Usage
^^^^^^^^^^^^^^

- Using the glossary portal is quite straight forward and one has to search for the word or group of words in the search box.
- The search result leads to the corresponding term(s) in the target language.
- Alongside, a list of words ordered alphabetically will appear on the sidebar. More so, like a digital mimic of a physical dictionary.
- The glossary can be edited by the admin of the portal. It provides a easy to use interface for adding or editing words.

Summary
*******

The physical copy of the `English-Assamese Administrative Terms` was digitized. The digitized document was converted to machine readable format using Optical Character Recognition (OCR), that recognizes both English and Assamese characters. To make the document more accessible, and easy-to-use, a web portal was built.



Please feel free to write us at ``mailto:info@civicdatalab.in``, if you have any questions or concerns, we are happy to help!
