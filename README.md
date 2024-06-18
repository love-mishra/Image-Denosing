# Image-Denosing
### Introduction 
- This project involves a model which takes noisy image data and then convert them into denoised images.
- This model is simple autoencoder model which convert the input denoised image into latent space and then by upsampling convert them into denoised output image.
- We train our model using Train data and then we use this model for 
testing purpose.
### Dataset
- We have a Train and test dataset 
- Train Dataset contain low and high images where low image is noised image and high image is denoised image .
- Test dataset has low and  ground images where low images are noisy and ground images are denoisy .
### Evaluation 
- We use our train model on test low images and then predict the denoised images then calculate their psnr value corresponding to ground denoised images present in test folder.