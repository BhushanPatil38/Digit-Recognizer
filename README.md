# Digit-Recognizer

### Here we focus on identifying handwriting images via CNN. The CNN architecture used is  -

####   [[Conv2D->relu]*2 -> MaxPool2D -> Dropout]*2 -> Flatten -> Dense -> Dropout -> Out

###### Conv2D is the first layer is which is used as a filter. The filters here can be seen as a transformation of the image. The CNN then maps these features from the transformed images. 

###### Next layer is the MaxPool2D layer which is used to reduce computational cost and reduce overfitting. It is more like a downsampling filter which picks it’s 2 neighbouring pixels and chooses the maximum value. We pick the pooling size and as the size increases the downsampling becomes more significant.

###### Dropout is a regularization method, where a proportion of nodes in the layer are randomly ignored by setting their weights to zero for each training sample. This drops randomly a proportion of the network and forces the network to learn features in a distributed way. This technique also improves generalization and reduces the overfitting.

###### We have used ReLu as the activation function. 'relu' is the rectifier (activation function max(0,x). which is used to add nonlinearity to the network.

###### The Flatten layer is used to convert the final feature maps into a one single 1D vector. This flattening step is needed so that you can make use of fully connected layers after some convolutional/maxpool layers. It combines all the found local features of the previous convolutional layers.

#### We have considered epochs to be 2 to computational time, it can be increased to 30 for a higher accuracy.
