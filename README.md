# Generative Modelling using Autoencoders

### This repository contains jupyter notebooks on autoencoders using keras. The main aim of this repository was to **explore latent space representation of autoencoder(s)**.
I have explored the latent space for Standard Autoencoders and Variational Autoencoders. 

---

#### Dataset used - MNIST

---

### Standard Autoencoders 
The latent space for standard autoencoders may not be continous and hence it can't be used as a generative model. It just learns to replicate the data.
But if we're building a generative model, we just don't want to replicate the same image but want to randomly sample from the latent space, or generate variations on an input image,
from a continous space.

#### Architecture of Standard Autoencoder
![Standard Architecure](https://github.com/behlvaibhav/Autoencoders_using_keras/blob/master/Visuals/ae.jpg)



#### The latent space of a standard (deep) autoencoder looks something like this:

![Standard Autoencoder Latent Space](https://github.com/behlvaibhav/Autoencoders_using_keras/blob/master/Visuals/deep_latent_space.gif)

---

### Variational Autoencoders 
Unlike standard autoencoders, variational autoencoders have continous latent space (by design) allowing easy random sampling and interpolation, which makes it easy for generative modelling. 
It is possible due to the fact that the ouput of encoder in variational differs from standard (vanilla) autoencoders. Instead of just outputting an encoding vector of size n, it generates two outputting vectors of size n:
a vector of means, μ and another vector of standard deviations, σ.

Basically, the mean vector controls where the encoding vector should be centered around, while the standard deviation controls the "area", how much from the mean encoding can vary. As encodings are generated at random from anywhere inside the "circle" (the distribution), the decoder learns that not only is a single point in latent space referring to a sample of that class, but all nearby points refer to the same as well.

#### Architecture of a Variational Autoencoder
![Variatonal Architecture](https://github.com/behlvaibhav/Autoencoders_using_keras/blob/master/Visuals/vae.png)

#### The latent space of a variational autoencoder looks something like this:
![latent space vae](https://github.com/behlvaibhav/Autoencoders_using_keras/blob/master/Visuals/Variational_latent_space.gif)

**The difference between the latent space(s) is clear from the above visuals.**

---

### References 
[1] https://towardsdatascience.com/intuitively-understanding-variational-autoencoders-1bfe67eb5daf

---
***P.S. Apologies for the quality of gifs.***
