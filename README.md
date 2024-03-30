# ESO
ESO dataset v1.0
www.mllp.upv.es/eso-dataset



README CONTENTS
---------------

- [Overview](#overview)
- [Get the data](#get-the-data)
- [Corpus structure and contents](#corpus-structure-and-contents)
- [Acknowledgements](#acknowledgements)
<!--- - [Citation](#citation) Açò va baix d'Overview !!! --->
<!--- - [Extended description](#extended-description) --->
<!--- - [Legal disclaimers](#legal-disclaimers) --->
<!--- - [Licence](#licence) --->


OVERVIEW
--------

The ESO dataset includes:

#### Speech data

<!--- * 287 hours of English-language manually transcribed speech data in the oncology domain. --->
* 745 hours of English-language speech data in the oncology domain, of which 287 hours are manually transcribed data.
* 3 full sets of timed transcriptions: official non-verbatim transcriptions,
  automatically noise-filtered transcriptions and automatically verbatimized
  transcriptions.
* 18 hours of speech data with both manually revised verbatim transcriptions
  and official non-verbatim transcriptions, split in 2 independent
  validation-evaluation partitions for 2 realistic ASR tasks (with vs. without previous
  knowledge of the speaker).


<!--- CITATION
--------
[TBA] --->


GET THE DATA
------------

Download the full ESO speech and text corpus from:

https://www.mllp.upv.es/eso-dataset/eso_v1.0.tar.gz  
Size: 48 GiB  
<!--- SHA-256 checksum: 4d360170ef8f1d1ece55566eda4211274b27328427a3443061f43d80d3346e74 --->


CORPUS STRUCTURE AND CONTENTS
-----------------------------

Total size: 48 GiB

The data is organized in 3 main directories: "train" (training data), "dev"
(validation data) and "test" (evaluation data).
Both "dev" and "test" directories contain one subdirectory for each sample
and a list containing the IDs of the samples of the set. Each sample directory contains
the audio file, the slides and two subdirectories: the first one contains the transcription
data, with the transcription in plain-text format, the aligned transcription in srt format,
and the aligned transcription in srt format but sentence segmented.
The "train" directory contain one subdirectory for each sample and one list
for each subset of data as follows:
* train_audios.lst: contains the IDs of the training samples.
* train_slides.lst: contains the IDs of the samples with slides.
* train_trans.lst: contains the IDs of the samples with the manual transcriptions.
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
---------------
This work has received funding from the EU4Health Programme 2021-2027 as
part of Europe’s Beating Cancer Plan under Grant Agreements nos. 101056995 and 101129375;
and from the Government of Spain’s grant PID2021-122443OB-I00 funded by
MCIN/AEI/10.13039/501100011033 and by “ERDF A way of making Europe” and
grant PDC2022-133049-I00 funded by MCIN/AEI/10.13039/501100011033 and by
the “European Union NextGenerationEU/PRTR”. The authors gratefully acknowledge
the financial support of the Generalitat Valenciana under project IDIFEDER/2021/059.
