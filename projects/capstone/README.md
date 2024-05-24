# Brain Tumor Segmentation Project

## Problem Statement

The objective of this project is to develop a robust and efficient semantic segmentation model to accurately identify and delineate brain tumors in medical images. Accurate segmentation of brain tumors is crucial for diagnostic purposes, treatment planning, and monitoring the progression of the disease. This task involves differentiating between healthy brain tissue and tumor regions, which can significantly aid radiologists and medical professionals in providing better patient care.

## Dataset Description

[Download Dataset Here](https://www.kaggle.com/datasets/pkdarabi/brain-tumor-image-dataset-semantic-segmentation/data)

The dataset used in this project consists of medical images of brain scans annotated with brain tumor regions. Each image in the dataset is paired with a corresponding mask that highlights the tumor regions. The dataset is structured in the COCO format, which includes categories, images, and annotations.

- **Categories:** The dataset includes one category, "tumor," which represents the brain tumor regions in the images.
- **Images:** The images are medical brain scans, possibly including various imaging modalities like MRI or CT scans.
- **Annotations:** The annotations are in the form of binary masks where the pixel value of 1 indicates the presence of a tumor, and 0 indicates healthy brain tissue.

The dataset is divided into three subsets: training, validation, and testing. This division ensures that the model is trained on one subset, validated on another to tune hyperparameters, and tested on an unseen subset to evaluate its generalization performance.

## Install Necessary Libraries

To start, install the required libraries. The `segmentation-models-pytorch` library is particularly useful as it provides pre-implemented models and utilities tailored for image segmentation tasks, which saves a lot of time and effort compared to implementing these models from scratch.

## Methodology

1. **Setup and Configuration**: Defined configuration parameters such as file paths, model save paths, device (CPU/GPU), batch size, number of epochs, learning rate, patience for early stopping, and a delta for validation loss improvement.

2. **Data Loading**: Loaded the dataset in COCO format by parsing JSON files containing categories, images, and annotations. The dataset was divided into training, validation, and test sets.

3. **Custom Dataset Class**: Implemented a custom dataset class to handle loading and preprocessing of images and masks. This class resized images and masks, normalized the images, and prepared the data for model training.

4. **Data Loaders**: Created data loaders for the training, validation, and test sets to efficiently feed data into the model during training and evaluation.

5. **Model Initialization**: Selected the U-Net model architecture with a ResNet-34 encoder pre-trained on ImageNet. Initialized the model, moved it to the specified device (CPU/GPU), and set up the loss function (BCEWithLogitsLoss) and optimizer (Adam).

6. **Training Loop**: Defined the training loop with early stopping based on validation loss. For each epoch, the model was trained on the training data, and its performance was evaluated on the validation data. If the validation loss improved, the model was saved. The training loop included patience handling to stop training if the validation loss did not improve for a specified number of epochs.

7. **Model Evaluation**: Implemented a testing function to evaluate the model on the test set. This function computed the test loss and Intersection over Union (IoU) score to measure the model's performance.

8. **Results Visualization**: Created a function to visualize the model's predictions by overlaying the predicted masks on the original images along with the ground truth masks. This visual assessment helped in evaluating the model's segmentation quality.

9. **Model Testing**: Loaded the best model (based on validation performance) and evaluated it on the test set to obtain the final test loss and IoU score.

## Results

The images above show the original input images from a medical imaging dataset overlaid with both the ground truth masks and the predicted masks generated by the segmentation model. The comparison helps to visually assess the model's performance in identifying the target regions within the medical images.

## Conclusion

The model demonstrates a strong performance in segmenting the medical images, as evidenced by the good overlap between the predicted and ground truth masks. This visual assessment supports the quantitative results obtained during testing, with a Test Loss of 0.07201 and a Test IoU of 0.80568. While there are some cases where the prediction could be improved, overall, the model effectively identifies the target regions within the medical images, making it a useful tool for medical image segmentation tasks.