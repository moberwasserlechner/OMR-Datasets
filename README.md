# [Optical Music Recognition Datasets](https://apacha.github.io/OMR-Datasets/)

This repository contains a collection of many datasets used for various Optical Music Recognition tasks, including staff-line detection and removal, training of Convolutional Neuronal Networks (CNNs) or validating existing systems by comparing your system with a known ground-truth.

Note that most datasets have been developed by researchers and using their dataset requires accepting a certain license and/or citing their respective publications, as indicated for each dataset. Most datasets link to the official website, where you can download the dataset.

## Overview
The following datasets are referenced from this repository:

|                                           Name                                          	|    Types of Scores    	|     Size              |     Format             	|               Typical usages              	|
|-----------------------------------------------------------------------------------------	|:---------------------:	|:-----------------:    |:------------:         	|:-----------------------------------------:	|
| [Handwritten Online Musical Symbols (HOMUS)](#handwritten-online-musical-symbols-homus) 	| Handwritten           	| 15200 symbols   	    | Text-File             	| Symbol Classification (online + offline)  	|
| [Music Score Classification Dataset](#music-score-classification-dataset)               	| Printed               	| 1000 score images     | Images                	| Sheet Classification                      	|
| [Universal Music Symbol Collection](#universal-music-symbol-collection)                 	| Printed + Handwritten 	| ~ 90000 symbols	    | Images                	| Symbol Classification (offline)           	|
| [CVC-MUSCIMA](#cvc-muscima)                                                             	| Handwritten           	| 1000 score images     | Images                	| Staff line removal, writer identification 	|
| [MUSCIMA++](#muscima)                                                                   	| Handwritten           	| > 90000 annotatations | Images + XML          	| Symbol Classification, Object Detection   	|
| [DeepScores](#deepscores)                                                                	| Printed               	| 300000 images 	    | Images + XML              	| Symbol Classification, Object Detection, Semantic Segmentation                                   	|
| [MuseScore](#musescore)                                                                 	| Printed               	| > 340000 files 	    | MuseScore, PDF, MusicXML 	| Various                                   	|
| [MuseScore Monophonic MusicXML Dataset](#musescore-monophonic-musicxml-dataset)         	| Printed               	| 17000 IDs      	    | IDs for MuseScore files  	| Various                                   	|
| [Capitan collection](#capitan-collection)                                               	| Handwritten              	| 10230 symbols         | Images + Text-File    	| Symbol Classification                     	|
| [Rebelo Dataset](#rebelo-dataset)                                                        	| Printed               	| 15000 symbols  	    | Images                	| Symbol Classification                     	|
| [Fornes Dataset](#fornes-dataset)                                                       	| Handwritten           	| 4100 symbols   	    | Images                 	| Symbol Classification                     	|
| [Audiveris OMR](#audiveris-omr)                                                         	| Printed               	| 800 annotations	    | Images + XML          	| Symbol Classification, Object Detection   	|
| [Printed Music Symbols Dataset](#printed-music-symbols-dataset)                         	| Printed               	| 200 symbols    	    | Images                	| Symbol Classification                     	|
| [OpenOMR Dataset](#openomr-dataset)                                                     	| Printed               	| 706 symbols    	    | Images                	| Symbol Classification                     	|
| [Gamera MusicStaves Toolkit](#gamera-musicstaves-toolkit)                                	| Printed               	| 32 score images	    | Images                	| Staff line removal                        	|
| [Early Typographic Prints](#early-typographic-prints)                                   	| Printed               	| 240 score images      |                       	|                                           	|
| [Silva Online Handwritten Symbols](#silva-online-handwritten-symbols)                   	| Handwritten           	| 12600 symbols  	    |                       	|                                           	|
| [IMSLP](#imslp)                                                                         	| Printed               	| >420000 score images  | PDF                      	| Various                                      	|
| [Byrd Dataset](#byrd-dataset)                                                           	| Printed               	| 34 score images	    | Images                   	| Various                                      	|


If you find mistakes or know of any relevant datasets, that are missing in this list, please [open an issue](https://github.com/apacha/OMR-Datasets/issues/new) or directly file a pull request.

## Tools for working with the datasets
[![Build Status](https://travis-ci.org/apacha/OMR-Datasets.svg?branch=master)](https://travis-ci.org/apacha/OMR-Datasets) [![codecov](https://codecov.io/gh/apacha/OMR-Datasets/branch/master/graph/badge.svg)](https://codecov.io/gh/apacha/OMR-Datasets) [![PyPI version](https://badge.fury.io/py/omrdatasettools.svg)](https://badge.fury.io/py/omrdatasettools) [![Documentation Status](https://readthedocs.org/projects/omr-datasets/badge/?version=latest)](http://omr-datasets.readthedocs.io/en/latest/?badge=latest) [![Code Health](https://landscape.io/github/apacha/OMR-Datasets/master/landscape.svg?style=flat)](https://landscape.io/github/apacha/OMR-Datasets/master) [![GitHub license](https://img.shields.io/badge/License-MIT-blue.svg)](https://raw.githubusercontent.com/apacha/OMR-Datasets/master/LICENSE.txt) 


# Handwritten Online Musical Symbols (HOMUS)

**Official website**: [http://grfia.dlsi.ua.es/homus/](http://grfia.dlsi.ua.es/homus/)
 
[![License](https://img.shields.io/badge/License-Unknown-red.svg)](http://grfia.dlsi.ua.es/homus/)

**Summary**: The Handwritten Online Musical Symbols (HOMUS) dataset is a reference corpus with around 15000 samples for research on the recognition of online handwritten music notation. For each sample, the individual strokes that the musicians wrote on a Samsung Tablet using a stylus were recorded and can be used in online and offline scenarios.

**Scientific Publication**: J. Calvo-Zaragoza and J. Oncina, "Recognition of Pen-Based Music Notation: The HOMUS Dataset," 2014 22nd International Conference on Pattern Recognition, Stockholm, 2014, pp. 3038-3043. [DOI: 10.1109/ICPR.2014.524](http://dx.doi.org/10.1109/ICPR.2014.524)

**Example**:

![Example of HOMUS dataset](samples/homus.png)


*Remarks*: The original dataset contains around 20 artifacts and misclassifications that were reported to the authors and [corrected by Alexander Pacha](https://github.com/apacha/Homus). 


# Music Score Classification Dataset

**Official website**: [https://github.com/apacha/MusicScoreClassifier](https://github.com/apacha/MusicScoreClassifier) 

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)

**Summary**: A dataset of 2000 images, containing 1000 images of music scores and 1000 images of other objects including text documents. The images were taken with a smartphone camera from various angles and different lighting conditions.

**Scientific Publication**: Alexander Pacha, Horst Eidenberger, Towards Self-Learning Optical Music Recognition. 2017 16th IEEE International Conference on Machine Learning and Applications (ICMLA), Cancún, Mexiko, Dezember 2017. [DOI: 10.1109/ICMLA.2017.00-60](http://dx.doi.org/10.1109/ICMLA.2017.00-60)

**Example**:

![Example of MusicScoreClassifier dataset](samples/music-score-classifier.png)


# Universal Music Symbol Collection

**Official website**: [https://github.com/apacha/MusicSymbolClassifier](https://github.com/apacha/MusicSymbolClassifier), [Slides](https://docs.google.com/presentation/d/14g97TnrcI9o-5D6DIY-dMFfBp9kUAqpbe86c-VE83Bk/edit?usp=sharing) 

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)

**Summary**: A collection of various other datasets, that combines 7 datasets into a large unified dataset of 90000 tiny music symbol images from 79 classes that can be used to train a universal music symbol classifier. 74000 symbols are handwritten and 16000 are printed symbols.

**Scientific Publication**: Alexander Pacha, Horst Eidenberger. Towards a Universal Music Symbol Classifier. Proceedings of the 12th IAPR International Workshop on Graphics Recognition, Kyoto, Japan, November 2017. [DOI: 10.1109/ICDAR.2017.265](http://dx.doi.org/10.1109/ICDAR.2017.265)

**Example**:

![Example of MusicSymbolClassifier dataset](samples/universal-music-symbol-collection.png)


# CVC-MUSCIMA

**Official website**: [http://www.cvc.uab.es/cvcmuscima/index_database.html](http://www.cvc.uab.es/cvcmuscima/index_database.html)

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

**Summary**: The CVC-MUSCIMA database contains handwritten music score images, which has been specially designed for writer identification and staff removal tasks. The database contains 1,000 music sheets written by 50 different musicians. All of them are adult musicians, in order to ensure that they have their own characteristic handwriting style. Each writer has transcribed the same 20 music pages, using the same pen and the same kind of music paper (with printed staff lines). The set of the 20 selected music sheets contains music scores for solo instruments and music scores for choir and orchestra.

**Scientific Publication**: Alicia Fornés, Anjan Dutta, Albert Gordo, Josep Lladós. CVC-MUSCIMA: A Ground-truth of Handwritten Music Score Images for Writer Identification and Staff Removal. International Journal on Document Analysis and Recognition, Volume 15, Issue 3, pp 243-251, 2012. [DOI: 10.1007/s10032-011-0168-2](http://dx.doi.org/10.1007/s10032-011-0168-2)

**Example**:

![Example of CVC MUSCIMA dataset](samples/cvc-muscima.png)

# MUSCIMA++

**Official website**: [https://ufal.mff.cuni.cz/muscima](https://ufal.mff.cuni.cz/muscima)

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

**Summary**: MUSCIMA++ is a dataset of handwritten music notation for musical symbol detection that is based on the MUSCIMA dataset. It contains 91255 symbols, consisting of both notation primitives and higher-level notation objects, such as key signatures or time signatures. There are 23352 notes in the dataset, of which 21356 have a full notehead, 1648 have an empty notehead, and 348 are grace notes. Composite objects, such as notes, are captured through explicitly annotated relationships of the notation primitives (noteheads, stems, beams...). This way, the annotation provides an explicit bridge between the low-level and high-level symbols described in Optical Music Recognition literature.

**Scientific Publication**: Jan Hajič jr., Pavel Pecina. The MUSCIMA++ Dataset for Handwritten Optical Music Recognition. 14th International Conference on Document Analysis and Recognition, ICDAR 2017. Kyoto, Japan, November 13-15, pp. 39-46, 2017. [DOI: 10.1109/ICDAR.2017.16](http://dx.doi.org/10.1109/ICDAR.2017.16)

**Example**:

![Example of MUSCIMA++ dataset](samples/muscima-pp.png)

*Remarks*: Since this dataset is derived from the CVC-MUSCIMA dataset, using it requires to reference both works.


# DeepScores

**Official website**: [https://tuggeluk.github.io/deepscores/](https://tuggeluk.github.io/deepscores/)

[![License](https://img.shields.io/badge/License-Unknown-red.svg)](https://tuggeluk.github.io/deepscores/)

**Summary**: Synthetic dataset of 300000 annotated images of written music for object classification, semantic segmentation and object detection. Based on a large set of MusicXML documents that were obtained from [MuseScore](#musescore), a sophisticated pipeline is used to convert the source into LilyPond files, for which LilyPond is used to engrave and annotate the images. Images are rendered in five different fonts to create a variation of the visual appearance.

**Scientific Publication**: Lukas Tuggener, Isamil Elezi, Jürgen Schmidhuber, Marcello Pelillo, Thilo Stadelmann. DeepScores - A Dataset for Segmentation, Detection and Classification of Tiny Objects. Under review in ICPR 2018. 2018. [https://arxiv.org/abs/1804.00525](https://arxiv.org/abs/1804.00525)

**Example**:

![Example of deepscores dataset](samples/DeepScores1.png)

![Example of deepscores dataset](samples/DeepScores2.png)


# MuseScore

**Official website**: [https://musescore.com/sheetmusic](https://musescore.com/sheetmusic)

[![License: Mixed](https://img.shields.io/badge/License-Mixed-ff00ff.svg)](https://musescore.com/sheetmusic)

**Summary**: [MuseScore](https://musescore.org/) is a free music notation software and also allows their users to upload their sheet music to their website and share it with others. Currently (Jan. 2018) the website hosts over 340000 music sheets, that can be downloaded as MuseScore file (mscz), PDF, MusicXML, MIDI and MP3. 

**Publication**: [https://musescore.org](https://musescore.org)

**Example**:

![Example of MuseScore](samples/musescore.png)


# MuseScore Monophonic MusicXML Dataset

**Official website**: [https://github.com/eelcovdw/mono-musicxml-dataset]()

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)

**Summary**: This dataset contains the IDs to 17000 monophonic scores, that can be downloaded from musescore.com. A sample script is given that downloads one score, given you've obtained a developer key from the MuseScore developers.  

**Scientific Publication**: Eelco van der Wel, Karen Ullrich. Optical Music Recognition with Convolutional Sequence-to-Sequence Models. CoRR, arXiv:1707.04877, 2017. [https://arxiv.org/abs/1707.04877](https://arxiv.org/abs/1707.04877)

**Examples**: 

![Example of Monophonic MusicXML dataset](samples/monophonic-musescore.png)


# Capitan collection

**Official website**: [http://grfia.dlsi.ua.es/](http://grfia.dlsi.ua.es)

[![License](https://img.shields.io/badge/License-Unknown-red.svg)](http://grfia.dlsi.ua.es/homus/) (Freely available for research purposes)

**Summary**: A corpus collected by an electronic pen while tracing isolated music symbols from Early manuscripts. The dataset contains information of both the sequence followed by the pen and the patch of the source under the tracing itself. In total it contains 10230 samples unevenly spread over 30 classes. Each symbol is described as stroke (capitan stroke) and including the piece of score below it (capitan score).

**Scientific Publication**: Jorge Calvo-Zaragoza, David Rizo and Jose M. Iñesta. Two (note) heads are better than one: pen-based multimodal interaction with music scores. International Society of Music Information Retrieval conference, 2016. [Download the PDF](http://grfia.dlsi.ua.es/repositori/grfia/pubs/345/two-note-heads.pdf)

**Example**:

![Example of Capitan dataset](samples/capitan-collection.png)

*Remarks*: This dataset exists in two flavours: 

* As raw dataset, which contains only the textual descriptions of the strokes and the images, called *Bimodal music symbols from Early notation*. This format is similar to the HOMUS dataset.
* As rendered images inside of the *Isolated handwritten music symbols* dataset. Also refered to as Capitan collection.


# Rebelo Dataset

**Official websites**: [http://www.inescporto.pt/~arebelo/index.php](http://www.inescporto.pt/~arebelo/index.php) and [http://www.inescporto.pt/~jsc/projects/OMR/](http://www.inescporto.pt/~jsc/projects/OMR/)

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-blue.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

**Summary**: Three datasets of perfect and scanned music symbols including an extensive set of synthetically modified images for staff-line detection and removal. Contains approximately 15000 music symbols.

**Scientific Publication**: A. Rebelo, G. Capela, and J. S. Cardoso, "Optical recognition of music symbols: A comparative study" in International Journal on Document Analysis and Recognition, vol. 13, no. 1, pp. 19-31, 2010. [DOI: 10.1007/s10032-009-0100-1](http://dx.doi.org/10.1007/s10032-009-0100-1)

**Examples**:

![Example of Rebelo dataset](samples/rebelo1.png)
![Example of Rebelo dataset](samples/rebelo2.png)


*Remarks*: The dataset is usually only available upon request, but with written permission of Ana Rebelo I hereby make the datasets available under a permissive CC-BY-SA license, which allows you to use it freely given you properly mention her work by citing the above mentioned publication: [Download the dataset](https://owncloud.tuwien.ac.at/index.php/s/g3q0COsfPqbDUAW).


# Fornes Dataset
**Official website**: [http://www.cvc.uab.es/~afornes/](http://www.cvc.uab.es/~afornes/)

[![License](https://img.shields.io/badge/License-Unknown-red.svg)](http://grfia.dlsi.ua.es/homus/)

**Summary**: A dataset of 4100 black and white symbols of 7 different symbol classes: flat, natural, sharp, double-sharp, c-clef, g-clef, f-clef. 

**Scientific Publication**: A.Fornés and J.Lladós and G. Sanchez, "Old Handwritten Musical Symbol Classification by a Dynamic Time Warping Based Method", in Graphics Recognition: Recent Advances and New Opportunities. Liu, W. and Lladós, J. and Ogier, J.M. editors, Lecture Notes in Computer Science, Volume 5046, Pages 51-60, Springer-Verlag Berlin, Heidelberg, 2008. [DOI: 10.1007/978-3-540-88188-9_6
](http://dx.doi.org/10.1007/978-3-540-88188-9_6)

**Example**:

![Example of the Fornes Dataset](samples/fornes-accidentals.png)
![Example of the Fornes Dataset](samples/fornes-clefs.png)

# Audiveris OMR

**Official website**: [https://github.com/Audiveris/omr-dataset-tools](https://github.com/Audiveris/omr-dataset-tools)

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-AGPL--3.0-green.svg)](https://www.gnu.org/licenses/agpl-3.0.en.html)

**Summary**: A collection of four music sheets with approximately 800 annotated music symbols. The [DeepScore project](https://www.zhaw.ch/no_cache/en/research/people-publications-projects/detail-view-project/projekt/2895/) in cooperation with the ZHAW targets towards [automatically generating these images](https://github.com/Audiveris/omr-dataset-tools/wiki/Synthetic-Images) and the annotations from MuseScore or Lilypond documents. 

**Example**:

![Example of the Audiveris OMR Dataset](samples/audiveris-omr.png)


# Printed Music Symbols Dataset

**Official website**: [https://github.com/apacha/PrintedMusicSymbolsDataset](https://github.com/apacha/PrintedMusicSymbolsDataset)

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)

**Summary**: A small dataset of about 200 printed music symbols out of 36 different classes. Partially with their context (staff-lines, other symbols) and partially isolated.

**Example**: 

![Example of the Printed Music Symbols Dataset](samples/printed-music-symbols.png)


# OpenOMR Dataset

**Official website**: [http://sourceforge.net/projects/openomr/](http://sourceforge.net/projects/openomr/)

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-yellow.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)

**Summary**: A dataset of 706 symbols (g-clef, f-clef) and symbol primitives (note-heads, stems with flags, beams) of 16 classes created by Arnaud F. Desaedeleer as part of his master thesis to train artificial neural networks. 

**Scientific Publication**: Arnaud F. Desaedeleer, "Reading Sheet Music", Master Thesis, University of London, September 2006, [Download](http://sourceforge.net/projects/openomr/)


**Example**:

![Example of the Printed Music Symbols Dataset](samples/openomr.png)


# Gamera MusicStaves Toolkit

**Official website**: [http://music-staves.sf.net/](http://music-staves.sf.net/) and [https://github.com/hsnr-gamera](https://github.com/hsnr-gamera)

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-yellow.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)

**Summary**: The Synthetic Score Database by Christoph Dalitz that contains 32 scores that have been computer generated with different music typesetting programs. It contains ground truth data and is suitable for the deformations implemented in the toolkit.

**Scientific Publication**: C. Dalitz, M. Droettboom, B. Pranzas, I. Fujinaga: A Comparative Study of Staff Removal Algorithms. IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 30, no. 5, pp. 753-766 (2008) [DOI: 10.1109/TPAMI.2007.70749](http://dx.doi.org/10.1109/TPAMI.2007.70749)

**Example**:

![Example of the Gamera MusicStaves Dataset](samples/gamera-music-staves-toolkit.png)


# Early Typographic Prints

**Summary**: 240 pages of early typographic music having a total of 1478 staves and 52178 characters corresponding to 175 different symbols with ground-truth obtained by manually entering via a MIDI keyboard.

**Scientific Publication**: Laurent Pugin. Optical Music Recognition of Early Typographic Prints using Hidden Markov Models. 7th International Conference on Music Information Retrieval (ISMIR’06), Victoria, Canada, October 2006. [http://www.aruspix.net/publications/pugin06optical.pdf](http://www.aruspix.net/publications/pugin06optical.pdf)

**Example**:

![Example of the Pugin dataset](samples/pugin.png)

# Silva Online Handwritten Symbols 

**Summary**: Dataset of 12600 trajectories of handwritten music symbols, drawn by 50 writers with an Android application. Every writer drew each of the 84 different symbols three times.

**Scientific Publication**: Rui Miguel Filipe da Silva. Mobile framework for recognition of musical characters. Master Thesis. Universidade do Porto, June 2013. [https://repositorio-aberto.up.pt/bitstream/10216/68500/2/26777.pdf](https://repositorio-aberto.up.pt/bitstream/10216/68500/2/26777.pdf)


# IMSLP

**Official website**: [http://imslp.org](http://imslp.org)

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC_BY--SA_4.0-green.svg)](http://creativecommons.org/licenses/by-sa/4.0/)

**Summary**: The Petrucci Music Library is the largest collection of public domain music, with over 420000 (Jan. 2018) freely available PDF scores by almost 16000 composers accompanied by almost 50000 recordings. It also maintains an extensive list of [other music score websites](http://imslp.org/wiki/IMSLP:Other_music_score_websites), where you can find many more music sheets, e.g. collected during research projects by universities.

**Example**:

![The IMSLP music library](samples/imslp.png)

# Byrd Dataset

**Official website**: [http://www.diku.dk/hjemmesider/ansatte/simonsen/suppmat/jnmr/](http://www.diku.dk/hjemmesider/ansatte/simonsen/suppmat/jnmr/)

[![License](https://img.shields.io/badge/License-Unknown-red.svg)](http://grfia.dlsi.ua.es/homus/) (Authors want to be contacted)

**Summary**: A small dataset of 34 high quality images with individual music score pages of increasing difficulty. 

**Scientific Publication**: Donald Byrd & Jakob Grue Simonsen: "Towards a Standard Testbed for Optical Music Recognition: Definitions, Metrics, and Page Images". Journal of New Music Research, vol 44, nr.3, pages 169-195, 2015. [DOI: 10.1080/09298215.2015.1045424](http://dx.doi.org/10.1080/09298215.2015.1045424)

**Example**:

![Example of the Byrd Dataset](samples/byrd.png)

