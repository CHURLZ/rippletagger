**This works, but is no longer maintained. Please see the original project for the latest updates: https://github.com/datquocnguyen/RDRPOSTagger**

# RippleTagger

**RippleTagger** identifies part-of-speech tags (Nouns, Verbs, and so on...). You give it a sentence, it gives you a list of tags back. Tagging is the first step in many language processing tasks.

## Example usage

```python
>>> from rippletagger.tagger import Tagger
>>> tagger = Tagger(language="en")
>>> print tagger.tag(u"The quick brown fox jumps over the lazy dog .")

[
    (u'The', u'DET'),
    (u'quick', u'ADJ'),
    (u'brown', u'ADJ'),
    (u'fox', u'NOUN'),
    (u'jumps', u'VERB'),
    (u'over', u'ADP'),
    (u'the', u'DET'),
    (u'lazy', u'ADJ'),
    (u'dog', u'NOUN'),
    (u'.', u'PUNCT'),
]
```

You can read about what the different tags mean at the [Universial Dependencies project](http://universaldependencies.org/u/pos/index.html).

## Why should you use RippleTagger?

- It supports 40 (!) languages out of the box.
- It's fast.
- It has good accuracy.
- It has no dependences and is pure python.

## Installation

```bash
pip install rippletagger
```

## Develop locally and run the tests

```bash
git clone git@github.com:EmilStenstrom/rippletagger.git
cd rippletagger
python setup.py test
```

## Supported languages

You can use either the 2-letter code, 3-letter code or language name as the parameter to Tagger. In some cases there are more than one treebank available for a language. In that case you can choose which treebank you want to use by appending "-2", "-3" and so on to the language code.

2-letter code | 3-letter code | Name | Treebank | Accuracy
:------- | :------- | :------- | :------- | :-------
-- | grc | ancient_greek | Ancient_Greek | 91.56865075
-- | grc | ancient_greek | Ancient_Greek-PROIEL | 95.71938169
ar | ara | arabic | Arabic | 94.414521
eu | eus | basque | Basque | 92.42635595
bg | bul | bulgarian | Bulgarian | 96.1294013
ca | cat | catalan | Catalan | 96.51742106
zh | zho | chinese | Chinese | 89.45221445
hr | hrv | croatian | Croatian | 93.86666667
cs | ces | czech | Czech | 97.67695433
cs-2 | ces-2 | czech-2 | Czech-CAC | 97.82568807
cs-3 | ces-3 | czech-3 | Czech-CLTT | 97.00802724
da | dan | danish | Danish | 93.47382733
nl | nld | dutch | Dutch | 88.75577614
nl-2 | nld-2 | dutch-2 | Dutch-LassySmall | 94.36650592
en | eng | english | English | 92.70401658
en-2 | eng-2 | english-2 | English-LinES | 94.39924537
et | est | estonian | Estonian | 93.83607943
fi | fin | finnish | Finnish | 92.2428884
fi-2 | fin-2 | finnish-2 | Finnish-FTB | 90.9631537
fr | fra | french | French | 95.22884882
gl | glg | galician | Galician | 96.3053856
de | deu | german | German | 90.39729092
-- | got | gothic | Gothic | 93.85420706
el | gre/ell | greek | Greek | 96.85956246
he | heb | hebrew | Hebrew | 93.5171585
hi | hin | hindi | Hindi | 95.02399097
hu | hun | hungarian | Hungarian | 88.68949233
id | ind | indonesian | Indonesian | 90.74702886
ga | gle | irish | Irish | 90.60455378
it | ita | italian | Italian | 96.48434167
kk | kaz | kazakh | Kazakh | 79.22077922
la | lat | latin | Latin | 90.39735099
la-2 | lat-2 | latin-2 | Latin-ITTB | 98.24373855
la-3 | lat-3 | latin-3 | Latin-PROIEL | 95.78693144
lv | lav | latvian | Latvian | 86.34880803
no | nor | norwegian | Norwegian | 94.60278351
cu | chu | old_church_slavonic | Old_Church_Slavonic | 94.62492617
fa | fas | persian | Persian | 95.99826281
pl | pol | polish | Polish | 94.0848991
pt | por | portuguese | Portuguese | 95.08144363
pt-2 | por-2 | portuguese-2 | Portuguese-BR | 95.08798152
ro | ron | romanian | Romanian | 94.51972789
ru | rus | russian | Russian-SynTagRus | 97.65354521
sl | slv | slovenian | Slovenian | 94.02687904
sl-2 | slv-2 | slovenian-2 | Slovenian-SST | 91.15554049
es | spa | spanish | Spanish | 95.12795276
es-2 | spa-2 | spanish-2 | Spanish-AnCora | 96.78868917
sv | swe | swedish | Swedish | 94.39564215
sv-2 | swe-2 | swedish-2 | Swedish-LinES | 94.47010209
ta | tam | tamil | Tamil | 82.08886853
tr | tur | turkish | Turkish | 91.92623412

## Technical details

RippleTagger is a slimmed down version of [RDRPOSTagger](https://github.com/datquocnguyen/RDRPOSTagger).

The general architecture and experimental results of RDRPOSTagger can be found in our following papers:

- Dat Quoc Nguyen, Dai Quoc Nguyen, Dang Duc Pham and Son Bao Pham. [RDRPOSTagger: A Ripple Down Rules-based Part-Of-Speech Tagger](http://www.aclweb.org/anthology/E14-2005). In *Proceedings of the Demonstrations at the 14th Conference of the European Chapter of the Association for Computational Linguistics*, EACL 2014, pp. 17-20, 2014. [[.PDF]](http://www.aclweb.org/anthology/E14-2005) [[.bib]](http://www.aclweb.org/anthology/E14-2005.bib)

- Dat Quoc Nguyen, Dai Quoc Nguyen, Dang Duc Pham and Son Bao Pham. [A Robust Transformation-Based Learning Approach Using Ripple Down Rules for Part-Of-Speech Tagging](http://content.iospress.com/articles/ai-communications/aic698). *AI Communications* (AICom), vol. 29, no. 3, pp. 409-422, 2016. [[.PDF]](http://arxiv.org/pdf/1412.4021.pdf) [[.bib]](http://rdrpostagger.sourceforge.net/AICom.bib)

### Citations

**Please cite** either the EACL or the AICom paper whenever RDRPOSTagger is used to produce published results or incorporated into other software.

