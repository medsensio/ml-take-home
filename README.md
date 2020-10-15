

# Introduction

This document describes the take-home assignment for the machine learning position. 
The goal is to train a model that can **classify abnormal lung sounds in short audio clips**. Most of Medsensio's machine learning projects are based on audio data and the take-home assignment is therefore related to what Medsensio does on a day to day basis. 

The data in this take-home assignment is from an open-access research database, and there are several versions of this datasets available today. We have anonymized it and made several changes to make it simpler to develop a machine learning problem around it.

# Description

The goal of the assignment is to train a model that can classify abnormal lung sounds in short audio clips. In short you will need to perform several steps:

 - **Read audio data into memory.** Data cleaning might be necessary. Source data is not of the highest quality, do not hesitate to remove data from the training set.
 - **Features engineering and selection**. What are the inputs to the model? If you are coming from a computer vision background, using [spectrograms](https://en.wikipedia.org/wiki/Spectrogram) is an easy way to turn the audio data into a computer vision task.
 - **Develop a cross-validation strategy**. How to make sure the model is not overfitting?
 - **Choose a method**. Deep learning, Hidden Markov Model, support vector machine or maybe random forests?
 - **Training procedure.** Which hyperparameters? 

Training could be time-consuming, we are therefore not concerned about the accuracy/performance of the model. **Don't spend time on tuning hyperparameters or training the model for optimal performance.** We are interested in how you approach ML problems and how you set up the experiments, using unique or untraditional techniques are encouraged.

If you do need a GPU, but don't have access to one. You can use available notebooks on [kaggle notebooks](https://www.kaggle.com/notebooks). 
There is no requirement to what kind of method/model you choose to use.

## Data
The data is available at this link: [training data](https://drive.google.com/file/d/1-QxacNGlcPily4HR2AfmScqr50QbCi2o/view?usp=sharing)
The size is around 2GB and the total amount of files is 5500.
The data consist of a folder called *train* with consists of short audio clips. The format is .wav using 16 PCM bit format.

A file with annotations is included named *train.csv*.
You will see that there are three categories of lung sounds *normal*, *wheeze*, *crackle*. *Wheeze* and *crackle* are both abnormal sounds and can be present at the same time, however, they can not be present at the same time as the *normal* class.

# Requirements

- Code should be runnable in a reproducible environment. Use docker container, or [kaggle notebooks](https://www.kaggle.com/notebooks)
- Code should be commented and documented.
- You need to use a cross-validation strategy.
- The model should predict one or more *classes* for each audio clip. 
- Deliver result as a git repo on a remote hosting platform, or as a zipped folder with code.