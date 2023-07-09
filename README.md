# Tumor-Detetction-from-Brain-MRIs
A CNN program to analyze brain scan images and determine if a tumor is present or not. We take this task as a binary classification image processing task and design a CNN to do the same.

## Dataset
The dataset consists of a directory with 2 sub-directories, yes and no, with them containing scans with tumors and without tumors, respectively.
I have mounted my drive to use the dataset in this notebook.

## Creation of train and validation data
We'll be using tf.keras.utils.image_dataset_from_directory to create train and validation datasets with inferred labels, set image size and batch size, and label mode as binary as well.

## Building our model
We'll be building our own custom model, with rescaling layer as input for our images(along with a defined inout shape), 2D convolutional layers and 2D pooling layers, along with Dense and Dropout layers. A final Dense layer with 1 neuron with a sigmoid activation function is used

## Fitting our model
We now compile our model with optimiser, loss and metrics set, along with callbacks in fitting process. We then fit our model for 30 epochs(availability of big computational sources can provide the possibility to explore much higher epoch values in fitting process)

Note : We cache our train and validation data using AUTOTUNE sized buffers to make the data steps of our model fitting faster by keeping the data present in cache memory. We also shuffle our train dataset to increase the integrity of our model training process

## Plot loss and accuracy values throughout the epochs
We now plot the loss values and accuracy values across the epochs to analyse the trend of the CNN's working and learning throughout the fitting process

## Analysing model efficiency
We then unbatch our validation data, make predictions in the form of probabilities and predicted class values, compare the two to find model efficiency via 2 popular metrics ( accuracy and F1 score), along with finding false positive and false negative percentage.

Then, we plot the confusion matrix for the given model's performance and obtain the classification report for good measure

We report an accuracy of 86% and an F1 score of 90%, which is satisfactory for a model of the level of simplicity and computational complexity of our's.

## Thank you
### By : Karthik Sabareesh
