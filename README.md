# Dog Breed Classifier
This is the capstone project for Udacity’s Data Scientist Nanodegree Program

### Table of Contents
1. [Project Overview](#overview)
2. [List of Dependencies](#dependency)
3. [Instructions to use the repository](#instructions)
4. [File Descriptions](#desc)
5. [Results](#results)
6. [Conclusion](#conc)
7. [Tips to improve the performance](#improve)
8. [Licensing, Authors, and Acknowledgements](#licensing)


## Project Overview<a name="overview"></a>
The project is an end-to-end deep learning pipeline to process real-world, user-supplied images. The pipeline accepts any user-supplied image as input and predicts whether a dog or human is present in the image. If a dog is detected in the image, it returns an estimate of the dog’s breed. If a human is detected, it returns an estimate of the dog breed that is most resembling.

## List of Dependencies<a name="dependency"></a>
In the requirements folder there are the libraries/dependencies required to run this project.

## Instructions to use the repository<a name="instructions"></a>
1. Clone this github repository.
2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).
3. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).

## File Descriptions<a name="desc"></a>
1. The haarcascades folder contains the pre-trained weights in the xml file format. This is used with the OpenCv face detector class. 
2. The images folder contains the sample images that are used to test the predictions.
3. The extract_bottleneck_features.py file contains the code to use pre-trained imagenet models for transfer learning.
4. The dog_app.ipynb file is the main file for this project. It is a jupyter notebook containing code of face detector, dog detector and dog breed classifier models and also the final algorithm that uses all these three models to make predictions.

## Project workflow<a name="analysis"></a>
The steps for making this pipeline were:
1. Import and explore the dog and human datasets
2. Create a human face detector using OpenCV
3. Create a dog detector using Resnet50
4. Create a CNN to classify dog breeds using Keras and evaluate model performance
5. Use Transfer Learning to improve the initial CNN and evaluate model performance
6. Write an algorithm to test new images

## Post with the results<a name="results"></a>
The step by step explanation of the project can be found at the post available [here](https://medium.com/@psiodoros/dog-breed-classification-using-cnns-b065913527c).

## Conclusion<a name="conc"></a>
This project is a good starting point to start exlpoiting deep learning. Data exploration and visualizations are extremely important before training any Machine Learning model as it helps in choosing a suitable performance metric for evaluating the model. CNN models in Keras need image data in the form of a 4D tensor. All images need to be reshaped into the same shape for training the CNN models in batch. 

Building CNN models from scratch is extremely simple in Keras. But training CNN models from scratch is computationally expensive and time-consuming. There are many pre-trained models available in Keras (trained on ImageNet dataset) that can be used for transfer learning.

The most interesting thing to note is the power of transfer learning to achieve good results with small computation. It works well when the task is similar to the task on which the pre-trained model weights are optimized.

## Tips to improve the performance<a name="improve"></a>
1. Use data augmentation to fix orientation, color adjustment, size issues, and other quality of images issues.
2. Try different optimization algorithms and batch sizes.
3. Handling multiple humans or dogs in an image and also a mix of humans and dogs in the image.

## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Credit to Udacity for the data and python 3 notebook.
