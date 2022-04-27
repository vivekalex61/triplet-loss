
# Face net and Triplet loss 

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)

Learning a distance embedding for facerecognization tasks. 


## Introduction 

#### What is  Facenet and Triplet loss?
Face recognisation has been a phenominal in recent years. Mobiles phones, Face recognization at offices, Security systems, They are adopted to use every scenerios. A good face recognization system has lowest false postive errors and They need only limited resources to train.

FaceNet is the name of the facial recognition system that was proposed by Google Researchers in 2015 in the paper titled FaceNet: A Unified Embedding for Face Recognition and Clustering. 

They proposed an approach in which it generates a high-quality face mapping from the images using deep learning architectures. They used a method called triplet loss as a loss function to train this architecture.
By computing similarity between the face embeddding we can conclude how much similar it is .

##### Triplet loss

![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)
Intuition behind the triplet loss is we will a have three types of images. A positive, Anchor and Negative image.
Anchor and postive  image will be selected from a same class and anchor from a different class.
In Triplet loss, Train the model to reduce distance between anchor and positive image and increase the distance between anchor image and negative image.

In other words, We are pointing similar images to a single point in embeddding space and creating a margin between similar images and negative images.
![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)                      
                  
                  fig 1 formula
![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)

                    fig 1 formula
## Overview of Tripletloss
- Datasets and Data-Loading
- Image Preprocessing
- Model creation

### Datasets and Data-Loading

MNIST digits classification dataset. This is a dataset of 60,000 28x28 grayscale images of the 10 digits, along with a test set of 10,000 images. More info can be found at the MNIST homepage.
### image Preprocessing

The aim of pre-processing is an improvement of the image data that suppresses undesired distortions or enhances some image features relevant for further processing and analysis task.
. The aim of pre-processing is an improvement of the image data that suppresses undesired distortions or enhances some image features relevant for further processing and analysis task. 
 
Ref : https://www.mygreatlearning.com/blog/introduction-to-image-pre-processing/
MNIST digits classification dataset. This is a dataset of 60,000 28x28 grayscale images of the 10 digits, along with a test set of 10,000 images. More info can be found at the MNIST homepage.
#### Triplet image pair creation
The model needs pair of inputs (postive image, anchor image , negative image)

### Model building and training

Model building has two parts:

1)Base model creation 

2)Sharing the base model with three inputs(Postivie, Anchor, Negative)

3)Custom Triplet loss function 
#### 1)Base model creation :
Base model can be made by using any ptrtrained archetectures like VGG,ResNet etc.
we should replace input shape with image dimensions and output with dimension of embedding we need.
[alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)

#### 2)Sharing the base model with three inputs(Postivie, Anchor, Negative).
![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)
#### 3)Custom Triplet loss function 

Ref : https://arxiv.org/pdf/1503.03832.pdf

![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)
![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)
![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)


ref :https://omoindrot.github.io/triplet-loss
## Predictions
![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)
![alt text](https://raw.githubusercontent.com/vivekalex61/insightsearch/master/test/overall_sentiments.png)


## End Notes

The model is not finetuned .