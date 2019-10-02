# emotionClassification
# Emotion Detection from audio based data using Convolutional Neural Networks (CNNs)

### List of contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Working](#working)
- [Installation](#installation)
- [Running](#running)


## Introduction
---
[(Back to top)](#list-of-contents)

This project deals with multiclass classification problem of classifying the emotions from audio clips using Convolutional Neural Networks. It classifies the audio into 10 labels namely :
- female_sad
- female_angry
- female_happy
- female_fearful
- female_calm
- male_sad
- male_angry
- male_happy
- male_fearful
- male_calm

### Following is a distribution of class labels for the problem at hand.
 
 ![img](https://imgur.com/Y0JCMIC.jpg)
 
 ## Dataset
 ---
[(Back to top)](#list-of-contents)

Dataset used is : [The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)](https://zenodo.org/record/1188976)
It contains audio data as well as video+audio data for the task of emotion classification. We will be using audio only data from the dataset mentioned above. 
 
 
## Working
---
[(Back to top)](#list-of-contents)

The step-by-step procedure of the Project:

+ Collection and Understanding of dataset from the link mentioned above;
+ Extraction of MFCCs (state-of-the-art feature for speech recognition) using librosa library. The MFCC coefficients extracted will then be passed to CNN (These features will act as a feature vector same as a vector of pixels passed in case of computer vision tasks.)
+ Data Augmentation applied to audio clips to enhance the quality. Important augmentation techniques used are: Pitch change, Stretching, Adding noise etc. These are done to make our model robust to any kind of audio.
+ Training the Convolutional Neural Network for multiclasification task.
+ Testing on an audio file.


NOTE : The whole Machine Learning pipeline is implemented in the jupyter environment.
 

## Installation
---
[(Back to top)](#list-of-contents)

Following Python Libraries need to be installed for the successful completion of project.
- [Librosa](https://librosa.github.io/librosa/)
- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://numpy.org/)
- [Keras](https://keras.io/)
- [Tensorflow](https://www.tensorflow.org/)

Install above required packages using pip or any other method.

Note : You can simply use Google Colab which already has configured environment!

## Running

- Plotting of Spectogram (Unique for a particular audio clip!).

![img](https://imgur.com/6vPfSQ9.jpg)

- Extraction of MFCC for a particular audio clip using Librosa library.

![img](https://imgur.com/gPsmpwp.jpg)

- Passing the MFCC coefficients (different for different audio clips) in batches of 8 to a convolutional Neural Network having a standard architecture that most of the classification tasks have.

- Testing on an audio file

![img](https://imgur.com/QkKqPSp.jpg)
