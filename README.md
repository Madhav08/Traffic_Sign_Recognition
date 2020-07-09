# Build a Traffic Sign Recognition Project

The goals / steps of this project are the following:
* Load the data set：[German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset)
* Explore, summarize and visualize the data set
* Design, train and test a Convonlutional Neural Network model architecture
* Use the model to make predictions on new images
* Analyze the softmax probabilities of the new images

## Data Set Summary & Exploration

I  calculate summary statistics of the traffic signs data set:

* The size of training set is 31367
* The size of the validation set is 7842
* The size of test set is 12630
* The shape of a traffic sign image is 32x32x3
* The number of unique classes/labels in the data set is 43

## Design and Test a Model Architecture

### 1. Preprocess the image data.

‘Train’ folder contains 43 folders each representing a different class. The range of the folder is from 0 to 42. With the help of the OS module, we iterate over all the classes and append images and their respective labels in the data and labels list.

The PIL library is used to open image content into an array.

Finally, I have stored all the images and their labels into lists (data and labels).

We need to convert the list into numpy arrays for feeding to the model.

The shape of data is (39209, 30, 30, 3) which means that there are 39,209 images of size 30×30 pixels and the last 3 means the data contains colored images (RGB value).

With the sklearn package, we use the train_test_split() method to split training and testing data.

From the keras.utils package, we use to_categorical method to convert the labels present in y_train and t_test into one-hot encoding.

* The shape of a processed traffic sign image is 30x30x3

 
### 2. Model results

My final model results were:
* validation set accuracy of 98.10% 
* test set accuracy of 94.33%
