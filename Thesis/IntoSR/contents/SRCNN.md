#Papers 
# [Image Super-Resolution Using Deep Convolutional Networks](https://arxiv.org/pdf/1501.00092.pdf)
***
The *sparse-coding-based method* [[Image super-resolution as sparse representation of raw image patches]], [[Image super-resolution via sparse representation]] is one of the
representative *external example-based SR methods*. 
## This method involves several steps in its solution pipeline.
1. Overlapping patches are densely cropped from the input image and pre-processed (e.g.,subtracting mean and normalization).
2. These patches are then encoded by a low-resolution dictionary. 
3. The sparse coefficients are passed into a high-resolution dictionary for reconstructing high-resolution patches. 
4. The overlapping re-constructed patches are aggregated (e.g., by weighted averaging) to produce the final output. 

This pipeline is shared by most external example-based methods, which pay particular attention to learning and optimizing the **[[dictionaries]]** [2], [49], [50] or building efficient *mapping functions* [25], [41], [42], [47]. However, the rest of the steps in the pipeline have been rarely optimized or considered in an unified optimization framework. In this paper, we show that the aforementioned pipeline is equivalent to a deep convolutional neural network [27] (more details in Section 3.2).

## 3 CONVOLUTIONAL NEURAL NETWORKS SUPER-RESOLUTION
#### 3.1 Formulation
Consider a single low-resolution image, we first upscale it to the desired size using [[bicubic interpolation]], which is the only pre-processing we perform<sup>3</sup> . Let us denote the interpolated image as Y. Our goal is to recover from Y an image F (Y) that is as similar as possible to the ground truth high-resolution image X. For the ease of presentation, we still call Y a “low-resolution” image, although it has the same size as X. We wish to learn a mapping F , which conceptually consists of three operations:

1) **Patch extraction and representation:** this operation extracts (overlapping) patches from the low-resolution image Y and represents each patch as a high-dimensional vector. These vectors comprise a set of feature maps, of which the number equals to the dimensionality of the vectors.
2) **Non-linear mapping:** this operation nonlinearly maps each high-dimensional vector onto another high-dimensional vector. Each mapped vector is conceptually the representation of a high-resolution patch. These vectors comprise another set of feature maps.
3) **Reconstruction:** this operation aggregates the above high-resolution patch-wise representations to generate the final high-resolution image. This image is expected to be similar to the ground truth X.


We will show that all these operations form a convolutional neural network. An overview of the network is depicted in Figure 2. Next we detail our definition of each operation.

![[Pasted image 20220302044411.png]]


##### [Code](https://github.com/titu1994/Image-Super-Resolution)