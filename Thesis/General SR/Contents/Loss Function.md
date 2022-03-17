#epi-center 
# Loss Function
#### 1| Pixel Loss
***
- Most simple and common
- L2, L1 or other difference metric is used.
- Optimizes PSNR but 
- Doesn't optimize perceptual quality
- Not pleasing to the human eyes
#### 2| Perceptual loss
***
- Tries to match high-level features in a generated image with a given HR
- Takes pre-trained network and uses the difference of feature outputs.
- Was introduced in SRGAN

#### 3| Charbonnier Loss
***
- LapSRN
- Deals better with outliers 
- Produces sharper images compared to L2 loss
- Generally smoother
#### 4| Texture Loss
***
- EnhanceNet
- Tries optimizing *gram matrix* of feature outputs 
- Inspired by Style Transfer loss function
- Captures texture information in an HR image
#### 5| Adversarial loss
***
- Used in all GAN related architectures.
- Helps in fooling *the discriminator* 
- Better perceptual quality
- ESRGAN adds an extra variant of this by using the *relativistic discriminator*
