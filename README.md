# Crop Classification Using VGG16

## Project Overview
This project is a deep learning-based classification model that predicts different crop types (jute, maize, rice, sugarcane, wheat) using the VGG16 model as a feature extractor.

## Dataset
The dataset consists of images categorized into five crop classes:
- Jute
- Maize
- Rice
- Sugarcane
- Wheat

The images are stored in a directory structure where each class has its own folder.

## Prerequisites
Ensure you have the following dependencies installed before running the project:

```bash
pip install tensorflow keras numpy pandas matplotlib
```

## Project Structure
```
Crop_prediction/
│── crop_images/
│   ├── jute/
│   ├── maize/
│   ├── rice/
│   ├── sugarcane/
│   ├── wheat/
│── train.py
│── README.md
```

## Model Training
The model uses transfer learning with VGG16. Below is a summary of the approach:
1. Load and preprocess the dataset using `ImageDataGenerator`.
2. Use VGG16 without the top layer as the feature extractor.
3. Add a flatten layer and a dense layer for classification.
4. Compile and train the model using categorical cross-entropy loss.

## Running the Training Script

```bash
python train.py
```

## Expected Output
After 5 epochs, the model achieves an accuracy of ~62%.

## Future Improvements
- Increase the number of training images.
- Apply data augmentation techniques.
- Fine-tune the VGG16 layers instead of freezing them.




