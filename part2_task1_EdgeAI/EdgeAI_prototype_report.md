# Practical Implementation Report: Edge AI Prototype (Task 1)

## Goal
To train a lightweight image classification model for recognizing recyclable items and convert it to the TensorFlow Lite (TFLite) format for on-device deployment.

## 1. Model Training and Methodology
### Model Architecture
A Transfer Learning approach was used with the MobileNetV2 model.

- **Base Model:** MobileNetV2 with frozen layers.
- **Model Head:** 
  - GlobalAveragePooling2D
  - Dropout(0.2)
  - Dense(1, activation='sigmoid')

### Dataset
Trained on "Waste Classification data" from Kaggle, augmented during training.

## 2. Results and Accuracy Metrics
- **Final Validation Accuracy:** 93.53%
- **Final Deployed Asset:** model.tflite

## 3. Deployment Steps
1. Load Asset
2. Initialize Interpreter
3. Capture Image
4. Pre-process
5. Run Inference
6. Get Output

## 4. How Edge AI Benefits Real-Time Applications
- **Low Latency:** Instant classification on-device.
- **Enhanced Privacy:** Local processing of sensitive data.
- **Reliability & Offline Capability:** Functional without internet connection.