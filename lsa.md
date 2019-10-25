# Latent Semantic Analysis

[Python App](https://github.com/doubleyip/TensorflowProject)

### About the Latent Semantic Analysis Project

Latent Semantic Analysis is the mapping of words to numbers in an attempt for computers to "understand" human languages.
The Latent Semantic Analysis app takes 2 sentences and determines how close they are in meaning. It returns a value between 0 and 1 where 1 is most similar and 0 is least similar.

### How does the Latent Semantic Analysis App work?

The app uses Google's [Tensorflow](https://www.tensorflow.org/) framework to train a model using corpus. 
I used the Word2Vec module which created word embeddings using text represented by vectors of numbers.
Word2Vec then uses training techniques such as RNN (Recurrent Neural Network) to calculate similarities between
words. This is done in layers where after the next layer is calculated, all previous layers are slightly adjusted 
using back propogation. These values are then plotted on a chart where words with similar meanings are often near each other.
The more steps the training takes, the more accurate the embeddings will be.

<img src="/images/10ksteps.png" width="40%" height="40%">
<img src="/images/100ksteps.png" width="40%" height="40%">
