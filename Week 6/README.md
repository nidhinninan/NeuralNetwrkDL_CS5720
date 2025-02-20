# CNN Implementation for CIFAR-10 Image Classification
## In-Class Programming Assignment 5 (Week 6)  

**Github Repo Link:** https://github.com/nidhinninan/NeuralNetwrkDL_CS5720.git 

**Name:** Nidhin Ninan

**ID:** 700772413

## Description
This repository contains an implementation of a Convolutional Neural Network (CNN) for classifying images from the CIFAR-10 dataset using Keras and TensorFlow.

### **File:** `Week5_NN_1a.ipynb`  
**Video Link**: Problem 1a - https://drive.google.com/file/d/1i5ig7v0SNeXzLY9DvCpTcIdHnHgreRSZ/view?usp=drive_link

### Model Architecture Summary
The CNN model consists of multiple layers:
1. Input Layer:
   - Convolutional layer with 32 filters (3x3 kernel)
   - ReLU activation
   - Dropout (20%)

2. Feature Extraction Layers:
   - Multiple convolutional layers (32, 64, and 128 filters)
   - Max pooling layers (2x2)
   - Dropout layers for regularization

3. Classification Layers:
   - Flatten layer
   - Dense layers (1024 and 512 units)
   - Output layer with softmax activation (10 classes)

### Neural Net Architecture
#### **1. Convolutional Layers**
- **Convolutional Input Layer:** 32 filters, 3×3 kernel, ReLU activation, with kernel constraint.
- **Dropout Layer:** 20% dropout.
- **Convolutional Layer:** 32 filters, 3×3 kernel, ReLU activation.
- **Max Pooling Layer:** 2×2 pool.
- **Convolutional Layer:** 64 filters, 3×3 kernel, ReLU activation.
- **Dropout Layer:** 20% dropout.
- **Convolutional Layer:** 64 filters, 3×3 kernel, ReLU activation.
- **Max Pooling Layer:** 2×2 pool.
- **Convolutional Layer:** 128 filters, 3×3 kernel, ReLU activation.
- **Dropout Layer:** 20% dropout.
- **Convolutional Layer:** 128 filters, 3×3 kernel, ReLU activation.
- **Max Pooling Layer:** 2×2 pool.

#### **2. Fully Connected Layers**
- **Flatten Layer:** Converts feature maps into a 1D vector.
- **Dropout Layer:** 20% dropout.
- **Fully Connected Layer:** 1024 units, ReLU activation.
- **Dropout Layer:** 20% dropout.
- **Fully Connected Layer:** 512 units, ReLU activation.
- **Dropout Layer:** 20% dropout.

#### **3. Output Layer**
- **Fully Connected Output Layer:** 10 units, Softmax activation (for classification).

## Implementation Details

### Data Processing:
- Loading CIFAR-10 dataset (50,000 training and 10,000 test images)
- Normalizing pixel values to [0,1]
- One-hot encoding of labels
- Data splitting into training and test sets

### Model Training:
- Optimizer: Stochastic Gradient Descent (SGD)
- Learning rate: 0.01 with decay
- Epochs: 60
- Batch size: 32
- Loss function: Categorical crossentropy

### Visualization:
- Training and validation accuracy plots
- Training and validation loss plots
- Sample predictions with actual vs predicted labels
- Test image visualization

## Features
- Implementation of deep CNN architecture
- Dropout layers for preventing overfitting
- MaxNorm constraints for weight regularization
- Comprehensive model evaluation
- Visual performance analysis

## Dependencies
- Python 3.x
- TensorFlow/Keras
- NumPy
- Matplotlib
- CIFAR-10 dataset (automatically downloaded via Keras)

## Usage
1. Ensure all required packages are installed:
   ```bash
   pip install tensorflow numpy matplotlib
   ```

## Model Performance
- The model evaluates performance on test data
- Displays accuracy metrics
- Shows predictions vs actual labels for sample images
- Visualizes learning curves

## Visualization Outputs
- Training progress plots
- Sample image predictions
- Model architecture summary

## Notes
- Random seed is set to 7 for reproducibility
- Model includes regularization techniques (Dropout, MaxNorm)
- Learning rate decay is implemented for training optimization

## Acknowledgments
- CIFAR-10 dataset provided by the Canadian Institute For Advanced Research
- Implementation based on Keras deep learning framework
