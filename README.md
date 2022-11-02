# turkish-spacy-models

Welcome to page of Turkish spaCy models. You can find all the models under our [Huggingface repo](https://huggingface.co/turkish-nlp-suite).
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
You can download all the models from Huggingface:

* Transformer based model `pip install https://huggingface.co/turkish-nlp-suite/tr_core_news_trf/resolve/main/tr_core_news_trf-any-py3-none-any.whl`
* Large model: `pip install https://huggingface.co/turkish-nlp-suite/tr_core_news_lg/resolve/main/tr_core_news_lg-any-py3-none-any.whl`
* Medium model: `pip install https://huggingface.co/turkish-nlp-suite/tr_core_news_md/resolve/main/tr_core_news_md-any-py3-none-any.whl`

## Usage at a glance

After installing the models via pip you can directly use by loading into spaCy:

```
import spacy
nlp = spacy.load("tr_core_news_trf")

doc = nlp("Dün ben de gittim.")
```

Documentation is available on our website: [TODO]

## Tutorials
Please visit my channel and find the details in my upcoming book "Handbook of Turkish NLP"

