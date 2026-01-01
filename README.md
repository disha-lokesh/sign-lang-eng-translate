*Real-Time Sign Language Translator*
Overview

This project is a computer vision–based real-time sign language translator designed to bridge the communication gap between sign language users and non-signers. It recognizes hand gestures using a webcam and converts them into readable text in real time.

Problem Statement

Communication between sign language users and non-signers is limited due to the lack of accessible and real-time translation tools that work with standard cameras and devices.

Solution

A real-time sign language recognition system built using computer vision and deep learning that detects hand landmarks, classifies gestures, and displays the corresponding text output.

Dataset Used

Dataset Name: ASL Alphabet Dataset

Source: Kaggle

Link: https://www.kaggle.com/datasets/grassknoted/asl-alphabet

Only hand landmark coordinates extracted using MediaPipe are used for training (raw images are not included in this repository).

Technologies Used
Computer Vision

OpenCV

MediaPipe Hands (21 hand landmarks)

Deep Learning

TensorFlow / Keras

Multilayer Perceptron (MLP)

Programming Language

Python 3

Model Architecture

Input: 63 features (21 hand landmarks × x, y, z)

Fully Connected (Dense) Layers

ReLU activation

Softmax output layer for classification

Optimizer: Adam

Loss Function: Categorical Crossentropy

Evaluation Metrics

Classification Accuracy

Real-time prediction consistency during webcam inference

Project Structure
sign-language-translator/
│
├── scripts/
│   ├── collect_data.py
│   ├── extract_landmarks.py
│   ├── train_model.py
│   └── real_time_translate.py
│
├── utils/
│   └── mediapipe_utils.py
│
├── models/
│   └── sign_model.h5
│
├── dataset/
│   └── README.md
│
├── requirements.txt
├── README.md
