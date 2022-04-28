
# **Autoencoder-Guided GAN for Minority-Class Cloth-Changing Gait Data Generation**

## Motivation

In the gait recognition task, cloth-changing data (e.g., CL-class data in the CASIA-B dataset) account for a very low proportion of the gait dataset, which brings serious recognition accuracy degradation to gait recognition algorithm in clothes changing scenarios. One way to solve this problem is to use data generation algorithms to expand the cloth-changing data. When facing the generation of minority-class Data, the existing GAN-based image data expansion algorithms require a large amount of data to ensure the convergence and can cause mode collapse due to the conflict between the true-false discriminant loss and the classification loss. In order to solve the above problems, we propose an autoencoder-guided GAN for cloth-changing gait data generation, which uses the autoencoder with embedding layer to extract the data features of the entire data set, rather than only extracting the data features of the required CL data. Then the labeled latent vector (representing the extracted data features) in the autoencoder is taken as the input of the GAN, solving the problem that GAN convergence requires a lot of training data. The GAN has the same topology as the autoencoder and uses the parameter matrix of the autoencoder as the initial weights. Secondly, the true classification in GAN is canceled, and only the false classification is retained, which solves the problem of the collision of the loss function between the true-false discrimination and the classification discrimination. 

## Generated Silhouettes

​                               ![image-20220428201014722](C:\Users\xjxjx\AppData\Roaming\Typora\typora-user-images\image-20220428201014722.png)

## SSIM Comparison

![image](https://github.com/sspBIT/Autoencoder-Guided-GAN-for-Minority-Class-Cloth-Changing-Gait-Data-Generation/blob/main/%E5%9B%BE%E7%89%871.svg)

## Gait Recognition Network Accuracy

### Original Dataset

CASIA-B: 6 sets of NM and 2 sets of CL

### Expansion Method

Ours, ACGAN, Rebooting ACGAN,Copying, Noise injection

### Gait Recognition Network

GaitSet, GaitPart, GEINet

### Size

6 sets of NM and 6 sets of CL

### Accuracy Comparison

​                                                                                                    Comparison of the recognition accuracy of GaitSet

![image-20220428201631083](C:\Users\xjxjx\AppData\Roaming\Typora\typora-user-images\image-20220428201631083.png)



​                                                                                                     Comparison of the recognition accuracy of GaitPart

![image-20220428201640333](C:\Users\xjxjx\AppData\Roaming\Typora\typora-user-images\image-20220428201640333.png)



​                                                                                                     Comparison of the recognition accuracy of GaitSet

![image-20220428201646518](C:\Users\xjxjx\AppData\Roaming\Typora\typora-user-images\image-20220428201646518.png)



We are in the process of extending our algorithm to other gait datasets such as OU-MVLP, and when this work is complete we will open source our code.
