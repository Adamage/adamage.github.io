---
layout: post
title:  "How to setup CNTK with Visual Studio"
date:   2017-02-02 16:16:01 +0000
categories: tutorial
tags : [CNTK, C#, tutorial, installation, windows]
---
{% include JB/setup %}

# Overview.
In this tutorial we will go through the process on installing Microsoft CNTK, creating a Visual Studio solution and using the CNTK nuget package to access CNTK binaries.<br>
Then, we will write a small tester program to check if it's configured properly.

# Install CNTK.
For an extensive instruction guide please refer to <a href="https://github.com/Microsoft/CNTK/wiki/Setup-CNTK-on-Windows">CNTK github</a> page.<br>
Supported OS and libraries combinations: <a href="https://github.com/Microsoft/CNTK/wiki/Test-Configurations">Test Configurations</a><br>
Reference guide for setting up environmental variables: <a href="https://github.com/Microsoft/CNTK/wiki/Windows-Environment-Variables">Environment-Variables</a><br>
Visual Studio requirements:<br>
'Visual Studio 2015+, Community Edition+'<br>`Common Visual Tools for Visual C++ 2015<br>
Other requirements: see first link.<br><br>

Manual installation for windows using binary distribution <a href="https://github.com/Microsoft/CNTK/wiki/Setup-Windows-Binary-Manual">guide</a>:<br>
`Visual C++ Redistributable Package for Visual Studio 2015`<br>
`Microsoft MPI Version 7 (7.0.12437.6)`<br>

GPU drivers on <a href="http://www.nvidia.com/Download/index.aspx?lang=en-us">NVIDIA page</a><br>

Download a release binary from <a href="https://github.com/Microsoft/CNTK/releases">here</a>:<br>
`CNTK for Windows v.2.0 Beta 10 GPU with 1bit-SGD`<br>

# Run test examples using python.
`cntk\Tutorials\NumpyInterop<br>python FeedForwardNet.py`

# Run test examples using brainscript.
`cd \CNTK\Tutorials\HelloWorld-LogisticRegression<br>
cntk configFile=lr_bs.cntk makeMode=false command=Train`

# Try a simple project!
Here - this one should work! <br>
<a href="https://adamage.github.io/tutorial/2017/02/02/Simple-CNTK-brainscript">Simple logistic regression with CNTK</a>