# Brain Tumor Classification Using Deep Learning

## Overview
This project focuses on the classification of brain tumors using deep learning models applied to MRI images. The primary goal is to categorize brain MRI scans into one of four classes:
- Glioma tumor
- Meningioma tumor
- Pituitary tumor
- No tumor (healthy brain)

The implementation compares the performance of three popular convolutional neural network (CNN) architectures: **VGG19**, **MobileNetV2**, and **ResNet50**, and evaluates their accuracy in this classification task.

## Dataset
The dataset contains **7,153 MRI images**, with the following distribution across the four classes:

| Category      | Number of Images |
|---------------|------------------|
| Glioma        | 1,621            |
| Meningioma    | 1,775            |
| Pituitary     | 1,757            |
| No tumor      | 2,000            |

The dataset is imbalanced, which has been addressed using class weights during training.

## Methodology

### Models Implemented
1. **VGG19**:
   - A deep CNN with 19 weight layers.
   - Achieved **98% accuracy** over 70 epochs.
2. **MobileNetV2**:
   - A lightweight CNN model designed for mobile and edge devices.
   - Achieved **97.8% accuracy** over 70 epochs.
3. **ResNet50**:
   - A residual learning framework with 50 layers.

### Techniques for Improved Performance
- **Data Splitting**: Training (80%), validation (20%), and a separate test set for final evaluation.
- **Data Augmentation**: Includes random rotation, translation, shearing, zooming, and horizontal flipping.
- **Transfer Learning**: Pretrained layers from ImageNet used to capture general features.
- **Regularization**:
  - Batch normalization
  - Dropout layers (rates: 0.5 and 0.6)
  - L2 regularization
- **Early Stopping**: Monitors validation loss to prevent overfitting.
- **Learning Rate Scheduler**: Reduces learning rate if validation loss plateaus.
- **Class Weights**: Adjusted weights to address dataset imbalance.


## Results
The best-performing model was **VGG19**, achieving an accuracy of **98%** on the validation set. MobileNetV2 followed closely with **97.8% accuracy**.

## Project Structure
```
brain-tumor-classification/
├── data/                  # Dataset folder
├── models/                # Pretrained models and saved weights
├── scripts/               # Training, evaluation, and prediction scripts
├── notebooks/             # Jupyter notebooks for experimentation
├── requirements.txt       # Python dependencies
├── train.py               # Training script
├── evaluate.py            # Evaluation script
├── predict.py             # Prediction script
└── README.md              # Project documentation
```

## Citation
https://www.kaggle.com/datasets/tombackert/brain-tumor-mri-data

---
Feel free to open an issue or pull request for any improvements or bug fixes!
