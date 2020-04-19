# Celebrities faces generator



## Project Overview
in this proyect we'll be define and train a DCGAN on a dataset of faces. The goal is to get a generator network to generate new images of faces that look as realistic as possible!

## Sample images from Dataset
![Sample Output](https://raw.githubusercontent.com/lcarcamo1526/Celeb-faces-generator/master/assets/processed_face_data.png)


## Specs:
* **GPU**: Nvidia GTX 1060 3G
*  **RAM** 16 GB DDR4
* **CPU**: CPU RYZEN 2600 12 CORES
* **Training Time** : 1 Hour
* **No Epochs: 20**
* **Discriminator Optimizer: Adam**
* **Generator Optimizer: Adam**
* **Learning Rate: 0.0001**
* **Batch Size : 32**




# Datasets

* Download the [Celeb dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)



## Discriminator Arch
    Discriminator(
      (cnn1): Sequential(
        (0): Conv2d(3, 64, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
      )
      (cnn2): Sequential(
        (0): Conv2d(64, 128, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
        (1): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      )
      (cnn3): Sequential(
        (0): Conv2d(128, 256, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
        (1): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      )
      (cnn4): Sequential(
        (0): Conv2d(256, 512, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
        (1): BatchNorm2d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      )
      (dropout): Dropout(p=0.4, inplace=False)
      (fc1): Linear(in_features=2048, out_features=1, bias=True)
    )


## Generator ARCH
    Generator(
      (fc1): Linear(in_features=100, out_features=2048, bias=True)
      (tcnn1): Sequential(
        (0): ConvTranspose2d(512, 256, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
        (1): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      )
      (tcnn2): Sequential(
        (0): ConvTranspose2d(256, 128, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
        (1): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      )
      (tcnn3): Sequential(
        (0): ConvTranspose2d(128, 64, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
        (1): BatchNorm2d(64, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
      )
      (tcnn4): Sequential(
        (0): ConvTranspose2d(64, 3, kernel_size=(4, 4), stride=(2, 2), padding=(1, 1), bias=False)
      )
      (dropout): Dropout(p=0.4, inplace=False)
    )


-----

## Sample Output











