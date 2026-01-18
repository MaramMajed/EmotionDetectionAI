### Facial Expression Recognition (FER)


A Convolutional Neural Network (CNN)–based facial expression recognition system built using FER-2013 and extended with RAF-DB for additional emotion classes.


## Project Overview

This repository implements an end-to-end pipeline for facial emotion recognition:

    Dataset ingestion (FER-2013)

    Multi-dataset fusion (FER-2013 + RAF-DB)

    CNN model design and training using TensorFlow/Keras

    Model evaluation and single-image inference in Google Colab

The final model supports 9 emotion classes:

    angry, disgust, fear, happy, sad, surprise, neutral, contempt, confused

## 🧠 Model Architecture

The system uses a lightweight CNN optimized for 48×48 grayscale facial images:


Convolution + ReLU activation


Max pooling layers


Fully connected dense layers


Dropout for regularization


Softmax output layer


This design balances performance and computational efficiency, making it suitable for Colab and low-resource environments.

    All images are converted to grayscale and resized to 48×48

## Installation & Setup (Google Colab)

pip install tensorflow opencv-python-headless pandas kagglehub

Datasets are downloaded directly inside Colab (manually uploaded).

## Training

Image normalization and horizontal flipping are applied

80/20 train-validation split

Optimizer: Adam

Loss function: Categorical Crossentropy

Training duration: 25 epochs

Training Performance (Final Model)

Training Accuracy: ~69%

Validation Accuracy: ~55%

    Note: Performance is limited by class imbalance and label ambiguity across datasets.

## 📊 Evaluation

The trained model is evaluated on the FER-2013 test split using a Keras data generator.

Metrics reported:

Test Loss

Test Accuracy

## 🖼️ Inference (Single Image Prediction)

Users can upload an image in Colab and receive a predicted emotion label:

Steps:

Upload image

Convert to grayscale

Resize to 48×48

Normalize and predict

Output includes:

Predicted emotion label

Visualized input image

## 📚 References

FER-2013 Dataset

RAF-DB Dataset

AffectNet 

# preview
<img width="354" height="261" alt="image" src="https://github.com/user-attachments/assets/05505871-255f-4aa6-a7f4-2ff6e1a8ed25" />

<img width="544" height="513" alt="image" src="https://github.com/user-attachments/assets/004a9af1-f77e-4286-8506-cc9a5cae3d05" />

# FUll project is in Google colab
