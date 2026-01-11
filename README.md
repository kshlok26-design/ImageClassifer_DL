Image Classification: Custom CNN vs. Transfer Learning
This repository demonstrates a comparative approach to image classification using two distinct Deep Learning strategies: a Custom Convolutional Neural Network (CNN) and Transfer Learning with MobileNetV2.

🚀 Project Overview
The goal of this project was to evaluate the performance difference between building a model from scratch and leveraging state-of-the-art pre-trained architectures for image recognition tasks.

1. Custom CNN Architecture
A "from-scratch" approach designed to learn specific spatial features of the dataset.

Layers: Multiple Conv2D and MaxPooling2D blocks for feature extraction.

Regularization: Integrated Dropout layers to mitigate overfitting during the training phase.

Outcome: Serves as a baseline to understand the complexity required for the specific dataset.

2. Transfer Learning (MobileNetV2)
Utilizes the MobileNetV2 model pre-trained on the ImageNet dataset as a powerful feature extractor.

Base Model: Frozen weights from ImageNet to preserve general visual knowledge (edges, textures, shapes).

Custom Head: Added Global Average Pooling and specialized Dense layers for the final classification.

Fine-Tuning: Implemented a two-stage training process where the base layers were eventually unfrozen at a very low learning rate to optimize performance.

📁 Project Structure
improved_image_classifier.ipynb: The main notebook containing data preprocessing, model architecture, training, and evaluation.

test images/: A collection of sample images used to verify the model's predictive power.

Results/: Visualizations of training accuracy and loss curves.

.gitignore: Configured to exclude heavy data/ folders and .keras model files to keep the repository lightweight.

📊 Results
The training process involves monitoring both training and validation metrics.
