# Labelled Faces in the wild
An exploration of the faces in the wild dataset.
The original dataset can be found [here](http://vis-www.cs.umass.edu/lfw/)
This project implements machine learning concepts such as Principal Component Analysis (PCA) and Support Vector Machine (SVM).

## PRINCIPAL COMPONENT ANALYSIS
The objective of PCA is to perform dimensionality reduction while preserving as much of the randomness in the high-dimensional space as
possible. It is mainly concerned with identifying correlations in the data. We use PCA because many algorithms that work fine in low
dimensions become intractable when the input is high-dimensional. In this project we have restricted the Number of components for PCA to 10.
We first convert our 3 dimensional array to a 2 dimensional array by flattening the array and then fit it to a PCA with n_components = 10.
We then transform our dataset using the given PCA to train our Classifier.

## ClASSIFICATION USING SVM
Once the preprocessing of the dataset is done we can now use a classifier to train it for the given dataset. We chose Support Vector
Machine as our classifier for this project. SVM’s are supervised learning models with associated learning algorithms that analyze data
and recognize patterns. We use a nonlinear support vector classification model with the kernel as radial basis function (rbf). We first
fit the classifier with the data that was transformed using PCA and the labels which were extracted while reading the images in the
directory. To check the predictions on the testing dataset we first take the gray scale value of the face in the image, store in a 2 D
array, flatten the array and then transform it using our PCA which we fitted earlier. Once we get the transformed array we predict the
label for the test image and print it out.

![screenshot](screenshots/faces_in_the_wild)
