# Plant Disease Detection using CNN

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red.svg)
![Accuracy](https://img.shields.io/badge/Accuracy-97.1%25-brightgreen.svg)

## Project Overview
This project is a deep learning-based image classification system designed to identify plant diseases from leaf images. Using a Custom **Convolutional Neural Network (CNN)**, the model can classify 38 different combinations of crop and disease states, helping in early detection and agricultural yield protection.

## Dataset
The model was trained on the augmented version of the famous **PlantVillage Dataset**.
* **Total Images:** ~87,000+
* **Classes:** 38 different classes (including healthy and diseased leaves from apples, tomatoes, grapes, potatoes, etc.)
* **Preprocessing:** Images were resized to `224x224` and normalized (rescaled by `1./255`).

## Model Architecture
The network is built from scratch using TensorFlow/Keras with the following structure:
* **Input Layer:** `224x224x3` (RGB Images)
* **Convolutional Blocks:** 3x `Conv2D` layers (32, 64, 128 filters) each followed by `MaxPooling2D` to extract spatial features (edges, spots, textures).
* **Fully Connected Layer:** A `Dense` layer with 512 neurons.
* **Regularization:** `Dropout(0.5)` applied to prevent overfitting.
* **Output Layer:** `Dense` layer with 38 neurons using `Softmax` activation for multi-class classification.

## Results
After training for 10 epochs, the model achieved exceptional results, proving its capability to generalize well on unseen data without heavy overfitting:
* **Training Accuracy:** `%97.11`
* **Validation Accuracy:** `%93.80`

## How to Run
**1. Clone this repository:**
> git clone [https://github.com/YOUR_GITHUB_USERNAME/plant-disease-detection.git](https://github.com/YOUR_GITHUB_USERNAME/plant-disease-detection.git)

**2. Install required libraries:**
Make sure you have Python installed, then install the dependencies:
> pip install tensorflow numpy matplotlib

**3. Download the Model:**
**Important:** Due to GitHub's file size limits, the trained model (`.h5` file) is stored in the **Releases** section. Download the `plant_disease_model.h5` file from the [Releases](https://github.com/cerenk44/plant-disease-detection/releases) tab and place it in the project root directory.

## 🔮 Future Work
* Integrating Transfer Learning (e.g., MobileNetV2) for comparison to achieve even higher accuracy.
* Developing a simple Web Interface (Flask/Streamlit) to upload leaf images and get real-time predictions.
