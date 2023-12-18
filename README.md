# Measuring Political Sentiment in Tweets through Weighted Hashtag Analysis

### Final Project, *MIT 6.8610 Quantitative Methods of Natural Language Processing*

**See final paper [here](https://drive.google.com/file/d/1YP8lB3kXKD6tXG8ITDzQHiYFL88nDhPM/view?usp=sharing).**

Tweets are an abundant source of opinionated statements from the general public, and analyzing the political sentiment behind them could yield important insights, such as predictions on the outcome of a presidential election [(Ibrahim et al., 2015)](https://ieeexplore.ieee.org/abstract/document/7395825?casa_token=uUpkFuB5e5cAAAAA:NBFID3M3gMM_DLeJ9dTUuu22IrnVq5Ad53j7MyCQMeoeUhyk3h7HOTJ8oIeV8Bg_3ns4vTsXtg). However, many existing analyses of political Tweets either consider hashtags with equal weight as the rest of the text [(Varma and Harsha, 2022)](https://link.springer.com/chapter/10.1007/978-981-19-0475-2_3) or remove them from training data entirely [(Harjule et al., 2020)](https://ieeexplore.ieee.org/abstract/document/9091774). In this project, we create a political sentiment analyzer that places more weight on the embedding vectors corresponding to hashtagged phrases while conducting political sentiment analysis on Tweets, as hashtags often times convey critical information regarding a person's political affiliations, are shared between people who have similar views, and can contribute a significant amount to understanding political sentiment.

We analyze the impact of scaling hashtagged word embedding vectors through 4 different model architectures for political sentiment classification that span both context-agnostic and context-dependent embeddings: a Naive Word2Vec model trained on our custom Tweet vocabulary with a Logistic Regression head, a [Pre-trained Word2Vec model with a Logistic Regression head](https://radimrehurek.com/gensim/models/word2vec.html), a Pre-trained Contextualized Embedding Transformer [(DistilBERT)](https://huggingface.co/docs/transformers/model_doc/distilbert) for Sequence Classification model, and a RNN-based Classifier with a Sigmoid activation head for sequence classification. 

To run our pretrained Word2Vec model and evaluation, follow the notebook in [`w2v_pretrained_test.ipynb`](https://github.com/zjohhson/6861Project/blob/main/w2v_pretrained_test.ipynb).

To run our naive Word2Vec and RNN based classifer models and evaluation, follow the notebook in [`w2v_project.ipynb`](https://github.com/zjohhson/6861Project/blob/main/w2v_project.ipynb).

To run our Contextualized Embedding (DistilBERT) model and evaluation, follow the notebook in [`DistilBERT.ipynb`](https://github.com/zjohhson/6861Project/blob/main/DilstilBERT.ipynb).
