# CIFAR-10 Image Classification with EfficientNetV2B1, Label Smoothing, and Multitask Learning

## Overview

This Jupyter notebook demonstrates an approach to CIFAR-10 image classification using the EfficientNetV2B1 architecture, label smoothing, and multitask learning. The goal is to achieve accurate and robust predictions for the CIFAR-10 dataset, which contains a diverse set of images belonging to ten different classes.

## Approach

1. **Architecture**: The EfficientNetV2B1 architecture is employed as the backbone of the image classification model with a classifier that has two outputs stacked upon it..

2. **Label Smoothing**: The model benefits from label smoothing, a technique that enhances robustness by transforming class labels into multi-dimensional vectors. In this transformed vector, the true class is assigned a probability of 1 minus the smoothing factor, while the probabilities of other classes are each set to the smoothing factor divided by the number of classes minus one. This adjustment helps the network generalize more effectively and adapt to varying degrees of uncertainty.

3. **Multitask Learning**: Multitask learning is applied to predict both class labels and the presence of animals within the images. This approach optimizes predictive accuracy by sharing knowledge between related tasks and helps the model to eliminate a significant number of mistakes.

## Insights

Through manual error analysis, recurring patterns contributing to erroneous predictions were identified. These patterns include challenges like cluttered backgrounds, partially occluded objects, color influences, contextual cues, unusual animal poses, and distinctive features. Also we have found mislabellings in the test set. Addressing these challenges can further refine the model's performance.

## Results

The approach outlined in this notebook yielded promising results (91% of test accuracy without fine-tuning and 97% of test accuracy after fine-tuning), showcasing improved accuracy and robustness in CIFAR-10 image classification.

## Future Directions

As a basis for further improvements, we consider exploring the following:
- Fine-tuning hyperparameters to optimize model performance.
- Incorporating additional data augmentation techniques to enhance model generalization.
- Experimenting with alternative architectures to uncover new insights.
