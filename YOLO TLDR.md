# You Only Look Once: Unified, Real-Time Object Detection

## Existing Methods (subverted paradigms) :

- Sliding Window classification

- R-CNN : region proposal

## One sentance :

YOLO reframes object detection as a single regression problem.

## One Figure :

![](C:\Users\CALEGRAND.M\AppData\Roaming\marktext\images\2022-04-07-09-56-10-image.png)

## TL;DR :

### Concept

YOLO splits the imput into a grid of $S \times S$ for each it will predict B boxes and the class of the grid cell. Each box will take the class probability of the cell and combine it with it's object probability 

$Pr(Class_i|Object) \times Pr(Object) \times IoU^{truth}_{pred} = Pr(Class_i) \times IoU_{truth}$

### Architecture

YOLO uses a convolutional network to encode the picture. And then use two dense layers to classsify the cell and regress  the box coordinates and the class probabilities.

### Training

To train the model, they used a tweaked sum squared error that grades a box differently depending on wether it is responsible for an object.

# 
