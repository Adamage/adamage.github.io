---
layout: post
title:  "TensorFlow net with MNIST - digit recognizer"
date:   2017-01-31 16:16:01 +0000
categories: tutorial
tags : [tensorflow, tutorial, python, MNIST, image data]
---
{% include JB/setup %}

# Overview
This tutorial covers defining and training a neural net to recognize hand-written digits. We will use the popular, classic data-set MNIST.<br>
Also, it is loosely based on an already existing <a href="https://www.kaggle.com/kakauandme/digit-recognizer/tensorflow-deep-nn">Kaggle tutorial </a> by Kirill Kliavin.<br>
What I am aiming for is to create a tutorial with lower entry level, even if you do not know any of the AI lingo.<br>

You can find the full implementation on my github:<br>
<a href="https://github.com/Adamage/neural-nets-tutorials/tree/master/tensorflow/images/digit_recognizer_mnist">Digit Recognizer with Tensorflow </a> <br>

# Obtain data.
You can download the data set from here:<b>
<a href="https://www.kaggle.com/c/digit-recognizer/data">Kaggle Digit Recognizer competition</a>

# Imports.
Make sure you have all those libraries installed:
{% highlight python %}
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import matplotlib.cm as cm
import tensorflow as tf
{% endhighlight %}

# Helper tools.
You can just copy paste it right after imports.
{% highlight python %}
class Tools:
    @staticmethod
    def display(image, width, height):
        image = image.reshape(width, height)
        plt.imshow(image, cmap=cm.get_cmap("binary"))

    @staticmethod
    def dense_to_hot(labels_dense, num_classes):
        num_labels = labels_dense.shape[0]
        index_offset = np.arange(num_labels) * num_classes
        labels_one_hot = np.zeros((num_labels, num_classes))
        labels_one_hot.flat[index_offset + labels_dense.ravel()] = 1
        return labels_one_hot

    @staticmethod
    def weight_variable(shape):
        initial = tf.truncated_normal(shape, stddev=0.1)
        return tf.Variable(initial)

    @staticmethod
    def bias_variable(shape):
        initial = tf.constant(0.1, shape=shape)
        return tf.Variable(initial)

    @staticmethod
    def convolution2d(x, w):
        return tf.nn.conv2d(x, w, strides=[1,1,1,1], padding='SAME')

    @staticmethod
    def max_pool_2x2(x):
        return tf.nn.max_pool(x, ksize=[1,2,2,1], strides=[1,2,2,1], padding='SAME')
{% endhighlight %}

# Define hyperparameters.
We can tweak them later.
{% highlight python %}
LEARNING_RATE = 1e-4
TRAINING_ITERATIONS = 1000
DROPOUT = 0.5
BATCH_SIZE = 50
VALIDATION_SIZE = 2000
IMAGE_TO_DISPLAY = 10
{% endhighlight %}

# Pre-process data.
Store training data in memory.
{% highlight python %}
data = pd.read_csv('../input/train.csv')
{% endhighlight %}

Allocate values, convert to float and normalize.
{% highlight python %}
images = data.iloc[:,1:].values
images = images.astype(np.float)
images = np.multiply(images, 1.0 / 255.0)
{% endhighlight %}

{% highlight python %}
{% endhighlight %}
# Construct layers of Artificial Neural Net.

# Train.

# Save model.

# Print confusion matrix.

# But what does it mean?
`Parameters of our classifier:
-
-
-
`
`Layers
-
-
-`
