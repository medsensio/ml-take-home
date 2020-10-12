
# Introduction

The goal of this task is to train a model that will be able to predict lung sounds. We are using open and accessible data, but have modified it for this task. Since we are working with audio data and lung sounds, the task is closely related to what Medsensio does on a day to day basis. The goal is to set up the experiment and start training a model. Training could take a long time, we are therefore not concerned about the accuracy/quality of the model. We are much more concerned and interested in how you set up the experiment and you are encouraged to try unique or new approaches that do not necessarily have the highest predictive power.

If you do need a GPU, but don't have access to one. You can use available notebooks on [kaggle notebooks](https://www.kaggle.com/notebooks). 
There is no requirement to what kind of method/model you choose to use.

# General tips
Some data cleaning might be necessary. The source of the data is not of the highest quality, do not hesitate to remove data from the training set.
If you are coming from a computer vision background, using [spectrograms](https://en.wikipedia.org/wiki/Spectrogram) is an easy way to turn the problem into a computer vision task.


## Data
The data is available at this link: [training data](https://drive.google.com/file/d/1-QxacNGlcPily4HR2AfmScqr50QbCi2o/view?usp=sharing)
The size is around 2GB and the total amount of files is 5500.
The data consist of a folder called *train* which consists of short audio clips. 
Audio data is using the format of .wav using 16 PCM bit format.

A file with annotations is included named *train.csv*.
You will see that there are three categories of lung sounds *normal*, *wheeze*, *crackle*. *Wheeze* and *crackle* are both abnormal sounds an can be present at the same time, however, they can not be present at the same time as the *normal* class.


# Requirements:

- Code should be runnable in a reproducible environment. Use docker container, or [kaggle notebooks](https://www.kaggle.com/notebooks)
- Code should be commented and documented thoroughly.
- You need to use cross-validation strategy.
- Code should produce model weights that can be exported to a production environment.
- The model should predict one or more labels for each lung sounds. 