## Problem Statement
In autonomous driving and driver-assist systems, timely identification of **cut-in maneuvers** (where a vehicle suddenly enters another vehicle's lane) is critical for preventing accidents. However, detecting such events in real-world traffic is challenging due to:
Their **rarity** and **class imbalance** in driving datasets,
The need to **understand temporal vehicle behavior**,
The demand for **real-time inference** and **driver alerts**.

This project proposes a **multitask deep learning model** that not only detects cut-in events but also predicts the **direction** of approaching vehicles, enabling intelligent warning systems that improve driving safety.



##  Overview
This project presents a multitask deep learning framework for real-time **vehicle cut-in detection** and **movement direction prediction**, enhancing road safety in autonomous driving environments. The model is designed to handle **class imbalance**, incorporate **temporal dependencies**, and provide **real-time driver alerts** using advanced deep learning components.



##  Key Features

### 1. Multitask Learning Framework
  Simultaneously performs:
    **Cut-in event detection**
    **Vehicle movement direction prediction**
  Uses shared features for improved generalization and performance.

### 2. YOLOv5 for Object Detection
  Integrates a pre-trained **YOLOv5** model to detect vehicles in real-time.
  Bounding box information is extracted and fed into the multitask model.

### 3. Temporal Modeling with LSTM + Attention
  Uses **LSTM layers** to model sequential vehicle behavior.
  An **Attention mechanism** emphasizes crucial frames for better prediction.

### 4. Custom Loss Functions: Focal Loss
  Implements **focal loss** to address class imbalance (rare cut-in events).
  Dynamically focuses on hard-to-classify examples, improving accuracy.

### 5. Real-Time Warning System
  Predicts:
    Cut-in likelihood
    Vehicle movement direction
  Triggers **visual**, **audio**, and **haptic alerts** to warn the driver and reduce response times.

### 6. Hyperparameter Tuning
  Uses `GridSearchCV` to optimize:
    LSTM units
    Dense layer units
    Batch size
    Epochs
  Ensures best configuration through exhaustive search.

### 7. Attention Visualization
  Visualizes attention weights across the input sequence.
  Useful for debugging and understanding how the model makes decisions.



## Tech Stack

 Python
 
 [YOLOv5](https://github.com/ultralytics/yolov5)
 
 TensorFlow / PyTorch
 
 OpenCV
 
 Scikit-learn (for GridSearchCV)
 
 Custom Focal Loss
 
 LSTM + Attention Mechanism



## Results
  Higher detection and prediction accuracy with multitask learning.
  Improved performance on rare events through focal loss.
  Real-time alerts for improved driver awareness and safety.
