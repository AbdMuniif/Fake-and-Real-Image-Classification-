Machine Learning Pipeline Design to Predict Status of a Loan 
==============================
This project is a robust image classification pipeline designed to differentiate between fake and real images. It utilizes the ResNet50 architecture, renowned for its exceptional performance in image recognition tasks, to assess image authenticity with an impressive 92% accuracy. The trained ResNet50 model is saved and integrated into a prototype for user testing.
The prototype is an interactive application built with Tkinter, offering a user-friendly interface for classifying images. Users can easily upload an image, and the application provides real-time feedback on whether the image is classified as fake or real based on the pre-trained model. This streamlined interface enhances user experience while effectively demonstrating the model's classification capabilities.

Pipeline Overview:
-------------------
Data Loading and Preprocessing:
The pipeline starts by loading images from specified directories. Images are converted using the Error Level Analysis (ELA) technique to enhance detection of tampering.
The convert_to_ela_image function processes images to highlight discrepancies introduced by manipulation, making it easier to classify them as fake or real.

Feature Preparation:
Images are resized and normalized before being fed into the model. The data is then split into training and validation sets to ensure the model's generalizability.

Model Building:
A ResNet50 model is used as the base, with additional layers for classification. The model is customized with a Global Average Pooling layer, Batch Normalization, and Dense layers with dropout for regularization.
The model is compiled with the Adam optimizer and a learning rate schedule to handle large datasets effectively.

Data Augmentation and Training:
To enhance model robustness and prevent overfitting, data augmentation techniques such as rotation, shifting, shearing, and flipping are applied.
The model is trained with these augmented images and early stopping is employed to halt training when performance plateaus.

Evaluation:
After training, the model's performance is evaluated using accuracy, loss metrics, and a confusion matrix.
Detailed classification reports are generated to assess the model's ability to distinguish between fake and real images.

Model Saving:
The trained model is saved for future use in testing or deployment.

Directory Structure
-------------------
- `Dataset` Dataset used in the project.
- `RESNET 28` Python script of data training, model development, and experimentation.
- `Interface` Python script for the tkinter user interface or testing.
  
Download Dataset
------------
Open the data folder, and given the link to download the .csv dataset in kaggle, Download the dataset and put into the data folder. follow the instruction in the Dataset folder.

Installation (Terminal)
------------
pip install pillow numpy keras tensorflow matplotlib scikit-learn

Make sure to install the necessary libraries and modules before running the project.

The Example of the prototype 
------------
![image](https://github.com/user-attachments/assets/52e99f5d-24ba-4489-abc4-c9ecf582ae66)
