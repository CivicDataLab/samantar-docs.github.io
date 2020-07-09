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
* Label Stats and User Stats

Cheyyali is currently been used to annotate entities and relations in indian court judgements as part of a collaboration with HAQ.

Methodology
***********

This section explains the setup and process.

Setup
#####

Cheyyali is a fork of `Doccano <https://github.com/doccano/doccano>`_. Installation and running guide is provided `here <https://github.com/CivicDataLab/cheyyali>`_.

This is hosted in https://cheyyali.samantar.in

Process
#######

The document uploaded to Cheyyali is first converted to its machine readable form. This is followed by preprocessing and then converted to the format that Cheyyali supports. The output - annotated text is in the ``JSON format``.


lglint
^^^^^^


This is a python package that has the scripts to perform the above process. The installation and running guide is provided `here <https://github.com/CivicDataLab/lglint>`_.

Plugging in an example pipeline::

     pipeline \
    .add(GetCNRFromPdf(data_dir=all_judgements_pdf_directory,
                       file_format="pdf",
                       cnr_pattern=r".* - (.*)\.pdf")) \
    .add(LoadMetaData(base_data_dir=settings.base_data_dir,
                      metadata=settings.combined_metadata_file)) \
    .add(FilterMetaDataByCNR(cnr_list=[])) \
    .add(Pdf2Txt(all_judgements_pdf_directory, all_judgements_txt_directory)) \
    .add(AddTitleGeoCNRToFirstLine(input_dir=all_judgements_txt_directory,
                                   pattern=r'.* - (.*)\.txt',
                                   use_cnr=True)) \
    .add(ConvertToCheyyaliFormat(input_dir=all_judgements_txt_directory,
                                 out_file=settings.final_cheyyali_judgements,
                                 pattern=r'.* - (.*)\.txt',
                                 use_cnr=True))

     pipeline.execute()


From the above example, ``GetCNRFromPdf``, ``LoadMetaData``, ``FilterMetaDataByCNR`` are preprocessing functions. Once the preprocessing is done, the PDF is converted to a text file using ``Pdf2Txt`` and some post-processing has been performed on the machine readable file using ``AddTitleGeoCNRToFirstLine``. The then data is transformed into cheyyali's format using ``ConvertToCheyyaliFormat`` function.


Similar to the above example, custom pipelines can be made with custom independent functions. This modularity in the workflow makes lglint scalable.

If you are facing any difficulty, please raise an issue at https://github.com/CivicDataLab/lglint/issues


Platform Usage
^^^^^^^^^^^^^^

- Once you login to the platform using the above link, you can see the list of projects that you are part of and can also create projects of your own.

- Cheyyali has moderation layers, namely - the project admin, the annotator and the annotation approver. Project admin is the creator of the project; they can create teams, invite people to the team, annotate and also approve the annotations. The annotator can only annotate the free text. The annotation approver is the person who approves the annotations.

- The annotated text becomes valid only when it's approved by the annotation approver.

- When the user gets inside a project, they can see or create the required entities/tags. Each entity can also be assigned a keyboard shortcut key (hotkeys).

- Drag along the words(or subwords or group of words) and assign tags by either selecting from the given tags or by the hotkeys.

 The User and Label stats can be viewed in the ``Statistics`` section.

- One can write Annotation Guidelines for each of the project. This helps other collaborators to get along with the prescribed standard.


Summary
*******

Cheyyali is a text annotation platform that can be used for Sequence Labeling, Sequence-to-Sequence and Text Classification tasks. This means to say that while preparing datasets for Entity Recognition, Machine Translation, and so on. Cheyyali is optimised for teams to collaboratively annotate the free text. It is completly open-source under the MIT license. It is currently being used to annotate entities and relations in Indian Court judgements, and has pre-built pattern recognition for certain entities.

The future is to automate the entity recognition process by introducing a Machine learning model (Named Entity Recogniser, NER) in the workflow, and reduce the time and efforts of the annotator.


Please feel free to write us at ``mailto:info@civicdatalab.in``, if you have any questions or concerns, we are happy to help!
