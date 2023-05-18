### The Problem:
Waste System recycling.
ref: https://www.researchgate.net/publication/343841421_A_Distributed_Architecture_for_Smart_Recycling_Using_Machine_Learning
The reference guides the techniques and parameters of models trained

## Data Collection and Preparation: 
    - Trashnet dataset can be found @ https://github.com/garythung/trashnet 
    - Get_Data.ipynb clones the repo and prepares it    
    - 501 glass
    - 594 paper
    - 403 cardboard
    - 482 plastic
    - 410 metal
    - 137 trash

## Framework: 
    - TensorFlow: Standard computer vision and neural networks library with augmentation processing and pretrained models

## Model Development: 
    - CNN architecture
    - Some of the better architectures mentioned in the paper referenced
    
    - InceptionResnetV2 89.13% 
    - DenseNet121 95.10%
    - Inception-V4 94.24%
    - MobileNet-V2 (reference personalised) 96.57%

## Training: 
    - Set up Models
    - Train base Models
    - tune hyper parameters
    - train with augmented data

## Evaluation:
    - Base training models
    - BasicCNN 200 epochs 78% accuracy
    - ResNet50V2 91% accuracy 100 epochs
    - MobileNetV2 89% accuracy 100 epochs 
    
    - Validation accuracy is less than 20% with 0.1 of training data

## Documentation: 
    - The model is not yet performing, the training metrics are not accurate measurements of live performance and more research on the data shall be applied such as, sub classes or yolo model training.  
    - Ideally if one object can be identified as recyclable or not then maybe the type of material can be identified from there as a common outcome in the validation confusion matrix is that trash is an unidentifiable class, also by a personal observation.   

## Overview: 
    The purpose of this module was to identify trash types for waste recycling systems that seperate and aggregate trash and recyclables.    

## Dependencies: 
    - conda install tensorflow
    - conda install matplotlib
    - conda install scikit-learn
    - conda install seaborn 
    - conda install numpy


## Installation Instructions: 
    - clone and run notebooks

## Usage Guide: 
    Using Anaconda enviroment (install Anaconda)
    Then install dependencies for standard notebook experience
    Get_Data.ipynb gets the trashnet repository and splits a train and validation set which is 10% of each class
    Training models can be performed with evaluation metrics and graphs
    

## Configuration: 
    - Input shapes are different for both pre trained models
    - ResNet50V2 image size (150, 150)
    - MobileNet image size (224,224)

## Continuous Improvement: 
    - explore 
        - yolo training
        - sub class classification
        - recyclable binary classifier, then trash type classifier 
