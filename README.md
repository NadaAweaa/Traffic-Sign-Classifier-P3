# Self-Driving Car Engineer Nanodegree
## Traffic Sign Recognition Calssifer 

This project shows how to classify german traffic signs using a modified LeNet neuronal network. 
(See e.g. [Yann LeCu - Gradiant-Based Learning Applied to Document Recognition](http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf))

### Rubric 
The goals / steps of this project are the following:
* Load the data set
* Explore, summarize and visualize the data set
* Design, train and test a model architecture
* Use the model to make predictions on new images
* Analyze the softmax probabilities of the new images
* Summarize the results with a written report

### Dependencies 
This project requires Python 3.5 and the following Python libraries installed:

   - Jupyter
   - NumPy
   - SciPy
   - scikit-learn
   - TensorFlow
   - Matplotlib
   
You can setup them all using the starter-kit:
  * [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit)
  
[Link to Traffic Signs Data](https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/traffic-signs-data.zip) 


### Data Summery 
I used the numpy library and Tensorflow to calculate summary statistics of the traffic signs data set:

    The size of training set is 34799
    The size of the validation set is 4410
    The size of test set is 12630
    The shape of a traffic sign image is (32, 32, 3)
    The number of unique classes/labels in the data set is 43
    
#### Here is a diagram of the layers present in the myLeNet() function:


| Layer         		|     Description	        					| 
|:---------------------:|:---------------------------------------------:| 
| Input         		| 32x32x3 RGB image   							| 
| Convolution 5x5   | 1x1 stride, valid padding, outputs 28x28x6 	|
| Dropout					|	 Externally tunable keep_prob					    |
| Max pool	      	| Size 2x2, strides 2x2, valid padding, outputs 14x14x6				|
| Convolution 5x5	    | Stride 1, valid padding.  Outputs 10x10x16   						|
| Dropout					|	 Externally tunable keep_prob					    |
| Max pool	      | Size 2x2, strides 2x2, valid padding, outputs 5x5x16				|
| Flatten		| Input 5x5x16, output 400					|
| Fully connected	| Input 400, output 120       |
| Dropout					|	 Externally tunable keep_prob					    |
| Fully connected	| Input 120, output 84								|
| Dropout					|	 Externally tunable keep_prob					    |
|	Fully connected	|	 Input 84, output 43 (labels)	|

