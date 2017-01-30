---
layout: post
title:  "How to install Kensor with TF backend on Windows with python"
date:   2017-01-30 16:16:01 +0000
categories: tutorial
tags : [keras, tensorflow, tutorial, installation, windows, python]
---
{% include JB/setup %}

# Overview
Believe me, I have wasted hours on this problem. You will probably be best off using Anaconda. You can find all the details here:
<a href="https://github.com/tensorflow/tensorFlow/blob/master/tensorflow/g3doc/get_started/os_setup.md">TF installation guide</a> <br>
Keras itself should already be packed inside Anaconda, if not use (source: <a href="https://anaconda.org/conda-forge/keras">here</a>):<br>
`conda install -c conda-forge keras=1.0.7` <br>


But.. If you do not want to install Anaconda, for whatever reason, this is a guide for you!

# Install pywin
What it is - sourceforge project site: <a href="https://sourceforge.net/projects/pywin32/">Pywin</a><br>
Get a suitable version from here (for your python version and Windows version): <a href="https://sourceforge.net/projects/pywin32/files/pywin32/Build%20220/">Builds</a>


Follow installation instructions. After it finishes, basically in that folder you have a separate python interpreter with already installed various libraries for calculations!
You can update libraries using:

`<path to pywin>\python.exe -m pip install --upgrade keras`


# Install tensorflow
`<path to pywin>\python.exe -m pip install tensorflow-gpu`

# Check installation.
Run your favourite IDE and try these imports:
{% highlight python %}
import keras
import tensorflow
import scipy
import numpy
import pandas
{% endhighlight %}

# Try a simple project!
Here - this one should work! <br>
{% post_url 2017-01-30-Simple-net-Keras-TF %}