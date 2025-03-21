# Sentiment Analysis on Movies Reviews


## Install

You can use `Docker` to easily install all the needed packages and libraries:

```bash
$ sudo docker build -t s06_project .
```

### Run Docker

```bash
$ sudo docker run --rm -it \
    -p 8888:8888 \
    -v $(pwd):/home/app/src \
    s06_project \
    bash
```

## Run Project

It doesn't matter if you are inside or outside a Docker container, in order to execute the project you need to launch a Jupyter notebook server running:

```bash
$ jupyter notebook --ip 0.0.0.0 --port 9000 --allow-root
```

Then, inside the file `Sentiment_Analysis_NLP.ipynb`, you can see the project statement, description and also which parts of the code you must complete in order to solve it.

## Tests

We've added some basic tests to `Sentiment_Analysis_NLP.ipynb` that you must be able to run without errors in order to approve the project. If you encounter some issues in the path, make sure to be following these requirements in your code:

- Every time you need to run a tokenizer on your sentences, use `nltk.tokenize.toktok.ToktokTokenizer`.
- When removing stopwords, always use `nltk.corpus.stopwords.words('english')`.
- For Stemming, use `nltk.porter.PorterStemmer`.
- For Lematizer, use `Spacy` pre-trained model `en_core_web_sm`.

You can use others methods if you want to do extra experimentation but do it outside the code used to run the tests. Otherwise, they may fail for some specific cases.
