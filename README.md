# Crater Detection on Mars Using Deep Learning

## Overview

This repository contains the implementation of a U-Net++ model with a ResNeSt200e encoder for automating crater detection on the surface of Mars. The project uses high-resolution THEMIS infrared images and the Robbins & Hynek Mars Crater Dataset (RH2012) to train and evaluate the model. This work aims to assist planetary surface analysis, including impact history studies, hazard detection, and spacecraft navigation.

---

## Project Structure

- **`download_data.ipynb`**: Notebook for downloading and organizing the THEMIS image dataset and annotations.
- **`get_stats.ipynb`**: Computes dataset statistics such as mean and standard deviation of pixel values, used for data normalization.
- **`split_patches.ipynb`**: Splits large THEMIS image tiles into 512 × 512 patches for model training and evaluation.
- **`train_val_test_split.ipynb`**: Splits the dataset into training, validation, and test sets, ensuring balanced latitude coverage.
- **`model_training.ipynb`**: Contains the training pipeline for the U-Net++ model, including data augmentation, model configuration, and performance monitoring.
- **`.gitignore`**: Specifies files and directories to exclude from version control.
- **`LICENSE`**: The license file for the repository.

---

## Key Features

- **Deep Learning Model**: U-Net++ with ResNeSt200e encoder, designed for robust segmentation of craters in high-resolution images.
- **Dataset**: THEMIS daytime infrared mosaic images of Mars, aligned with RH2012 crater annotations.
- **Preprocessing**: Handling of missing pixel regions, normalization using computed mean and standard deviation, and patching of large images.
- **Augmentation**: Random flips, rotations, noise, brightness/contrast adjustment, and blurring for robust training.
- **Metrics and Evaluation**: Precision, recall, IoU, F1-score, accuracy, and loss metrics are tracked and visualized across epochs.

---

## Requirements

- Python 3.8+
- GDAL
- PyTorch
- Albumentations
- segmentation-models-pytorch
- torchmetrics
