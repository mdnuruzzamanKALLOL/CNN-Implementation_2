# CNN-Implementation

Residual Neural Network (ResNet)
What is Resnet?
ResNet, short for Residual Networks,Residual neural networks are a type of artificial neural network (ANN) that forms networks by stacking residual blocks. It is a convolutional neural network used as a backbone for many computer vision tasks. The fundamental breakthrough with ResNet was it allowed us to train extremely deep neural networks with 150+layers. It is an innovative neural network that was first introduced by Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun in their 2015 computer vision research paper titled ‘Deep Residual Learning for Image Recognition’.

ResNet has many variants that run on the same concept but have different numbers of layers. Resnet50 is used to denote the variant that can work with 50 neural network layers(48 Convolution layers along with 1 MaxPool and 1 Average Pool) deep

Why Resnet?
Convolutional Neural Networks have a major disadvantage — ‘Vanishing Gradient Problem’. During backpropagation, the value of gradient decreases significantly, thus hardly any change comes to weights. To overcome this, ResNet is used. It make use of “SKIP CONNECTION” which lies at the core of the residual blocks, is the strength of this type of neural network.

All algorithms train on the output ‘Y’ but, ResNet trains on F(X). In simpler words, ResNet tries to make F(X)=0 so that Y=X.
