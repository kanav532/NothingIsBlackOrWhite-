![](img/Presentation0.jpg)

![](img/Presentation1.png)

# Nothing’s Black or White

# Team 70

![](img/Presentation2.png)

# Slide 1

PROBLEM

![](img/Presentation3.png)

![](img/Presentation4.png)

![](img/Presentation5.png)

# The Problem

# We Are Limited By Grayscale Images

![](img/Presentation6.png)

# Current Solutions are Unsatisfactory

![](img/Presentation7.png)

# Goal

![](img/Presentation8.png)

![](img/Presentation9.png)

![](img/Presentation10.jpg)

![](img/Presentation11.png)

# Nuances That Increase Difficulty

![](img/Presentation12.png)

<span style="color:#FF6E00">Orange</span>  and  <span style="color:#0FE84A">Light Green </span> have the  __Same Grayscale __ and  __Same Shape__

# Data Processing

# Data

![](img/Presentation13.png)

# Data Splits

30000

RGB IMAGES

# Practical Testing Images

# Data Cleaning

![](img/Presentation14.png)

# Data Pipeline

![](img/Presentation15.png)

# Practical Images May Not Be Real Color

![](img/Presentation16.png)

<span style="color:#F03F2B">Manually Colorized</span>

![](img/Presentation17.jpg)

![](img/Presentation18.jpg)

![](img/Presentation19.jpg)

![](img/Presentation20.png)

![](img/Presentation21.jpg)

# Baseline Modelregression Based Model

# Starter Baseline Model

![](img/Presentation22.png)

A regression\-based CNN Model altered to only take in greyscale inputs\.

![](img/Presentation23.png)

# Results

![](img/Presentation24.png)

Decent results\! A good starter But definitely lots of scope for improvement\.

Avg Loss for training : 0\.0017

Avg Loss for validation : 0\.0035

![](img/Presentation25.png)

![](img/Presentation26.png)

![](img/Presentation27.png)

# Initial ModelClassification Based Model

# Scoping & Defining our Problem

![](img/Presentation28.png)

We will scope the task of image colourization into a pixel\-wise classification task

We label each pixel with one of 24 colours

The 24 colours are selected using [k\-means clustering](https://en.wikipedia.org/wiki/K-means_clustering) over colours\, and selecting cluster centers

Given a grayscale image\, predict each pixel as a color amongst the 24 colors

![](img/Presentation29.png)

![](img/Presentation30.png)

# Dataset & Constraints 

 CIFAR-10, which has images of small dimensions 32*32 pixels

We just focus on the “horse” category of the dataset 
Furthermore, the error is calculated by defining distances over RGB space.

# Model Architecture

![](img/Presentation31.png)

![](img/Presentation32.png)

* The architecture we use is U\-NET
* This architecture has following additions over a more basic CNN architecture:
  * Strided & Transposed Convolutions instead of upsampling
  * functions
  * Skip connections

![](img/Presentation33.png)

# Results & Discussion

![](img/Presentation34.png)

![](img/Presentation35.png)

![](img/Presentation36.png)

![](img/Presentation37.png)

![](img/Presentation38.png)

# Final modelGenerative Adversarial Network

# GAN Architecture Overview

![](img/Presentation39.png)

Generator tries to “trick” the Discriminator as they compete and train in parallel

![](img/Presentation40.png)

Convolutional Layers/Deconvolutional layers connected via skip net connections

![](img/Presentation41.png)

# GAN Architecture - Generator

![](img/Presentation42.png)

![](img/Presentation43.png)

* 5 Convolutional Blocks
  * Conv2d
  * BatchNorm2d
  * ReLU
* 5 Deconvolutional Blocks
  * ConvTranspose2D
  * BatchNorm2D
  * ReLU
* Tanh activation Function

# GAN Architecture - Discriminator

![](img/Presentation44.png)

![](img/Presentation45.png)

* 6 Convolutional Blocks
  * Conv2d
  * BatchNorm2d
  * ReLU
* 1 Fully Connected Layer
* Sigmoid Activation

# GAN Results

![](img/Presentation46.png)

![](img/Presentation47.png)

![](img/Presentation48.png)

![](img/Presentation49.png)

![](img/Presentation50.png)

![](img/Presentation51.png)

![](img/Presentation52.png)

# GAN Discussion

![](img/Presentation53.png)

* GAN has abnormal loss graphs
  * Competition between models induces settling at value instead of typical trends
* Qualitative results are best for determining success rate of model
  * Difficult to quantify
* Colors not as vibrant and some incorrect coloring found
  * Could be due to shorter training period/training size

![](img/Presentation54.png)

# Using AI to do this!

# Demonstration

# 

![](img/Presentation55.png)

![](img/Presentation56.png)

# Conclusion

Any questions ?

