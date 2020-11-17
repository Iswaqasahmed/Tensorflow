### The IMDB dataset:
We’ll work with the IMDB dataset: a set of `50,000` highly polarized reviews from the
Internet Movie Database. They’re split into 25,000 reviews for training and 25,000
reviews for testing, each set consisting of *50%* *negative* and *50%* positive reviews.
Why use separate training and test sets? Because you should never test a machinelearning
model on the same data that you used to train it! Just because a model performs
well on its training data doesn’t mean it will perform well on data it has never
seen; and what you care about is your model’s performance on new data (because you
already know the labels of your training data—obviously you don’t need your model
to predict those). For instance, it’s possible that your model could end up merely memorizing
a mapping between your training samples and their targets, which would be
useless for the task of predicting targets for data the model has never seen before.
We’ll go over this point in much more detail in the next chapter.
Just like the MNIST dataset, the IMDB dataset comes packaged with Keras. It has
already been preprocessed: the reviews (sequences of words) have been turned into
sequences of integers, where each integer stands for a specific word in a dictionary.
The following code will load the dataset (when you run it the first time, about
80 MB of data will be downloaded to your machine).
