# csphw2

Project 1: Training StyleGAN to Generate Realistic Faces
https://towardsdatascience.com/explained-a-style-based-generator-architecture-for-gans-generating-and-tuning-realistic-6cb2be0f431
https://www.youtube.com/watch?v=kSLJriaOumA

## Description:
Generative Adversarial Networks (GAN) is an architecture introduced by Ian Goodfellow and his colleagues in 2014 for generative modeling, which is using a model to generate new samples that imitate an existing dataset. It is composed of two networks: the generator that generates new samples, and the discriminator that detects fake samples. The generator tries to fool the discriminator while the discriminator tries to detect samples synthesized by the generator.StyleGAN generates the artificial image gradually, starting from a very low resolution and continuing to a high resolution (1024×1024).

## Components/inputs:
-2 Neural Networks: A Generator (learns to generate plausible data. The generated instances become negative training examples for the discriminator) and a Discriminator (learns to generate plausible data. The generated instances become negative training examples for the discriminator)
-Noise/random input/latent code
-Sample images

## Process:
-With this technique, first the network learns the base components of the image - starting out with a very low resolution version of it (4 x 4 px). As time goes on, resolution is increased and more details are learned. Training low-res images 
first makes it faster and easier to train high-res images in the long run.
-The generator inputs a random vector/noise and at first outputs noise as well. With more training, it gets feedback from the descriminator, comparing the generated samples with the real ones, and works to improve the result.
-The generator separates the image into three "styles" 

The styles are divided into 3 types:
-Coarse (resolution of up to 82 - affects pose, general hair style, face shape, etc)
-Middle (res of 162 to 322 - affects finer facial features, hair style, eyes open/closed, etc)
-Fine (res of 642 x 10242 - affects color scheme (eye, hair and skin) and micro features)

![diagram](https://developers.google.com/machine-learning/gan/images/gan_diagram.svg)


## Bjork's AI Generated Soundtrack 

https://www.youtube.com/watch?time_continue=10&v=HXSSA064EEs&feature=emb_title

# Description: Collaborating with New York’s design-centric Sister City hotel and Microsoft, the result is Kórsafn—an AI-powered composition that builds on the generative soundscape concept that Sister City launched with Julianna Barwick in 2019. In Icelandic, “kór” = “choral,” and “safn” = “archives.”

# Input:
- All kinds of weather data (temperature, barometric pressure, sunrises, sunsets)
-Choral Arrangements
-Camera footage from a rooftop

# Process:
-The AI, depending on the kind of data it receives, makes sounds that have been pre-recorded by a choir and Bjork herself. As it learns more and more, eventually it starts separating between different events that happen in the video footage; such as birds migrating, etc and plays adjusted sounds depending on everything that it thinks happens 
-It doesn’t just find clouds, but denotes the density and type of cloud, whether cumulus or nimbus. And it won’t just find a bird, but will also distinguish an entire flock of birds (from Microsoft)
