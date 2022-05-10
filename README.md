# Dog Breed Classifier
This is the capstone project for Udacity’s Data Scientist Nanodegree Program

### Table of Contents
1. [Project Overview](#overview)
2. [Requirements](#dependency)
3. [Instructions](#instructions)
4. [File Descriptions](#desc)
5. [Project Workflow](#analysis)
6. [Results](#results)
7. [Conclusion](#conc)
8. [Tips for improvements](#improve)
9. [Licensing, Authors, and Acknowledgements](#licensing)


## Project Overview<a name="overview"></a>
The project is an end-to-end deep learning pipeline to process real-world, user-supplied images. The pipeline accepts any user-supplied image as input and predicts whether a dog or human is present in the image. If a dog is detected in the image, it returns an estimate of the dog’s breed. If a human is detected, it returns an estimate of the dog breed that is most resembling.

## Requirements<a name="dependency"></a>
The libraries required to run this project are in the requirements folder.

## Instructions<a name="instructions"></a>
1. Clone this github repository.
2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).
3. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).

## File Descriptions<a name="desc"></a>
1. The haarcascades folder contains the pre-trained weights in the xml file format. This is used with the OpenCv face detector class. 
2. The images folder contains the sample images that are used to test the predictions.
3. The extract_bottleneck_features.py file contains the code to use pre-trained imagenet models for transfer learning.
4. The dog_app.ipynb file is the main file for this project. It is a jupyter notebook containing code of face detector, dog detector and dog breed classifier models and also the final algorithm that uses all these three models to make predictions.

## Project Workflow<a name="analysis"></a>
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
In this project, we utilized several methods for developing a dog breed identification app.

Building a CNN from scratch using Keras may have been simple, but it clearly was not effective, only classifying one percent of test images correctly. With CNN transfer learning, we almost obtained an accuracy of 84% in our testing set. I have done many experiments regarding combinations of parameters. The majority of them are disappointing, but this is how machine learning works. Finding the right architecture for the right model is very important but it takes a lot of practice and experience to get a better sense of using the architecture in different scenarios.

Taking into account that there are breeds that are virtually identical and the existence of sub-breeds, also the possibility of some images being either blurred or having too much noise, I think the result is satisfying as a first attempt.

## Tips for improvements<a name="improve"></a>
1. Use data augmentation to fix orientation, color adjustment, size issues, and other quality of images issues.
2. Try different optimization algorithms and batch sizes.
3. Handling multiple humans or dogs in an image and also a mix of humans and dogs in the image.

## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Credit to Udacity for the data and python 3 notebook.
