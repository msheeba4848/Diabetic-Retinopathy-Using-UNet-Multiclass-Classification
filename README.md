# U-Net Segmentation Model for Diabetic Retinopathy

This repository contains code for training and saving a U-Net model tailored for segmenting retinal images to assist in the diagnosis of diabetic retinopathy. Diabetic retinopathy is a leading cause of vision loss among people with diabetes, and early detection is crucial for effective treatment and prevention. 

## Introduction

The U-Net architecture is particularly well-suited for medical image segmentation due to its ability to capture fine details and perform accurate pixel-level classification. By segmenting retinal images, we aim to highlight regions affected by diabetic retinopathy, thereby aiding in automated diagnosis and monitoring. This model is designed to help healthcare professionals by providing an efficient tool for analyzing retinal images, ultimately improving patient outcomes and supporting early intervention strategies.

## Files

- **`<BACKBONE>_Retinal.json`**: Contains the model architecture in JSON format.
- **`<BACKBONE>_Retinal.h5`**: Contains the model weights.
- **`<BACKBONE>_Retinal.csv`**: Contains the training history, including metrics like loss and accuracy over epochs.

## Code Overview

1. **Model Configuration and Creation**:
   - The U-Net model is defined with a specified backbone, such as ResNet34, and configured for binary or multiclass segmentation based on the number of classes.
   - Loss functions (Dice Loss and Focal Loss) and metrics (IOU Score and F-Score) are set up to optimize performance in retinal image segmentation.

2. **Saving the Model**:
   - The model architecture is saved as a JSON file.
   - Model weights are saved in HDF5 format for later use.

3. **Training History**:
   - Training metrics (such as loss and accuracy) are recorded and saved in a CSV file for analysis and review.

## How to Use

1. **Training**:
   - Ensure you have TensorFlow, segmentation_models, and pandas installed.
   - Adjust model parameters such as the backbone and input dimensions according to your dataset.

2. **Saving and Loading**:
   - Use the provided code to save the model architecture and weights.
   - To reload the model, use `model_from_json` to reconstruct the model from the JSON file and `load_weights` to load the saved weights.

3. **Analyzing Results**:
   - Review the CSV file to analyze training metrics.
   - Use the `.tail()` method to view the most recent epochs' performance data.

## Dependencies

- TensorFlow/Keras
- segmentation_models (for loss functions and metrics)
- pandas (for saving and analyzing training history)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- U-Net architecture and segmentation models library for providing the tools needed for effective image segmentation.
- TensorFlow/Keras for the deep learning framework.
- The broader research community for advancements in diabetic retinopathy detection and medical image analysis.

