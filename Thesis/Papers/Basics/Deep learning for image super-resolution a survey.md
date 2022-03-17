#Papers 
# Deep Learning for Image Super-resolution: A Survey
***

a variety of classical SR methods have been proposed, including prediction-based methods [10], [11], [12], edge-based methods [13], [14], statistical methods [15], [16], patch-based methods [13], [17], [18], [19] and sparse representation methods [20], [21]

In general, the family of SR algorithms using deep learning techniques differ from each other in the following major aspects: different types of network architectures [26], [27], [28], different types of loss functions [8], [29], [30], different types of learning principles and strategies [8], [31], [32], etc.
***
## 2.3 Image Quality Assessment
### PSNR

![[Pasted image 20220309235536.png]]
```ad-note
title: PSNR

PSNR is defined via the maximum pixel value (denoted as L) and the mean squared error (MSE) between images.

```

### SSIM
![[Pasted image 20220310002718.png]]
![[Pasted image 20220312082051.png]]
![[Pasted image 20220312082118.png]]
```ad-note
title: SSIM

the structural similarity index (SSIM) [58] is proposed for measuring the structural similarity between images, based on independent comparisons in terms of **luminance, contrast, and structures**.

```

### Learning based perceptual quality
***
## 3.1 SR Frameworks
###### [Super Resolution is an Ill-posed problem](https://homepages.inf.ed.ac.uk/rbf/CVonline/LOCAL_COPIES/AV1011/Super_Resolution_CVonline.pdf)

### Pre-upsampling
### Post-upsampling
### Progressive-upsampling
### Iterative up and down upsampling
