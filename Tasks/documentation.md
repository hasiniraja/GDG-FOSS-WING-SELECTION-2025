  TensorFlow

## What is TensorFlow?
TensorFlow is an open-source machine learning and deep learning framework developed by Google. It provides an ecosystem of tools, libraries, and community resources for building, training, and deploying machine learning models.TensorFlow supports execution on CPUs, GPUs, and TPUs, making it suitable for every type of project.
TensorFlow.js is an open-source web ML library that can run anywhere JavaScript can. We use TensorFlow.js to create new machine learning models and deploy existing models with JavaScript.It helps us to deploy a production-ready ML pipeline for training.TensorFlow offers multiple data tools to help clean and preprocess data at scale.

## Explore these fields!
 Before you dive into the world of tensorflow you need to know the core of Machine learning concepts and the basics of deep learning concepts(neural network principles)
 To get started you can read about the various models that are pretrained from the website https://www.tensorflow.org/hub

# Upgrade pip first
pip install --upgrade pip

# Install TensorFlow (CPU)
pip install tensorflow

# Install TensorFlow with GPU support (Linux / WSL2)
pip install tensorflow[and-cuda]

# Try the preview (unstable) build
pip install tf-nightly

It is highly recommended to create and work inside a virtual environment (venv or conda) to avoid conflicts with other Python packages.
I want to share another important resource- https://arsanatl.medium.com/how-to-setup-tensorflow-2-3-1-cpu-gpu-windows-10-e000e7811e2b, It helps us to setup TensorFlow 2.3.1 — CPU/GPU (Windows 10)  in a simple way.

and also the  TensorFlow tutorials are written as Jupyter notebooks and run directly in Google Colab that is a hosted notebook environment that requires no setup.

## Why this Exists ?
Whether you're an expert or a beginner, TensorFlow is an end-to-end platform that makes it easy for you to build and deploy ML models.
We can build and train models by using the high-level Keras API, which makes getting started with TensorFlow and machine learning easy.
We can train and deploy models in JavaScript environments using TensorFlow.js.

## How to dive deeper?
-First we need to define and train neural networks using high-level APIs like Keras.(good for beginners)
-secondly perform some data preprocessing and pipeline management tasks.
-Export models for deployment on servers, mobile, or edge devices.
-Use TensorFlow Extended (TFX) for end-to-end ML workflows.

## Where is this used?
TensorFlow can train and run deep neural networks for:
-handwritten digit classification
-image recognition
-word embeddings
-recurrent neural networks
-sequence-to-sequence models for machine translation
-natural language processing

## Worth a read !
 Created and maintained by Google, TensorFlow is an open source library for numerical computation and large-scale machine learning. It was released as open-source software in November 2015, and has since become one of the most popular frameworks for machine learning and deep learning projects.

The single biggest benefit TensorFlow provides for machine learning development is abstraction.Instead of dealing with the tiny details of implementing algorithms, developer can focus clearly on the overall logic of the application. Tensorflow will take care of all those details behind the scenes. 

Mainly it provides a cross-platform deployment on cloud,web or mobile. We can get scalable performance with multi-gpu and tpu support.
I hope this helps.