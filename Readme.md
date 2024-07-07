
# AI-Generated vs Real Image Categorisation

Luca Pedranzini
Florian Tilliet

All notebooks can be viewed [here](https://nbviewer.org/github/lucapdr1/ai-generated-images-detection/tree/master/) in their html rendered version


## Overview

This repository contains a deep learning project aimed at categorizing images as either AI-generated or real. The project explores various deep learning techniques, model architectures, and data processing methods to enhance the accuracy of image classification.

## Project Structure

The project is divided into several iterations, each with objective of improving upon the previous one or trying a different architecture. This modular approach allows for detailed analysis and comparison of different methodologies and configurations.

### Project Iterations

- **v1.0**: Baseline implementation based on an example project.
- **v1.1**: Subdivision of the baseline into distinct steps with performance evaluation on a laptop.
- **v1.2**: Implementation using ResNet and other similar architectures.
- **v1.3**: Addition of data augmentation and early stopping techniques.
- **v2.0**: Experimentation with a similar dataset.
- **v3.0**: Implementation using Vision Transformer (ViT) architecture.

### Dataset Loading

We decided to use the [CIFAKE: Real and AI-Generated Synthetic Images](https://www.kaggle.com/datasets/birdy654/cifake-real-and-ai-generated-synthetic-images)

## Results
###  [`v1.0-baseline`](https://nbviewer.org/github/lucapdr1/ai-generated-images-detection/tree/master/v1.0-baseline/)
- Adapted and executed a Kaggle deep learning notebook locally to understand its implementation and results.

###  [`v1.1-baseline-steps`](https://nbviewer.org/github/lucapdr1/ai-generated-images-detection/tree/master/v1.1-baseline-steps/)
- **Preprocessing**:
  - CIFake dataset size: ~0.5GB
  - Numpy arrays size: ~2.5GB
  - Processing time: ~1.5min
  - Loading time: ~0.5min
- **Training**:
  - Time: ~10min on Nvidia 950m laptop GPU
  - Model size: 0.5MB
- **Testing**:
  - Fast loading and prediction

###  [`v1.2-tuned-versions`](https://nbviewer.org/github/lucapdr1/ai-generated-images-detection/tree/master/v1.2-tuned-versions/)
- **Fine Tuning**:
  - Training ResNet: ~10 hours on laptop, ~6 hours on Colab/Kaggle free-tier
  - results

###  [`v1.3-data-augmentation`](https://nbviewer.org/github/lucapdr1/ai-generated-images-detection/tree/master/v1.3-data-augmentation/)
- **Data Augmentation and Early Stopping**:
  - Performance was worse than without these techniques
  - Hyperparameter tuning is crucial for optimal performance

###  [`v2.0-new-dataset`](https://nbviewer.org/github/lucapdr1/ai-generated-images-detection/tree/master/v2.0-new-dataset/)
- **Different Dataset (Missing)**:
  - todo

###  [`v3.0-visual-transformers`](https://nbviewer.org/github/lucapdr1/ai-generated-images-detection/tree/master/v3.0-visual-transformer/)
- **Vit**:
  - todo

## Potential Problems
- **Watermarks**: Handling visible and invisible watermarks in images.
- **Image Resizing**: Addressing issues from downsizing or upsizing images of different resolutions.
- **Choosing Generated Images**: Deciding on images generated by specific models or multiple models, and their relevance.
- **Image Types**: Selecting between drawings, specific art styles, photorealistic images, or a combination.
- **Model Performance**: Evaluating older/simpler architectures against newer, complex ones.