# Latent Semantic Analysis

[Python App](https://github.com/doubleyip/TensorflowProject)

### About the Latent Semantic Analysis Project

Latent Semantic Analysis is the mapping of words to numbers in an attempt for computers to "understand" human languages.
The Latent Semantic Analysis app takes 2 sentences and determines how close they are in meaning. It returns a value between 
0 and 1 where 0 is most similar and 1 is least similar.

### How does the Latent Semantic Analysis App work?

The app uses Google's [Tensorflow](https://www.tensorflow.org/) framework to train a model using corpus. 
I used the Word2Vec module found [here](https://www.tensorflow.org/) which created word embeddings using text represented by vectors of numbers.
Word2Vec then uses training techniques such as RNN (Recurrent Neural Network) to calculate similarities between
words. This is done in layers where after the next layer is calculated, all previous layers are slightly adjusted 
using back propogation. These values are then plotted on a chart where words with similar meanings are often near each other.
Generally, having more steps in the training will results in more "accurate" models. However, the training will eventually become overfitted
if there are too many steps.

###### Embedding plot after 10,000 steps
<img src="/images/10ksteps.png" width="50%" height="50%">


###### Embedding plot after 100,000 steps
<img src="/images/100ksteps.png" width="50%" height="50%">

Once the model is trained, the app takes two sentence and splits them into words. It then tries to find the word on the plot and measures the distance
between that word and the next word and adds that value to a vector. If the word is not found in the model, the default plot point will be 0,0. 
The app then calculates the cosine difference between the two sentence vectors and outputs a value between 0 and 1 where the closer the value is to 0,
the more similar the sentences are. For example, two exact sentences will result in a difference value of 0.

###### Example sentence of 2 similar sentences

<img src="/images/lsaexample.png" width="75%" height="75%">

### How to use the Latent Semantic Analysis App

Clone the repository [here](https://github.com/doubleyip/TensorflowProject) and run the word2vec.py file.
