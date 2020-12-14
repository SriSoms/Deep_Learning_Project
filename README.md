# Deep_Learning_Project
For Some reason, my markdown comments are not visible once I upload my .ipynb file to github. I have pasted all of my markdown comments below and I have submitted the editable google colab link to the assignment dropbox.


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


<font color="magenta"> Sri : Starting with setting up default display setting
  
 <font color="magenta"> Sri : After installing the autotime, we can see that it prints out the time taken to run each cell at the end of the cell.
  
  <font color="magenta"> Sri : Reference for loading data into google colab from kaggle- https://medium.com/@yvettewu.dw/tutorial-kaggle-api-google-colaboratory-1a054a382de0
  
  <font color="magenta"> Sri : After downloading the data from kaggle as seen above, we will ow unzip the data file below.
  
  <font color="magenta"> Sri : List the data files that have been downlaoded and unzipped. Note that the dataset already has test, train, validation and consolidated data placed into folders
  
  <font color="magenta"> Sri : Importing necessary libraries
  
  <font color="magenta"> Sri : Loading the data from directories
  
  <font color="magenta"> Sri : Re-using rescaling image code from previous assignments
  
  <font color="magenta"> Sri : As seen above, there are 230 categories of bird species and 32,025 images for training 1150 images each for validation and test data.
  
  <font color="magenta"> Sri : Display some of the images with labels.
Refrence : https://www.kaggle.com/piaiai/birds-eda
  
  <font color="magenta"> Sri : Using ResNet101V2
  
  <font color="magenta"> Sri : Trying out Data Augmentation
  
  <font color="magenta"> Sri : Slightly higher accuracy with data augmentation. The run time is the same as the model without data augmentation.
  <font color="magenta"> Sri : Building the model
