### The Problem:
Waste System recycling. <br />
ref: https://www.researchgate.net/publication/343841421_A_Distributed_Architecture_for_Smart_Recycling_Using_Machine_Learning <br />
The reference guides the techniques and parameters of models trained

## Data Collection and Preparation: 
Trashnet dataset can be found @ https://github.com/garythung/trashnet <br />
Get_Data.ipynb clones the repo and prepares it    <br />
    - 501 glass <br />
    - 594 paper <br />
    - 403 cardboard <br />
    - 482 plastic <br />
    - 410 metal <br />
    - 137 trash <br />

## Framework: 
TensorFlow: Standard computer vision and neural networks library with augmentation processing and pretrained models 

## Model Development: 
Some of the better architectures mentioned in the paper referenced which in our case will be trying to beat <br />    
- InceptionResnetV2 89.13% <br />
- DenseNet121 95.10% <br />
- Inception-V4 94.24% <br />
- MobileNet-V2 (source reference) 96.57% <br />

## Training: 
Set up Models <br />
Train base Models <br />
Tune hyper parameters <br />
Train with augmented data <br />

## Evaluation:
My model training  <br />
- BasicCNN 78% accuracy 200 epochs <br />
- ResNet50V2 91% accuracy 100 epochs <br />
- MobileNetV2 89% accuracy 100 epochs  <br />
Validation accuracy is less than 20% with 0.1 of training data

## Documentation: 
The model is not yet performing, the training metrics are not accurate measurements of live performance and more research on the data shall be applied such as, sub classes or yolo model training.  <br />
Ideally if one object can be identified as recyclable or not then maybe the type of material can be identified from there as a common outcome in the validation confusion matrix is that trash is an unidentifiable class, also by a personal observation common items look the same as other classes.   

## Overview: 
The purpose of this module was to identify trash types for waste recycling systems that seperate and aggregate trash and recyclables.    

## Dependencies: 
    conda install tensorflow
    conda install matplotlib
    conda install scikit-learn
    conda install seaborn 
    conda install numpy


## Installation Instructions: 
Clone and run notebooks

## Usage Guide: 
Using Anaconda enviroment (install Anaconda) <br />
Then install dependencies for standard notebook experience <br />
Get_Data.ipynb gets the trashnet repository and splits a train and validation set which is 10% of each class <br />
Training models can be performed with evaluation metrics and graphs <br />
    

## Configuration: 
- Input shapes are different for both pre trained models <br />
- ResNet50V2 image size (150, 150) <br />
- MobileNet image size (224,224) <br />

## Continuous Improvement: 
- Exploring  <br />
    - Yolo training <br />
    - Sub class classification <br />
