# ESO
ESO dataset v1.0  
www.mllp.upv.es/eso-dataset

An English-language speech corpus of the oncology domain for ASR training and benchmarking and MT benchmarking.

Keywords: automatic speech recognition; domain adaptation; large language models; machine translation; oncology; speech corpus; speech translation.

README CONTENTS
---------------

- [Overview](#overview)
- [Get the data](#get-the-data)
- [Corpus structure and contents](#corpus-structure-and-contents)
- [Acknowledgements](#acknowledgements)
- [Legal disclaimers](#legal-disclaimers)
<!--- - [Licence](#licence) --->
<!--- - [Citation](#citation) Açò va baix d'Overview !!! --->
<!--- - [Extended description](#extended-description) --->


OVERVIEW
--------

The ESO dataset includes:

#### Speech data

<!--- * 287 hours of English-language manually transcribed speech data in the oncology domain. --->
* 745 hours of English-language speech data in the oncology domain, of which 287 hours include manual transcriptions.
* 3 full sets of timed manual transcriptions.
* Both dev and test sets with temporally aligned manual translations.


<!--- CITATION
--------
[TBA] --->


GET THE DATA
------------

Download the full ESO speech and text corpus from:

https://www.mllp.upv.es/eso-dataset/eso_v1.0.tar.gz  
Size: 41 GiB  (compressed file)  
SHA-256 checksum: 24529aa4641cdc8b13f235f4fc2a295ab46e159fdaf846e561504ebacd498c6a


CORPUS STRUCTURE AND CONTENTS
-----------------------------

Total size: 48 GiB (uncompressed)

The data is organized in 3 main directories: "train" (training data), "dev"
(validation data) and "test" (evaluation data).
Both "dev" and "test" directories contain one subdirectory for each sample
and a list containing the IDs of the samples of the set. Each sample directory contains
the audio file, the slides and two subdirectories: the first one contains the transcription
data, with the transcription in plain-text format, the aligned transcription in srt format,
and the aligned transcription in srt format but sentence-segmented. On the other hand, the
manual_translation subdirectory contains a folder for each target language (de, es, fr, sl;
according to ISO 639-1 standard), in which we can find the original manual translation,
the source and target language files temporally aligned, and the file with the timestamps
for that language pair.
The "train" directory contains one subdirectory for each sample and one list
for each subset of data as follows:
* train_audios.lst: contains the IDs of the training samples.
* train_slides.lst: contains the IDs of the samples with slides.
* train_trans.lst: contains the IDs of the samples with manual transcriptions.
* trains_trans+slides.lst: contains the IDs of the samples with manual transcriptions and slides.

Here we can see more completely the corpus structure, with additional
subdirectories:

```
  ESO
  ├── dev
  │   ├── dev.lst
  │   ├── <SAMPLE_ID>
  │   │   ├── <SAMPLE_ID>.m4a
  │   │   ├── slides.pdf>
  │   │   ├── manual_transcription
  │   │   │   ├── <SAMPLE_ID>.srt
  │   │   │   ├── <SAMPLE_ID>.txt
  │   │   │   ├── sentence_segmented
  │   │   │   │   ├── <SAMPLE_ID>.srt
  │   │   ├── manual_translation
  │   │   │   ├── de
  │   │   │   │   ├── <SAMPLE_ID>.de
  │   │   │   │   ├── <SAMPLE_ID>.docx
  │   │   │   │   ├── <SAMPLE_ID>.en
  │   │   │   │   └── <SAMPLE_ID>.lst
  │   │   │   ├── es ...
  │   │   │   ├── fr ... 
  │   │   │   ├── sl ...
  ├── test ... // Same as dev
  ├── train
  │   ├── train_audios.lst
  │   ├── train_slides.lst
  │   ├── train_trans.lst
  │   ├── train_trans+slides.lst
  │   ├── <SAMPLE_ID>
  │   │   ├── <SAMPLE_ID>.m4a
  │   │   ├── <SAMPLE_ID>.srt
  │   │   ├── <SAMPLE_ID>_transcription.pdf
  │   │   ├── <SAMPLE_ID>_slide.pdf
```


ACKNOWLEDGEMENTS
----------------

This work has received funding from the EU4Health Programme 2021-2027 as
part of Europe's Beating Cancer Plan under Grant Agreements nos. 101056995 and 101129375;
and from the Government of Spain's grant PID2021-122443OB-I00 funded by
MCIN/AEI/10.13039/501100011033 and by "ERDF A way of making Europe" and
grant PDC2022-133049-I00 funded by MCIN/AEI/10.13039/501100011033 and by
the "European Union NextGenerationEU/PRTR".

The authors gratefully thank the [European School of Oncology](https://www.eso.net) 
for the provision of this dataset in the framework of the EU research project 
[Interact-Europe](https://www.europeancancer.org/eu-projects/impact/interact-europe). 


LEGAL DISCLAIMER
---------------
Speech and text data were provided by the [European School of Oncology
(ESO)](https://www.eso.net) from its online platform [e-ESO](https://www.e-eso.net) under
the EU research project
[Interact-Europe](https://www.europeancancer.org/eu-projects/impact/interact-europe).
The following disclaimers are those available in the [e-ESO platform](https://www.e-eso.net)
on April 3rd, 2024:

#### Content disclaimer

The content of the e-ESO website is intended as an informational and
educational tool. It is mainly designed for oncology professionals and
other physicians interested in oncology. With the aim of disseminating
information, the website will propose contents provided by
third-parties. However, ESO has no responsibility to whether this
content, or the content of linked websites, is accurate or complete.

Even though the website includes scientific and medical
information, it is not designed to provide medical advice and no
responsibility can be taken to whether the medical information is
complete, exhaustive or accurate. Patients and the general public
visiting the website should always seek professional medical advice.

#### Clinical cases disclaimer

The intent of the clinical case discussions is exclusively
educational and neither ESO nor the involved Experts and Discussants
can take responsibility for individual treatment/management decisions,
nor that considerations were complete, exhaustive or accurate. The
drugs and the medical interventions mentioned in the discussions are
not the only therapeutic options, but simply reflect the personal
choices of the presenter.

ESO's intent is not to provide paradigms but to debate real issues in
order to improve the level of its educational offer. The clinical case
presentations are not meant to provide medical advice, and patients and
the general public visiting the website should always seek
professional medical advice.

#### Presentations property and disclaimer

The website contains presentations aimed at providing new knowledge
and competences. These materials remain property of the authors or ESO
respectively. Each author continues to retain the rights to reproduce
the specific images and text which he/she provided. Users are granted
permission to view and, if permitted by the author, to download the
presentations. In any case, for any use other than personal, they must
seek permission from ESO (Via Turati, 29 - Milan, Italy).

Presentations from any single author or multiple authors may not be
reproduced without the written consent of that author. In turn,
authors are required to ascertain and respect the copyright property
of the information they provide in their presentations and to include
the source of such information.

ESO is not responsible for any injury and/or damage to persons or
property as a matter of a products liability, negligence or otherwise,
or from any use or operation of any methods, products, instructions or
ideas contained in the material published in these
presentations. Because of the rapid advances in medical sciences, we
recommend that independent verification of diagnoses and drugs dosages
should be made. Every effort has been made to faithfully reproduce the
material as submitted. However, no responsibility is accepted for
omissions. ESO does not endorse any opinions expressed in the
presentations.

#### Subtitles and transcriptions

Subtitles and transcriptions are available for selected materials for
the purpose of helping users understand the contents of the
educational sessions.

Uncertain words have been indicated with ?? before and after the part.

Parts that could not be understood at all have been indicated as
[Audio Not Clear].

Every effort has been made to faithfully reproduce the audio of the
sessions as recorded. However, no responsibility is accepted for
mistakes or omissions. ESO does not endorse any opinions expressed in
the presentations.

#### Website policy

Indicated disclaimers, policies and terms apply to the e-ESO website
and its users. ESO may decide at any time to amend these terms and
post the modified document on the website. ESO will not be liable for
any modification, suspension or termination of the service, or loss of
related information. Users assume all risk for any damage to their
computer system or loss of data that results from obtaining any
content from the website, including any damages resulting from
computer viruses. The content is provided on a 'as is', 'as available'
and 'with all faults' basis.
