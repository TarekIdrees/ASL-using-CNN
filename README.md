# ASL-using-CNN
> American Sign Language (ASL) is a natural language that serves as the predominant sign language of Deaf communities in the United States and most of Anglophone Canada. 

> ASL is a complete and organized visual language that is expressed by facial expression as well as movements and motions with the hands.

> CNN models build on RGB data.
 
# Architecture:
> Model 1

- Convolution : [filters = 16 , filter size =  3x3, padding = same , activation = relu, input sahpe = 64,64,3]
- Convolution : [filters = 32 , filter size =  3x3, padding = same , activation = relu]
- Maxpooling : [filter size = 3x3]

- Convolution : [filters = 32 , filter size =  3x3, padding = same , activation = relu]
- Convolution : [filters = 64 , filter size =  3x3, padding = same , activation = relu]
- Maxpooling : [filter size = 3x3]

- Convolution : [filters = 128 , filter size =  3x3, padding = same , activation = relu, input sahpe = 64,64,3]
- Convolution : [filters = 256 , filter size =  3x3, padding = same , activation = relu]
- Maxpooling : [filter size = 3x3]

- BatchNormalization
- Flatten
- Dropout(rate = 0.5)

- Dense : [512, activation = relu,kernel_regularizer = regularizers.l2(0.001)]
- Dense : [29, activation = softmax]

> Model 2

- Convolution : [filters = 32 , filter size =  5x5, activation = relu, input sahpe = 64,64,3]
- Maxpooling : [filter size = 2x2]


- Convolution : [filters = 64 , filter size =  3x3, activation = relu, input sahpe = 64,64,3]
- Maxpooling : [filter size = 2x2]


- Convolution : [filters = 64 , filter size =  3x3, activation = relu, input sahpe = 64,64,3]
- Maxpooling : [filter size = 2x2]

- BatchNormalization
- Flatten

- Dense : [128, activation = relu]
- Dense : [29, activation = softmax]

# Accuracy 
> model 1 accuracy on training data : 97.8%

> model 2 accuracy on training data : 98.8%

# Data
>The data set is a collection of images of alphabets from the American Sign Language, separated in 29 folders which represent the various classes.

> The ASL Alphabet data set provides 87,000 images of the ASL alphabet.

> The test data set contains a mere 29 images, to encourage the use of real-world test images.

> There are 2 data sets utilized in this notebook:
 - *ASL Alphabet train* - This data set is the basis for the model.
 - *ASL Alphabet Test* - This data set was made specifically for validating the model created using the above data set, and is intended to be used to improve the feature engineering and modeling process to make it more versatile in "the wild" with less contrived images.

> It is available on Kaggle as the ASL Alphabet Dataset. https://www.kaggle.com/grassknoted/asl-alphabet.

# Functions 
> *load_train_data*
```
function to load train data in RGB type.
```
> *load_test_data*
```
function to load test data in RGB type.
```
> *create_model*
```
function to build the models 1.
```
> *create_model_2*
```
function to build the models 1.
```
