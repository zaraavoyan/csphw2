# csphw2

Project 1: Training StyleGAN to Generate Realistic Faces
https://towardsdatascience.com/explained-a-style-based-generator-architecture-for-gans-generating-and-tuning-realistic-6cb2be0f431
https://www.youtube.com/watch?v=kSLJriaOumA

##Description:
Generative Adversarial Networks (GAN) is an architecture introduced by Ian Goodfellow and his colleagues in 2014 for generative modeling, which is using a model to generate new samples that imitate an existing dataset. It is composed of two networks: the generator that generates new samples, and the discriminator that detects fake samples. The generator tries to fool the discriminator while the discriminator tries to detect samples synthesized by the generator.StyleGAN generates the artificial image gradually, starting from a very low resolution and continuing to a high resolution (1024×1024).

##Components/inputs:
-2 Neural Networks: A Generator (learns to generate plausible data. The generated instances become negative training examples for the discriminator) and a Discriminator (learns to generate plausible data. The generated instances become negative training examples for the discriminator)
-Noise/random input/latent code
-Sample images

##Process:
-With this technique, first the network learns the base components of the image - starting out with a very low resolution version of it (4 x 4 px). As time goes on, resolution is increased and more details are learned. Training low-res images 
first makes it faster and easier to train high-res images in the long run.
-The generator inputs a random vector/noise and at first outputs noise as well. With more training, it gets feedback from the descriminator, comparing the generated samples with the real ones, and works to improve the result.
-The generator separates the image into three "styles" 

The styles are divided into 3 types:
-Coarse (resolution of up to 82 - affects pose, general hair style, face shape, etc)
-Middle (res of 162 to 322 - affects finer facial features, hair style, eyes open/closed, etc)
-Fine (res of 642 x 10242 - affects color scheme (eye, hair and skin) and micro features)

![diagram](https://developers.google.com/machine-learning/gan/images/gan_diagram.svg)



