# Post-Upsampling Super Resolution

In Pre-upsampling, the feature extraction occurs in the HR space. The computational power required is also on the higher end because of that. PUSR extracts in the LR space and Upsamples *in the end.* 
Instead of using simple Bicubic interpolation, a learned upsampling (Deconvolution/subpixel convolution) is used, making the network trainable from end to end.

## FSRCNN
![[Pasted image 20220129140937.png]]
```ad-info
title: FSRCNN

1. Post-upsampling, feature extraction in a lower res space.
2. 1x1 convo after the initial 5x5 convo to reduce the number of channels. Resulting in lesser computation and memory. [Inception Network](https://blog.paperspace.com/popular-deep-learning-architectures-resnet-inceptionv3-squeezenet/)
	- The above article also contains ResNet and SqueezeNet
3. Multiple 3x3 convolutions are used instead of having one big Convolutional filter. Simplifying the architecture, reducing the number of parameters.
4. Learned deconvolutional filter upsampling.

```

## ESPCN
##### Why Sub-pixel over Deconv?
Introduces sub-pixel convolution to replace the deconvolutional layer for upsampling. 
1. Deconvolution happens in high resolution space so it's computationally expensive.
2. Resolvs the *checkerboard issue*.
![[Pasted image 20220129154808.png]]
##### Sub-pixel Convolution
![[Pasted image 20220129160755.png]]
Works by converting *depth to space*.
