# Deep_Learning_Project
<font color="magenta"> Sri : **OVERVIEW OF THE ASSIGNMENT**

<font color="magenta">**Objective**: Create a deep learning model that can detect the species of the birds from an image.

<font color="magenta">**Data Description** : The data set is sourced from Kaggle : https://www.kaggle.com/gpiosenka/100-bird-species
It is a collection of 230 bird species with 32,035 training images, 1,150 test images and 1150 validation images.
The images are 224 X 224 X 3 size and in jpg color format.
The data is already divided into test, train and validation data and there is also consolidated folder with all of the images in one. For my asssignment, I used the pre-divided test, train and validation data and used the consolidated dataset for displaying images as a part of EDA.

<font color="magenta">**Summary of Methods and Model** : I started with loading the dataset from kaggle into google colab by using the dataset's API and kaggle.json files. The dataset was in a zipped folder and after unzipping it, we can see that the data is already divided into test , train and validation data.
Once the data is ready for use, the data directories have been specified, normalized the pixels in the images, and moved the images from the directories to the model using the flow_from_directory function.

<font color="magenta"> I've used ResNet101V2 , which is one of the most popular Residual Neural networks. This is a type of an ANN that works by skipping some layers, and is implemented using Relu activations and batch normalizations in between. I also added dropout layers to improve the accuracy.
Reference : https://www.tensorflow.org/api_docs/python/tf/keras/applications/ResNet101V2
https://en.wikipedia.org/wiki/Residual_neural_network

<font color="magenta">**Analysis of the results** : The accuracy recieved is about 97% on the final test data, which is a good number. The model ran for about 31 minutes with 10 epochs. I think with a higher number of epochs, a better accuracy can be obtained. Specifically because, the accuracy is higher than the validation accuracy, which also indicates that the model is not overfitting. Tried out Data Augmentation, and although the accuracy was slightly higher, the runtime was the same as without the data augmentation model.
