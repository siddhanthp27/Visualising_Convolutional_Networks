# Visualising_Convolutional_Networks

In this repository, I have tried to implement the work presented in ["Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps"](https://arxiv.org/pdf/1312.6034.pdf) by Simonyan et al. The gradient of the class score is calculated w.r.t. the input image, which maximises the class score. This generates an image which visualises the notion of the class as seen by the Convolutional Network. 

In this implementation, I have used the [CIFAR 10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html). 'CIFAR_visualisation.ipynb' will help visualize the different images of the dataset. 

'Deconv - Gradient.ipynb' and 'CIFAR_binfiles_training.ipynb' generate visualisations for all the layers of the Convolutional Network. As we can see from the output images, the relevant patterns that correspond to the particular digit class are highlighted in the input images. The only difference between the two is that in 'CIFAR_binfiles_training.ipynb' we have used a Average Pooling Layer toward the end of the ConvNet. 

In order to confirm that the patterns being highlighted in the data were due to the patterns corresponding to the digits and not noise patterns in the dataset, I generated large images with the digits arbitrarily placed on one corner of the image. The generation process is shown in 'Data Generator.ipynb'. 

The model is trained in 'Deconv - Gradient - GAP - Big.ipynb'. As we can see from the results, the patterns being recognized in the images are due to the input digits itself and not noise in the dataset. 
