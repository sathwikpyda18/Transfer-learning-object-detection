# Transfer Learning with ResNet50 on CIFAR-10

This project involves applying transfer learning using the ResNet50 architecture to classify images from the CIFAR-10 dataset. The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 different classes, with 6,000 images per class.

## Project Description

### Dataset

- **Dataset Source**: [Kaggle: CIFAR-10 - Object Recognition in Images](https://www.kaggle.com/c/cifar-10)
- **Classes**: Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck
- **Training Images**: 50,000
- **Test Images**: 10,000

### Transfer Learning

- **Pre-trained Model**: ResNet50
    - ResNet50 is a deep convolutional neural network that has been pre-trained on the ImageNet dataset, which contains over a million images and 1,000 classes.
    - Transfer learning allows us to leverage the pre-trained weights and architecture of ResNet50 and fine-tune it for our specific task of classifying CIFAR-10 images.

### Implementation

1. **Data Preprocessing**:
    - Normalized the pixel values to be between 0 and 1.
    - One-hot encoded the class labels.

2. **Model Architecture**:
    - Loaded the ResNet50 model with pre-trained ImageNet weights.
    - Replaced the top layer of ResNet50 with a new dense layer suitable for CIFAR-10 classification (10 classes).
