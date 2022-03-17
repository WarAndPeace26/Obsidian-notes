# Pre-Upsampling Super Resolution

1. Bicubic-interpolation
2. Deep learning

## SRCNN
![[Pasted image 20220129111229.png]]
```ad-info
title: SRCNN (Dec 2014)

Three layers:
1. Patch Extraction
	- Extract dense patch and represent using convolutional filters.
2. Non-linear mapping
	- 1x1 convolutional filters used to change the number of channels and add non-linearity.
3. Reconstruction
	- Reconstructs I<sub>y</sub>
	
Loss function: **MSE**
Evaluation: **PSNR**
```

## Very Deep Super Resolution

![[Pasted image 20220129120404.png]]
```ad-info
title: VDSR

An improvement on SRCNN adding
1. A deep network with small 3x3 convolutional filters based on the [VGG architecture](https://blog.paperspace.com/popular-deep-learning-architectures-alexnet-vgg-googlenet/)
2. Tries to learn *residual of the output image and the interpolated input* rather than the *direct mapping* (like SRCNN), as shown in the figure above. The initial LR image is added to the network output.
3. **Gradient Clipping** is used to train the deep network with higher learning rates. 

```
