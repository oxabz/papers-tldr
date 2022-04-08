# [Swin Transformer: Hierarchical Vision Transformer using Shifted Windows](https://arxiv.org/pdf/2103.14030.pdf)

## In one sentence :

Swin creates a transformer based architecture to replace the convolutions used as backbone in detection and as encoder in unets.

## In one figure :

![](C:\Users\CALEGRAND.M\AppData\Roaming\marktext\images\2022-04-08-13-56-17-image.png)

## TL;DR :

### General Idea

- Transformer seem to work well

- Convolutional network are the bases of all computer vision model

- ViT can't fit in the role

- ViT are prohibitively expensive to scale up

### Architecure

- 4 stages that divide the resolution by 2 and multiply the feature count by 2 (like most backbone)
  
  - The layers split the picture in patches that are used as token in the transformer
  
  - Rather than running a transformer on all the patches the models run it on a window of patches with a fixed number of patch.
    
    - Reduces complexity
  
  - To allow the extraction of features of two patch on both side of the window Swin uses  a shifting window
    
    <img title="" src="file:///C:/Users/CALEGRAND.M/AppData/Roaming/marktext/images/2022-04-08-14-28-55-image.png" alt="" width="290">
  
  - They add positional encoding to the patches relative to the window because they found out that absolute position encoding doesnt seem to improve performance

### Training

Considering that it is an end to end network it can be trained within any kind of model that typicaly use Convolutional networks without asle 


