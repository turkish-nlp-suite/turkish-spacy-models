# turkish-spacy-models

Welcome to page of Turkish spaCy models. You can find all the models under our [Huggingface collection](https://huggingface.co/collections/turkish-nlp-suite/turkish-spacy-models). The official Huggingface repo for our organization is [Turkish NLP Suite HF repo](https://huggingface.co/collections/turkish-nlp-suite).
This repo contains config files for

- tr_core_web_md
- tr_core_web_lg
- tr_core_web_trf

All pipelines contains a tokenizer, trainable lemmatizer, POS tagger, dependency parser, morphologizer and NER components.

## Available Models
`tr_core_web_lg` is a CNN-based large sized model, which offers a good accuracy and works on decent speed. This model includes all the components above
and is packaged with large sized Floret word vectors.

Similarly `tr_core_web_md` is a CNN-based medium sized model, which achieves a decent accuracy and might be a good choice for speed-critical applications.
and is packaged with medium sized Floret word vectors.

`tr_core_web_trf` is a Tranformer based pipeline. It offers a great accuracy, if you have good computing resources, this is your model of choice (even better some GPUs).

## Installation
You can download all the models from Huggingface, for more information please visit models' individual HF repos: [trf](https://huggingface.co/turkish-nlp-suite/tr_core_news_trf), [lg](https://huggingface.co/turkish-nlp-suite/tr_core_news_lg), [md](https://huggingface.co/turkish-nlp-suite/tr_core_news_md). Still installing at a quick glance:

* Transformer based model `pip install https://huggingface.co/turkish-nlp-suite/tr_core_news_trf/resolve/main/tr_core_news_trf-1.0-py3-none-any.whl`
* Large model: `pip install https://huggingface.co/turkish-nlp-suite/tr_core_news_lg/resolve/main/tr_core_news_lg-1.0-py3-none-any.whl`
* Medium model: `pip install https://huggingface.co/turkish-nlp-suite/tr_core_news_md/resolve/main/tr_core_news_md-1.0-py3-none-any.whl`

## Usage at a glance

After installing the models via pip you can directly use by loading into spaCy:

```
import spacy
nlp = spacy.load("tr_core_news_trf")

doc = nlp("Dün ben de gittim.")
```

For a quickstart, Colab code is available for all the models including installing, importing models and some minimal code for all the models, [trf](https://colab.research.google.com/drive/1pe9uZ9YFCmQn342XytYCFBzZq0s8if4a?usp=sharing), [lg](https://colab.research.google.com/drive/1mJIb4DBo83uZXIf9tFtcLC23rDWGRMey?usp=sharing) and [md](https://colab.research.google.com/drive/1pf1uJcs83y8rd8nkOfcvTuSv3bPAS9_t?usp=sharing)

## Tutorials
Please visit my channel for two playlists [Hızlı spaCy Türkçe tarifleri](https://www.youtube.com/playlist?list=PLJTHlIwB8VcoWxYHnsZOQCxWOraW42NBj) and [spaCy modeli nasıl yapılır?](https://www.youtube.com/playlist?list=PLJTHlIwB8Vcp_1b1eFwKcKKmzfs16EFtH). You'll find quick recipes with spaCy Turkish in the first playlist and the second playlist gives details of how to train&package a model for a new language.

This work is supported by Google Developer Experts Program. Part of Duygu 2022 Fall-Winter collection, "Turkish NLP with Duygu"/ "Duygu'yla Türkçe NLP". All rights reserved. If you'd like to use the models in your own work, please kindly cite the paper [A Diverse Set of Freely Available Linguistic Resources for Turkish](https://aclanthology.org/2023.acl-long.768/):

```
@inproceedings{altinok-2023-diverse,
    title = "A Diverse Set of Freely Available Linguistic Resources for {T}urkish",
    author = "Altinok, Duygu",
    booktitle = "Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2023",
    address = "Toronto, Canada",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.acl-long.768",
    pages = "13739--13750",
    abstract = "This study presents a diverse set of freely available linguistic resources for Turkish natural language processing, including corpora, pretrained models and education material. Although Turkish is spoken by a sizeable population of over 80 million people, Turkish linguistic resources for natural language processing remain scarce. In this study, we provide corpora to allow practitioners to build their own applications and pretrained models that would assist industry researchers in creating quick prototypes. The provided corpora include named entity recognition datasets of diverse genres, including Wikipedia articles and supplement products customer reviews. In addition, crawling e-commerce and movie reviews websites, we compiled several sentiment analysis datasets of different genres. Our linguistic resources for Turkish also include pretrained spaCy language models. To the best of our knowledge, our models are the first spaCy models trained for the Turkish language. Finally, we provide various types of education material, such as video tutorials and code examples, that can support the interested audience on practicing Turkish NLP. The advantages of our linguistic resources are three-fold: they are freely available, they are first of their kind, and they are easy to use in a broad range of implementations. Along with a thorough description of the resource creation process, we also explain the position of our resources in the Turkish NLP world.",
}
```
