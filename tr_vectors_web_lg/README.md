Large sized [Floret](https://github.com/explosion/floret) word vectors for Turkish trained on [MC4 corpus](https://arxiv.org/abs/1910.10683).

Vector dim is `300` and bucket size is `200.000` .

Note that if you want to relicate the experiment, you need a good size storage. You can pick up the vectors from [Huggingface repo](https://huggingface.co/turkish-nlp-suite/tr_vectors_web_lg).
You can build the vectors run `spacy project run all`. Note that script **doesn't** clean intermeidate files, you might need to clean `models/.bin` and `models/.vec` yourself if you don't
need those files.
