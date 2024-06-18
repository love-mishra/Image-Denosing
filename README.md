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
### Preprocessing
- We resize the images as (600,400)
- then convert them into gray 'L'
- rescale the images to 255 
- and then reshape the images into (400,600,1)
### Model
- This contain two part first encoder and second decoder part.
<br>*Encoder*:</br>
- It consists two CNN operation and two max pooling operation
- First operation has 64 filter as size of (3,3) and second has 32 filter as size of (3,3)
- and in both cnn operation max pooling operation has kernel of size (2,2)
<br>*Decoder*</br>
- Decoder part has two upsampling operation and one cnn operation 
- Both has kernel of size of (3,3) and 32 kernel
- last we have output cnn operation which has size (3,3) and one kernel
- We compile our model using adadelta optimization algorithm and binary cross entropy loss 
- We use split the train data into train and val and then perform early stopping concept
### Evaluation 
- We use our train model on test low images and then predict the denoised images then calculate their psnr value corresponding to ground denoised images present in test folder.
- mean psnr value I get for my test dataset is around 17.
