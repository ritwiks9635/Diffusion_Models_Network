# Diffusion_Models_Network
Diffusion Models are generative models, meaning that they are used to generate data similar to the data on which they are trained. Fundamentally, Diffusion Models work by destroying training data through the successive addition of Gaussian noise, and then learning to recover the data by reversing this noising process.

![](https://lilianweng.github.io/posts/2021-07-11-diffusion-models/unCLIP.png)

##**What are diffusion models used for?**
Diffusion models are powerful content-based image retrieval techniques that can be applied to image search tasks. Using the reverse diffusion process, the first step in using diffusion models for image search is to encode the images in a latent space.

Diffusion models are a type of generative model that use a two-step training process to generate images:
1. Forward diffusion: The model takes a clear image as input and adds noise to it iteratively.
2. Reverse diffusion: The model tries to reconstruct the original image from the noisy version. 

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQz6Dqs1c2Np93X_O5IR8jP9xQuAj07zIYSbg&usqp=CAU)

**Diffusion process**

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ4l-LKWZr3pjIH0ZXq5s7DfHAzTgu_qQG7Sg&usqp=CAU)

The basic idea behind diffusion models is rather simple. They take the input image 
𝑥
0
x 
0
​
  and gradually add Gaussian noise to it through a series of 
𝑇
T steps. We will call this the forward process. Notably, this is unrelated to the forward pass of a neural network. If you'd like, this part is necessary to generate the targets for our neural network (the image after applying 
𝑡
<
𝑇
t<T noise steps).

Afterward, a neural network is trained to recover the original data by reversing the noising process. By being able to model the reverse process, we can generate new data. This is the so-called reverse diffusion process or, in general, the sampling process of a generative model.
