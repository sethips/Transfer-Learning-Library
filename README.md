# Transfer-Learning-Library
Transfer Learning Library written in Keras for image classification. 

## Goals

- To classify images without making any custom model but rather using keras built in models.

- To get high accuracy for classifying almost any image.

## Models

All the Keras built in models are available

| Model  | Size  |  Top-1 Accuracy  |  Top-5 Accuracy  |  Parameters  |  Depth  |
| -------------     | ------------- | -------------| ------------- | ------------- | ------------- |
| VGG16    | 528 MB    |  0.715    | 0.901    | 138,357,544    | 23    |
| VGG19    | 549 MB    |  0.727    | 0.910    | 143,667,240    | 26    |
| ResNet50    |  99 MB    | 0.759    | 0.929    | 25,636,712    |  168    |
| Xception    |  88 MB    | 0.790    | 0.945    | 22,910,480     | 126    |
| InceptionV3    | 92 MB    | 0.788    | 0.944    | 23,851,784    |  159    |
| InceptionResNetV2    | 215 MB    |  0.804    | 0.953   | 55,873,736    |  572    |
| MobileNet    | 17 MB    | 0.665    | 0.871    | 4,253,864    | 88    |
| DenseNet121    | 33 MB    | 0.745    | 0.918    | 8,062,504    | 121    |
| DenseNet169    | 57 MB    | 0.759    | 0.928    | 14,307,880    |  169    |
| DenseNet201    | 80 MB    | 0.770    | 0.933    | 20,242,984    |  201    |
| NASNetMobile    | 21 MB    | NA    | NA    | 5,326,716    |  NA    |
| NASNetLarge    | 342 MB    | NA    | NA    | 88,949,818    |  NA    |

## To Execute

`pip install keras`

`git clone https://github.com/abhinavsagar/Transfer-Learning-Library.git`

`cd Transfer-Learning-Library`

`python main.py --model Xception`

## Result

![soccer ball](soccer_ball.jpeg)

```
Layer (type)                 Output Shape              Param #   
=================================================================
input_1 (InputLayer)         (None, 224, 224, 3)       0         
_________________________________________________________________
block1_conv1 (Conv2D)        (None, 224, 224, 64)      1792      
_________________________________________________________________
block1_conv2 (Conv2D)        (None, 224, 224, 64)      36928     
_________________________________________________________________
block1_pool (MaxPooling2D)   (None, 112, 112, 64)      0         
_________________________________________________________________
block2_conv1 (Conv2D)        (None, 112, 112, 128)     73856     
_________________________________________________________________
block2_conv2 (Conv2D)        (None, 112, 112, 128)     147584    
_________________________________________________________________
block2_pool (MaxPooling2D)   (None, 56, 56, 128)       0         
_________________________________________________________________
block3_conv1 (Conv2D)        (None, 56, 56, 256)       295168    
_________________________________________________________________
block3_conv2 (Conv2D)        (None, 56, 56, 256)       590080    
_________________________________________________________________
block3_conv3 (Conv2D)        (None, 56, 56, 256)       590080    
_________________________________________________________________
block3_conv4 (Conv2D)        (None, 56, 56, 256)       590080    
_________________________________________________________________
block3_pool (MaxPooling2D)   (None, 28, 28, 256)       0         
_________________________________________________________________
block4_conv1 (Conv2D)        (None, 28, 28, 512)       1180160   
_________________________________________________________________
block4_conv2 (Conv2D)        (None, 28, 28, 512)       2359808   
_________________________________________________________________
block4_conv3 (Conv2D)        (None, 28, 28, 512)       2359808   
_________________________________________________________________
block4_conv4 (Conv2D)        (None, 28, 28, 512)       2359808   
_________________________________________________________________
block4_pool (MaxPooling2D)   (None, 14, 14, 512)       0         
_________________________________________________________________
block5_conv1 (Conv2D)        (None, 14, 14, 512)       2359808   
_________________________________________________________________
block5_conv2 (Conv2D)        (None, 14, 14, 512)       2359808   
_________________________________________________________________
block5_conv3 (Conv2D)        (None, 14, 14, 512)       2359808   
_________________________________________________________________
block5_conv4 (Conv2D)        (None, 14, 14, 512)       2359808   
_________________________________________________________________
block5_pool (MaxPooling2D)   (None, 7, 7, 512)         0         
_________________________________________________________________
flatten (Flatten)            (None, 25088)             0         
_________________________________________________________________
fc1 (Dense)                  (None, 4096)              102764544 
_________________________________________________________________
fc2 (Dense)                  (None, 4096)              16781312  
_________________________________________________________________
predictions (Dense)          (None, 1000)              4097000   
=================================================================
Total params: 143,667,240
Trainable params: 143,667,240
Non-trainable params: 0
_________________________________________________________________
soccer_ball (99.99%)
```

### There are several substantial benefits to leveraging pre-trained models:

- super simple to incorporate
- achieve same or even better(depending on the dataset) model performance quickly
- there’s not as much labeled data required
- versatile uses cases from transfer learning, prediction, and feature extraction

## Citing

```
@misc{Abhinav:2019,
  Author = {Abhinav Sagar},
  Title = {Transfer Learning Library},
  Year = {2019},
  Publisher = {GitHub},
  Journal = {GitHub repository},
  Howpublished = {\url{https://github.com/abhinavsagar/Transfer-Learning-Library}}
}
```

## References

https://github.com/keras-team/keras-applications
