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
![1](https://user-images.githubusercontent.com/79649430/148147448-7653e858-ac02-42dc-937b-58a296dac1f5.JPG)


