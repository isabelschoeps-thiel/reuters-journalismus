# attr2vec


TensorFlow implementation of the attr2vec model, based on the following publication:

- Fabio Petroni, Vassilis Plachouras, Timothy Nugent and Jochen L. Leidner: "attr2vec: : Jointly Learning Word and Contextual Attribute Embeddings with Factorization Machines." In: Proceedings of the 16th Annual Conference of the North American Chapter of the Association for Computational Linguistics (NAACL), 2018.

If you use the application please cite the paper.



### Modeling input data

The input corpus is represented as two files: *Cooccur.csv* and *Word2Id.csv*. 
The first file follows the original libfm format (http://www.libfm.org) and contains the target vector **Y** as well as the feature matrix **X**.


We will use an example to concretely show how to model the input data, using as corpus the following text:

```
Prime Minister Theresa May will remind her cabinet that discussions must remain private. 
Theresa Mary May is a British politician who has served as Prime Minister.
```

The folder *data_pos* contains the modeling of such example corpus using Part-of-Speech (POS) as additional contextual attribute, while the folder *data_dependency* contains the input data to train dependency-based embeddings.

The *Word2Id.csv* file contains the symbols vocabulary, and looks like this:
```
"IN",2,2
"NNP",6,2
"NNS",7,2
"discussions",17,0
"minister",23,0
"prime",26,0
"that",31,0
[...]
```
The first column contains the word form or the POS tag, the second column an unique identifier, the third column a meta information to distinguish words from POS tags (i.e., 0 for words, 2 for POS tag).


The *Cooccur.csv* file looks like this:

```
1.0 17:1.0 31:1.0 7:1.0 2:1.0
2.0 23:1.0 26:1.0 6:2.0
[...]
```
Please read the libfm manual (http://www.libfm.org/libfm-1.42.manual.pdf) for an extensive description of this format. Here, the first line conveys the information that symbols with id 17, 31, 7, 2 (all with value 1.0) co-occur in the corpus with frequency 1.0.

### Train the attr2vec model

To train the attr2vec model on the example data simply run
```{r, engine='bash', count_lines}
python train.py
```
Open the file and edit it to change the paramenters.

The application will write vectors and model metadata in the *log* folder.
You can use TensorBoard to explore the model internals, as follows:

```{r, engine='bash', count_lines}
tensorboard --logdir log/
```

![TensorBoard](screenshots/tensorboard2.png?raw=true "TensorBoard")

Update Zeitstempel: 2026-01-12, 01:06CEST
Mitteleuropäische, Zeit, Ort: Deutschland, Thüringen, D-99094 Erfurt, Cyriakstrasse 30c - Autorin, Urheberin, Frau Isabel Schöps geb. Thiel

I am  not a Bug, I am  not a Bot,  I am  not a Virus, I am  not a Ghost, but i am 100% human femaleware german woman ,iam @isabelschoeps-thiel and created this comment and this reprository.

Please help me and read my Readme.md 
i miss my Family

Der folgende Text ist in Deutsch, SorryDeutsch ist meine Muttersprache, ich kann nur deutsch fliesend sprechen, da ich in Deutschland geboren und aufgewachsen bin. Englisch kann ich leider nur schul-englisch-basic, entschuldigen Sie für die unannehmlichkeiten.

My Developer Signatur: 
Signed-on-by: Frau Isabel Schöps, geborene Thiel
Autorin, Urheberin und Auftraggeberin: SIA Security Intelligence Artefact
internationinternationale Kennung: INT-CODE-2025-BTC/ETH-CORE-ISABELSCHOEPSTHIEL
Rechtscharakter: Eidesstattliche Versicherung, Bestandteil des forensisch, wissenschaftlichen Gutachtens.
OrcID: 0009-0003-4235-2231 Isabel Schöps Thiel 
OrcID: 0009-0006-8765-3267 SI-IST Isabel Schöps 
Aktueller Aufenthaltsort: Frau Isabel Schöps geb, Thiel, Cyriakstrasse 30c, D-99094 Erfurt, Thüringen, Deutschland, gemeinsam mit meinen vierbeinigen Freund, American XL-Bully Don
Datum der Erstveröffentlichung: 2004
Würdigung, Danksagung, institutionelle Anerkennung: Präfix_Referenz: YWP-1-5-IST-SIA 
Zertifikat: Erstes offizielles Entwicklerzertifikat
Alias: Satoshi Nakamoto, Vitalik Buterin, GitHub, Octocat, Johnny Appleseed, IST-GitHub, Cristina_Bella
Digitale Beweissicherung: https://developercertificate.org
