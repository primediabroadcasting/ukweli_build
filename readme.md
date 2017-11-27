# Building Ukweli

On the 21st and 22nd of November, a team from [EWN](http://ewn.co.za) took part in the [Editors Lab](https://www.globaleditorsnetwork.org/programmes/editors-lab/media-indaba-editors-lab/) hackathon.  The demo worked, but the code was not something we were terribly proud of.  This repo is a sane rebuild of the code so that we can share it.

Under the hood we are doing three things:

1. Doing a document similarity match against a corpus of known hoax messages
1. Using a machine learning model, trained on a corpus of spam SMS messages, to determine if your document has any similarity to SMS spam
1. Using a machine learning model, trained on a corpus of fake news articles, to determine if your document has any similarity to fake news

The plan is:

 - Strip the code back to the minimum, removing any modules that we can do without
 - Test different machine learning models (currently we are using a [Keras](https://keras.io) implementation of [fastText](https://arxiv.org/pdf/1607.01759.pdf) and a [Naive Bayes](http://scikit-learn.org/stable/modules/naive_bayes.html) model)
 - Test different options of feature extraction and engineering
 - Hyperparameter tuning on the selected models