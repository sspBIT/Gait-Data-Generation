
# **Autoencoder-Guided GAN for Minority-Class Cloth-Changing Gait Data Generation**

## Motivation

In the gait recognition task, cloth-changing data (e.g., CL-class data in the CASIA-B dataset) account for a very low proportion of the gait dataset, which brings serious recognition accuracy degradation to gait recognition algorithm in clothes changing scenarios. One way to solve this problem is to use data generation algorithms to expand the cloth-changing data. When facing the generation of minority-class Data, the existing GAN-based image data expansion algorithms require a large amount of data to ensure the convergence and can cause mode collapse due to the conflict between the true-false discriminant loss and the classification loss. In order to solve the above problems, we propose an autoencoder-guided GAN for cloth-changing gait data generation.
## Generated Silhouettes


## SSIM Comparison



## Gait Recognition Network Accuracy

### Original Dataset

CASIA-B: 6 sets of NM and 2 sets of CL

### Expansion Method

Ours, ACGAN, Rebooting ACGAN,Copying, Noise injection

### Gait Recognition Network

GaitSet, GaitPart, GEINet

We are in the process of extending our algorithm to other gait datasets such as OU-MVLP, and when this work is completed and the paper is accepted, we will open source our code and results.
