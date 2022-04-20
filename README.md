# Dog Breed Classifier
`The capstone project for Udacity’s Data Scientist Nanodegree Program`

### Table of Contents
1. [Project Overview](#overview)
2. [List of Dependencies](#dependency)
10. [Instructions to use the repository](#instructions)
11. [File Descriptions](#desc)
12. [Results](#results)
13. [Conclusion](#conc)
14. [Tips to improve the performance](#improve)
15. [Licensing, Authors, and Acknowledgements](#licensing)


## Project Overview<a name="overview"></a>
In this project, I have implemented an `end-to-end deep learning pipeline` to process real-world, user-supplied images. The pipeline will accept any user-supplied image as input and will predict whether a dog or human is present in the image. If a dog is detected in the image, it will provide an estimate of the dog’s breed. If a human is detected, it will provide an estimate of the dog breed that is most resembling. 

## List of Dependencies<a name="dependency"></a>
The `requirements folder` list all the libraries/dependencies required to run this project.

## Instructions to use the repository<a name="instructions"></a>
1. Clone this github repository.

2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip the folder and prepare image label pairs for training the model.

3. Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip). Unzip the folder and prepare images for the face detector model.

## File Descriptions<a name="desc"></a>
1. The `haarcascades folder` contains the pre-trained weights in the `xml file format` to use with the OpenCv face detector class that has been used in this project. 

2. The `images folder` contains the sample images that are used to test the predictions of the final algorithm in this project.

3. The `extract_bottleneck_features.py file` contains the code to use pre-trained imagenet models as **feature extractors** for transfer learning.

4. The `dog_app.ipynb file` is the main file for this project. It is a jupyter notebook containing code of face detector, dog detector and dog breed classifier models. The final algorithm that uses all these three models to make predictions is also implemented in this notebook.

## Project workflow<a name="analysis"></a>
The basic steps for making this pipeline were:
1. Import and explore the dog and human datasets
2. Create a human face detector using OpenCV
3. Create a dog detector using Resnet50
4. Create a CNN to classify dog breeds using Keras and evaluate model performance
5. Use Transfer Learning to improve the initial CNN and evaluate model performance
6. Write an algorithm to test new images

## Post with the results<a name="results"></a>
The step by step explanation of the project can be found at the post available [here](https://medium.com/@psiodoros/dog-breed-classification-using-cnns-b065913527c).

## Conclusion<a name="conc"></a>
This project serves as a good starting point to enter into the domain of deep learning. Data exploration and visualizations are extremely important before training any Machine Learning model as it helps in choosing a suitable performance metric for evaluating the model. CNN models in Keras need image data in the form of a 4D tensor. All images need to be reshaped into the same shape for training the CNN models in batch. 

Building CNN models from scratch is extremely simple in Keras. But training CNN models from scratch is computationally expensive and time-consuming. There are many pre-trained models available in Keras (trained on ImageNet dataset) that can be used for transfer learning.

The most interesting thing to note is the power of transfer learning to achieve good results with small computation. It works well when the task is similar to the task on which the pre-trained model weights are optimized.


## Tips to improve the performance<a name="improve"></a>
1. Using data augmentation.
2. Implementing a method to handle multiple humans or dogs in an image.
3. Handling a mix of humans and dogs in the image.









## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Must give credit to Udacity for the data and python 3 notebook.




