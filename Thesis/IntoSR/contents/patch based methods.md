#topics 
# Patch Based Methods
***
Given a set of paired LR and HR training images, patches can be cropped from the training images to learn **[[mapping functions]]**. The exemplar patches can be generated from external datasets ([[Example-based super-resolution]], [[Super-resolution through neighbor embedding]]), the input image itself [[Super-resolution from a single image]], [[Image and video upscaling from local self-examples]], or combined sources [44]. 

Various learning methods of the mapping functions have been proposed such as 
1. **weighted average** 31, [[Super-resolution through neighbor embedding]], 
2. kernel regression [17], 
3. support vector regression [23], 
4. Gaussian process regression [[Single image super-resolution using Gaussian process regression]], 
5. sparse dictionary representation 46, [[Single image super-resolution using sparse representation]], [[Image deblurring and super-resolution by adaptive sparse domain selection and adaptive regularization]], 24, 45, 39, 47, 19, 14. 

In addition to *equally averaging overlapped patches*, several methods for *blending overlapped pixels* have been proposed including weighted averaging [[Super-resolution from a single image]], 44, **Markov Random Fields ([[Example-based super-resolution]])**, and Conditional Random Fields [38].
