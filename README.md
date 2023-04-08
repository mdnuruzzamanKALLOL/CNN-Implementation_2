# CNN Implementation

Residual Neural Network (ResNet)
What is Resnet?
ResNet, short for Residual Networks,Residual neural networks are a type of artificial neural network (ANN) that forms networks by stacking residual blocks. It is a convolutional neural network used as a backbone for many computer vision tasks. The fundamental breakthrough with ResNet was it allowed us to train extremely deep neural networks with 150+layers. It is an innovative neural network that was first introduced by Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun in their 2015 computer vision research paper titled ‘Deep Residual Learning for Image Recognition’.

ResNet has many variants that run on the same concept but have different numbers of layers. Resnet50 is used to denote the variant that can work with 50 neural network layers(48 Convolution layers along with 1 MaxPool and 1 Average Pool) deep

Why Resnet?
Convolutional Neural Networks have a major disadvantage — ‘Vanishing Gradient Problem’. During backpropagation, the value of gradient decreases significantly, thus hardly any change comes to weights. To overcome this, ResNet is used. It make use of “SKIP CONNECTION” which lies at the core of the residual blocks, is the strength of this type of neural network.

All algorithms train on the output ‘Y’ but, ResNet trains on F(X). In simpler words, ResNet tries to make F(X)=0 so that Y=X.

ResNet Architecture
The 50-layer ResNet architecture includes the following elements, as shown in the table below:

![resnet](https://user-images.githubusercontent.com/105699438/230710955-2be90d79-dfa8-47a5-b14d-5cbb1efaab59.png)

@ A 7×7 kernel convolution alongside 64 other kernels with a 2-sized stride. <br/>
@ A max pooling layer with a 2-sized stride. <br/>
@ 9 more layers 3×3,64 kernel convolution, another with 1×1,64 kernels, and a third with 1×1,256 kernels. These 3 layers are repeated 3 times. <br/>
@ 12 more layers with 1×1,128 kernels, 3×3,128 kernels, and 1×1,512 kernels, iterated 4 times. <br/>
@ 18 more layers with 1×1,256 cores, and 2 cores 3×3,256 and 1×1,1024, iterated 6 times. <br/>
@ 9 more layers with 1×1,512 cores, 3×3,512 cores, and 1×1,2048 cores iterated 3 times. <br/>

<p align="center">(up to this point the network has 50 layers)</p>
@Average pooling, followed by a fully connected layer with 1000 nodes, using the softmax activation function. <br/>

# ResNet-50 Transfer Learning with Keras

Transfer learning means taking a pre-trained machine learning model and repurposing it for another related task for faster development. You can load a pretrained version of the neural network trained on more than a million images from the ImageNet database. The pretrained neural network can classify images into 1000 object categories, such as keyboard, mouse, pencil, and many animals. As a result, the neural network has learned rich feature representations for a wide range of images. It helps achieve higher performance even if the model is trained on a smaller dataset.
