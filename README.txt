The Pix2Pix Generative Adversarial Network, or GAN, is an approach to training a deep convolutional neural 
network for image-to-image translation tasks.

The careful configuration of architecture as a type of image-conditional GAN allows for both the generation of 
large images compared to prior GAN models (e.g. such as 256×256 pixels) and the capability of performing well 
on a variety of different image-to-image translation tasks.

The approach was presented by Phillip Isola, et al. in their 2016 paper titled “Image-to-Image Translation with 
Conditional Adversarial Networks” and presented at CVPR in 2017.

The GAN architecture is comprised of a generator model for outputting new plausible synthetic images, and a 
discriminator model that classifies images as real (from the dataset) or fake (generated). The discriminator 
model is updated directly, whereas the generator model is updated via the discriminator model. As such, the 
two models are trained simultaneously in an adversarial process where the generator seeks to better fool the 
discriminator and the discriminator seeks to better identify the counterfeit images.

The Pix2Pix model is a type of conditional GAN, or cGAN, where the generation of the output image is conditional
 on an input, in this case, a source image. The discriminator is provided both with a source image and the target
 image and must determine whether the target is a plausible transformation of the source image.

The generator is trained via adversarial loss, which encourages the generator to generate plausible images in the
 target domain. The generator is also updated via L1 loss measured between the generated image and the expected 
output image. This additional loss encourages the generator model to create plausible translations of the source 
image.

S M Ahmed Hassan