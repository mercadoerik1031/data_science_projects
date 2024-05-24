# CIFAR-10 Image Classification Using Convolutional Neural Networks (CNN)

## Description
This Jupyter notebook demonstrates the process of building and training a convolutional neural network (CNN) to classify images from the CIFAR-10 dataset. The notebook includes comprehensive steps from data loading and preprocessing, model architecture design, training, and evaluation.

## Contents
1. **Imports**: All necessary libraries and modules are imported at the beginning of the notebook.
2. **Data Loading**: The CIFAR-10 dataset is loaded into the notebook.
3. **Preprocessing**:
   - The image data is normalized to scale the pixel values between 0 and 1.
   - Data is split into training, validation, and test sets.
   - Labels are one-hot encoded.
4. **Model Building**:
   - A CNN architecture is defined using Keras.
   - Layers include Conv2D, AveragePooling2D, Flatten, and Dense layers, with BatchNormalization and Dropout for regularization.
5. **Data Augmentation**: Implemented to improve model generalization.
6. **Model Training**:
   - The model is compiled and trained using the Adam optimizer and categorical cross-entropy loss function.
   - Training is performed with early stopping and model checkpoint callbacks to save the best model based on validation loss.
7. **Evaluation**: Model performance is evaluated using the validation set.

## Usage
To run this notebook:
- Ensure you have Jupyter Notebook or JupyterLab installed.
- Open the notebook in Jupyter.
- Run the cells sequentially to observe the workflow from data loading to model evaluation.


## Authors
Geraldine Nnene, Xuying Yuki Yu, Erik Mercado
