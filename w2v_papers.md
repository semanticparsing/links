# W2V related
* [Glyph-aware Embedding of Chinese Characters](http://www.aclweb.org/anthology/W17-4109)
  - ACL2017 [Codes](https://github.com/falcondai/chinese-char-lm)
  - Notes
    - The distribution of Chinese characters deviate markedly from Zipf’s law, whereas Chinese words(segmented) distributed according the Zipf's law.
    - Language model and word segmentation tasks
    - Feed the glyph as an input to FNN, use the raw pixels(gray-scale image) of a glyph(Google Noto font).
    - CNN, Linear, ID
    - Conclusion: **Not that usefull**
* [Learning Character-level Compositionality with Visual Features](https://arxiv.org/pdf/1704.04859.pdf)
  - ACL2017 Graham Neubig
* [Sub-character Neural Language Modelling in Japanese](http://www.aclweb.org/anthology/W17-4122)
  - ACL2017, sclem2017
* [Non-distributional Word Vector Representations](http://www.manaalfaruqui.com/papers/acl15-nondist.pdf)
  - ACL2015 cdyer@CMU [Codes](https://github.com/mfaruqui/non-distributional)
  - Notes
    - linguistic vectors contain useful information orthogonal to distributional information.
    - linguistic word vectors construction: extracting word level information from linguistic resources
      - WordNet: `SYNSET.FILM.V.01`, `SYNSET.FILM.N.01`, `HYPO.COLLAGEFILM.N.01`, `HYPER:SHEET.N.06`
      - Supsersenses: `SS.NOUN.ANIMAL`
      - FrameNet: `VERB.FRAME.REGARD`, `VERB.FRAME.ROLE.EVALUEE`
      - Emotion & Sentiment: `POL.NEG`, `EMO.DISGUST`, `EMO.FEAR`
      - Connotation: `CON.NOUN.NEG`, `CON.ADJ.POS`, `CON.VERB.NEUT`
      - Color: `COLOR.RED`
      - Part of Speech Tags: `PTB.NOUN`, `PTB.VERB`
      - Synonymy & Antonymy: `SYNO.LOVE`, `SYNO.ACCEPTABLE`, `ANTO.FAVORITISM`, `ANTO.INJUSTICE`
    - Vector features:
      - 172,418 in length; 99.9% sparse: 34 non-zero features out of 172418 on average.
* [Joint Embeddings of Chinese Words, Characters, and Fine-grained Subcharacter Components](http://aclweb.org/anthology/D17-1027)
  - EMNLP2017 [Codes](https://github.com/HKUST-KnowComp/JWE)
  - Notes
    - Tasks: Word similarity & Word analogy
    - OOV problem, charactor of n-grams  for English(alphabetic writing systems), but Chinese is a logosyllabic writing system
    - Joint learning word embedding
      - CBOW
      - average of context word vectors, average of context character vectors, average of context subcharacter vectors to predict the target word
      - uses the sum of these three prediction losses as the objective function
* [Word-Context Character Embeddings for Chinese Word Segmentation](http://aclweb.org/anthology/D17-1080)
  - EMNLP2017 南京大学
* [Refining Word Embeddings for Sentiment Analysis](http://aclweb.org/anthology/D17-1057)
  - EMNLP 2017
  - Yuan Ze University, Taiwan
* [AutoExtend: Combining Word Embeddings with Semantic Resources.](http://www.mitpressjournals.org/doi/full/10.1162/COLI_a_00294)
  - Computational Linguistics, 2017.
  - Hinrich Schütze, LMU Munich
* [Enriching Word Vectors with Subword Information](https://research.fb.com/wp-content/uploads/2017/06/tacl.pdf?)
  - TACL, Association for Computational Linguistics (ACL 2017)
  - Armand Joulin, Edouard Grave, Piotr Bojanowski, [Tomas Mikolov](https://research.fb.com/people/mikolov-tomas/)
  - fastText [Codes](https://github.com/facebookresearch/fastText)
  - Notes
    - Limitation of assigning a distinct vector to each word, no parameter sharing. large vocabulary and rare words
    - Skipgram model, evaluated on word similarity and word analogy tasks.
      - Each word is represented as a bag of charecter *n*-grams
      - word vectors as the sum of these representations
* [Mimicking Word Embeddings using Subword RNNs](http://aclweb.org/anthology/D17-1010)
  - EMNLP2017 [Codes](https://github.com/yuvalpinter/mimick) based on DyNet
  - Given a word embedding dictionary (with vectors from, e.g. FastText or Polyglot or GloVe), Mimick trains a character-level neural net that learns to approximate the embeddings. It can then be applied to infer embeddings in the same space for words that were not available in the original set (i.e. OOVs - Out Of Vocabulary).
  - Notes
    - post-processing applied to exsiting word embeddings, regardless of how they were trained
    - Predictive function: Word Type Character Bi-LSTM
    - <img src="https://github.com/semanticparsing/links/blob/master/images/mimick.jpg" width="300px">
    - Nearest-neighbor examination for the learned model
      - word shape is learned well (acronyms, capitalizations, suf-fixes);
      - the model shows robustness to typos (e.g., developiong, corssing);
      - part-of-speech is learned across multiple suffixes (pesky – euphoric, ghastly);
      - word compounding is detected (e.g., lawnmower – bookmaker, postman);
      - semantics are not learned well (as is to be expected from the lack of context in training)
* [Polyglot: Distributed Word Representations for Multilingual NLP](http://www.aclweb.org/anthology/W13-3520)
  - ACL2013 [Codes](https://sites.google.com/site/rmyeid/projects/polyglot)
