# BRAIN TUMOR CLASSIFICATION AND PREDICTION USING CONVOLUTIONAL NEURAL NETWORKS
## Introduction:

A brain tumor is a collection, or mass of abnormal cells in our brain. Our skull, which encloses our brain, is very rigid. Any growth inside such a restricted space can cause problems. Brain tumors can be cancerous (malignant) or noncancerous (benign). When benign or malignant tumors grow, they can cause the pressure inside our skull to increase. This can cause brain damage, and it can be life-threatening. Early detection and classification of brain tumors is an important research domain in the field of medical imaging and accordingly helps in selecting the most convenient treatment method to save patients life.

## Problem Identification

### Problem statement formation
Brain Tumor Classification and Prediction using Convolutional Neural Networks to help automate the diagnostic process which will ensure proper treatment and will save lives and resources. 

### Context
Brain Tumors are complex. There are a lot of abnormalities in the sizes and location of the brain tumor(s). This makes it difficult for complete understanding of the nature of the tumor. Also, a professional Neurosurgeon is required for MRI analysis. Often, in developing countries the lack of skillful doctors and lack of knowledge about tumors makes it really challenging and time-consuming to generate reports from MRI’. So, an automated system on Cloud can solve this problem.
Data Wrangling and Exploratory Data Analysis

## Data Wrangling and Exploratory Data Analysis

### Dataset Summary:
The dataset contains four separate classes of brain MRI images: Glioma Tumor, Meningioma Tumor, Pituitary Tumor, and Without presence of tumor (No Tumor). The total number of images is more than seven thousand and I have divided the dataset into training set, validation set, and test set with a 70:15:15 ratio. Each of the training, validation, and test dataset contains all four classes. The characteristics of each tumor class is described below:

### Meningioma Tumor
A meningioma is a tumor that arises from the meninges — the membranes that surround our brain and spinal cord. Although not technically a brain tumor, it is included in this category because it may compress or squeeze the adjacent brain, nerves and vessels. Meningioma is the most common type of tumor that forms in the head. Most meningiomas grow very slowly, often over many years without causing symptoms. But sometimes, their effects on nearby brain tissue, nerves or vessels may cause serious disability.

### Glioma Tumor
Glioma is a type of tumor that occurs in the brain and spinal cord. Gliomas begin in the gluey supportive cells (glial cells) that surround nerve cells and help them function. Three types of glial cells can produce tumors. Gliomas are classified according to the type of glial cell involved in the tumor, as well as the tumor's genetic features, which can help predict how the tumor will behave over time and the treatments most likely to work. A glioma can affect your brain function and be life-threatening depending on its location and rate of growth.

### Pituitary Tumor
Pituitary tumors are abnormal growths that develop in your pituitary gland. Some pituitary tumors result in too much of the hormones that regulate important functions of your body. Some pituitary tumors can cause your pituitary gland to produce lower levels of hormones. Most pituitary tumors are noncancerous (benign) growths (adenomas). Adenomas remain in your pituitary gland or surrounding tissues and don't spread to other parts of your body.

### No Tumor
The MRI image does not contain any kinds of tumor cell.
## Data Wrangling
The steps I have taken to wrangle the dataset is described below:
I.	I have Imported all necessary modules and libraries
II.	Observed all the MRI images in training, validation, and test set with their respective file format.
III.	Observed whether the dataset contain RGB or grayscale images
IV.	Counted the number of images of each set
V.	Applied different filtering techniques to improve the image quality
VI.	Observed the shape of each image and found all the images of RGB with different shape
VII.	I have converted all the images into gray scale image of size (128, 128, 1).
## Exploratory Data Analysis
### Original MRI images
![image](https://user-images.githubusercontent.com/79649430/148147248-7077b6cf-0b53-4596-a3fe-c18ffbf2a6ba.png)
![image](https://user-images.githubusercontent.com/79649430/148147263-d785dab2-d64b-4792-953e-0583810bb776.png)
![image](https://user-images.githubusercontent.com/79649430/148147286-31b3235c-33f9-466b-8f61-1a6f9125912b.png)
![image](https://user-images.githubusercontent.com/79649430/148147299-28f31558-7633-48e3-af83-5872ae8092b6.png)
### Preprocessed MRI images
![1](https://user-images.githubusercontent.com/79649430/148147448-7653e858-ac02-42dc-937b-58a296dac1f5.JPG)![2](https://user-images.githubusercontent.com/79649430/148147515-9e585ae8-8457-404a-8b84-423d89844add.JPG)
![3](https://user-images.githubusercontent.com/79649430/148147540-fdf6828f-bb02-4a8d-9a18-f4d475361607.JPG)
![4](https://user-images.githubusercontent.com/79649430/148147557-ece9747a-6483-4a87-aa30-da8da952e301.JPG)

## Data Preprocessing
The steps I have taken to preprocess all the training, validation and test dataset is given below:
I.	I have Created image arrays and corresponding labels for training, validation, and test dataset
II.	The image arrays for feature vector are respectively X_train, X_valid, X_test, and the corresponding labels are y_train, y_valid, and y_test
III.	Then, I have Created one-hot vectors for y_train, y_test, and y_valid
IV.	Figure below shows the count plot of the final training, validation, and test dataset.

## Modeling
To classify and detect brain tumor, I have implemented and trained several models and evaluated them by using test data to measure models performance.

### Model 1: Simple neural network with only dense layers

#### Architecture of Model 1:
The model 1 contains an input layer, six Dense layers, and one output layer. I have used ReLU as an activation function for the Dense layers and Softmax as an activation function for the output layer for multiclass classification and Adam as an optimizer. 
![image](https://user-images.githubusercontent.com/79649430/148147666-c6575f98-ce93-40f6-97db-d33a9d97055b.png)

#### Training Progress for Model 1:
![image](https://user-images.githubusercontent.com/79649430/148148121-7a83134b-dabb-41e4-8c65-f5ab0306f708.png)
#### Evaluation Results of Model 1:
![image](https://user-images.githubusercontent.com/79649430/148148249-2dcf3706-1b3a-4f9a-9010-6cbf2433b276.png)

### Model 2: Convolutional neural network with two Conv2D layers
#### Architecture of Model 2:
Model 2 contains an input layer, two Conv2D layers with MaxPolling2D as a pooling layer, one Dense layer, and an output layer. Similar to model 1, I have used ReLU as an activation function for the hidden layers, Softmax as an activation function for the output layer, and Adam as an optimizer again. I have not used any regularization in model 2. 
![image](https://user-images.githubusercontent.com/79649430/148148377-9013f7d0-9486-4eec-893d-87e1a8d863c3.png)

#### Training Progress of Model 2:
![image](https://user-images.githubusercontent.com/79649430/148148400-1474fac2-292f-462e-ba3a-6934feb7b496.png)
#### Evaluation Results of Model 2:
![image](https://user-images.githubusercontent.com/79649430/148148435-886eab00-fbc9-4f8f-be0c-f372581e0f65.png)

### Model 3: Convolutional neural network with two Conv2D layers with regularization layers

#### Architecture of Model 3:
Model 3 is a copy of model 2. To overcome the overfitting caused by model 2, I have added BatchNorm2D layer after each convolutional layers and a Dropout layer. 
![image](https://user-images.githubusercontent.com/79649430/148148485-21a5a5d0-22a2-405d-803e-bf2b230574c7.png)
#### Training Progress of Model 3:
![image](https://user-images.githubusercontent.com/79649430/148148524-35a188b2-87eb-445f-96e2-c1849552ee59.png)
#### Evaluation Results of Model 3:
![image](https://user-images.githubusercontent.com/79649430/148148567-05102e3f-468d-4ec2-9f5b-96e490e4bc0d.png)

### Model 4: Convolutional neural network with three Conv2D layers and regularization layers

#### Architecture of Model 4:
Model 4 contains an input layer, three Conv2D layers with MaxPolling2D and BatchNorm2D, two Dense layers, and an output layer. The activation function, optimizer remains same with previous models. I have introduced learning rate scheduling and EarlyStopping for adaptive training.
![image](https://user-images.githubusercontent.com/79649430/148148641-4cfcf46d-b633-4731-be18-0a1cecf11e0c.png)
#### Training Progress of Model 4:
![image](https://user-images.githubusercontent.com/79649430/148148688-2ed60912-1008-4d3e-bd78-0f890ff32832.png)
#### Evaluation Results of Model 4:
![image](https://user-images.githubusercontent.com/79649430/148148720-52c8c9e4-2290-4cf0-b56e-9292f3c22e96.png)

### Model 5: Convolutional neural network with four Conv2D layers and regularization layers

#### Architecture of Model 5:
Model 5 contains an input layer, four Conv2D layers with MaxPolling2D and BatchNorm2D, one Dense layer, and an output layer. The activation function, optimizer remains same with previous models. I have introduced learning rate scheduling and EarlyStopping for adaptive training
![image](https://user-images.githubusercontent.com/79649430/148148772-f96a7bec-3e15-4e02-9b09-d87ed5caecf8.png)
#### Training Progress of Model 5:
![image](https://user-images.githubusercontent.com/79649430/148148804-8ed6782d-25f8-403e-9e84-b0d1b7c12baa.png)
#### Evaluation Results of Model 5:
![image](https://user-images.githubusercontent.com/79649430/148148838-6aa0340e-9db2-4643-9a5d-953e97b7c126.png)

## Results and Findings
Initially, I have implemented first model (model 1) without using any convolutional neural network and received 83.49% test accuracy and 83% recall value. After that, I have implemented model 2 with two Conv2D layers. Model 2 performed better than first model but had strong overfitting problem since I haven’t added any regularization techniques. I have introduced Batch Normalization and dropout layers to the previous model and implemented model 3 to overcome overfitting. Despite addition of regularization techniques, the evaluation metrics was unchanged, and the model’s training and test accuracy was not improving.
To overcome underfitting, I have implemented complex convolutional neural networks: model 4 with three Conv2D layers and Model 5 with four Conv2D layers. I have received test accuracy and recall value of 97% form model 4 and there was a fluctuation with training accuracy and validation accuracy also. Finally, the model 5 performed great compared with other models and I have received overall training accuracy, validation accuracy, test accuracy, and the weighted value of precision, recall, and F1-score of 98%. Also, by inspecting confusion matrix of model 5, I have observed that out of 1048 test images there is only 23 misclassifications.
![111](https://user-images.githubusercontent.com/79649430/148149052-04d92a48-7724-484a-b6c9-91f500258630.JPG)

## Conclusion
Despite lack of proper computational resources, I have implemented, trained, and tested all my models and obtained good evaluation results. The optimum model (model 5) showed training accuracy, validation accuracy, test accuracy, and the weighted value of precision, recall, and F1-score of 98% and contained only 23 misclassifications out of 1048 test images.
