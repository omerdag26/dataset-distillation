# Efficient Dataset Distillation for Cat and Dog Image Classification

## Project Overview

This project explores the application of dataset distillation techniques for the task of cat and dog image classification. Dataset distillation aims to create a smaller, synthetic dataset that retains the essential information of a larger one, thus reducing computational requirements while maintaining performance.

## Methodology

### Convolutional Neural Network (ConvNet)
We developed a convolutional neural network (ConvNet) as our primary model for the classification task. Our baseline performance using the entire dataset resulted in an accuracy of 91%.

### Data Augmentation
To investigate the impact of data augmentation, we applied various transformations such as rotation, flipping, and scaling to the images. However, this approach led to a decrease in accuracy, achieving only 77% for 10% of the data at random.

### Random Sampling
We also experimented with random sampling of the dataset, selecting 10% of the data at random. This method resulted in an accuracy of 76%, indicating that naive downsampling can lead to a significant loss of important information.

### Clustering
Finally, we applied a clustering-based approach to select a representative subset of the data. By clustering the images and selecting key samples from each cluster, we distilled the dataset down to 10% of its original size. This method yielded an accuracy of 89%, demonstrating that clustering can effectively preserve critical information with a much smaller dataset.

## Results Summary

| Method               | Accuracy |
|----------------------|----------|
| Baseline (Full Data) | 91%      |
| Data Augmentation    | 77%      |
| Random Sampling      | 76%      |
| Clustering           | 89%      |

## Conclusion

The results highlight the potential of dataset distillation techniques, particularly clustering, in maintaining high classification accuracy with significantly reduced data. This approach not only saves computational resources but also speeds up the training process, making it a valuable strategy for efficient machine learning.
