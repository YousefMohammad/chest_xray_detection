# Chest X-ray Detection

## Introduction
million people worldwide are suffering from Pneumonia which results in the death of 4 million people every year.
Pneumonia is an acute lower respiratory disease with traces of infection usually because of some micro-organism, bacteria or virus.
This project aims to harness the power of deep learning to develop a sophisticated model that can identify signs of pneumonia from chest X-ray images with high accuracy and efficiency. Our goal is to provide a tool that aids healthcare professionals in diagnosing this condition more swiftly and accurately, ultimately leading to improved patient care.


## Dataset
The normal chest X-ray (left panel) depicts clear lungs without any areas of abnormal opacification in the image. Bacterial pneumonia (middle) typically exhibits a focal lobar consolidation, in this case in the right upper lobe (white arrows), whereas viral pneumonia (right) manifests with a more diffuse ‘‘interstitial’’ pattern in both lungs.
[https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia?resource=download]

## Content
The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal).

Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.

For the analysis of chest x-ray images, all chest radiographs were initially screened for quality control by removing all low quality or unreadable scans. The diagnoses for the images were then graded by two expert physicians before being cleared for training the AI system. In order to account for any grading errors, the evaluation set was also checked by a third expert..

![jZqpV51](https://github.com/YousefMohamedSalah/chest_xray_detection/assets/99505074/2734b1eb-8190-406e-805d-8f05a1e018b7)

## Data Wrangling
Prior to training our model, we conducted thorough preprocessing steps. These included image resizing to a standard format, normalization of pixel values, and augmentation techniques to enhance model robustness.
The dataset displays a real-world distribution of cases, with a higher prevalence of pneumonia cases, mirroring real clinical scenarios.
Such a distribution challenges our model to learn from imbalanced data, a common issue in medical diagnostics.

## Data Preparation
All X-ray images were resized to a uniform dimension (224x224 pixels) to ensure consistency in input size for the neural network.
This standardization is vital for the model to process and learn from the images efficiently.
Pixel values in the images were normalized to a scale of 0 to 1. This step reduces the computational burden and helps in faster convergence during training.

## Data Augmentation
Data augmentation is a technique used to increase the diversity of our dataset by applying various transformations to the images. 
This process is crucial for improving the model's ability to generalize to new, unseen data.
We applied several augmentation techniques to the chest X-ray images, including random rotations, horizontal flips, zooming, and shifts in the image position.
These transformations mimic different imaging conditions and patient positions, creating a more comprehensive training dataset.
Augmentation helps in reducing overfitting, a common challenge in deep learning, especially when dealing with limited datasets.

## Results
Once the model has been evaluated, we can present the results.
There are two key aspects to present: the diagnostics of the learning behavior of the model during training and the estimation of the model performance.
First, the diagnostics involve creating a line plot showing model performance on the train and validation set during training. 
These plots are valuable for getting an idea of whether a model is overfitting, underfitting, or has a good fit for the dataset.
We will create a single figure with two subplots, one for loss and one for accuracy. 
The blue lines will indicate model performance on the training dataset and orange lines will indicate performance on the hold out test dataset. 


