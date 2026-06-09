# FedVGM: Privacy-Preserving Disease Prediction using Federated Learning & Explainable AI

This repository contains the research manuscript and architectural overview for **FedVGM**, a scalable, privacy-preserving federated learning framework designed for multi-modal medical image analysis. 

Traditional deep learning in healthcare is often hindered by strict data privacy regulations and fragmented institutional datasets. FedVGM addresses this by enabling decentralized model training across multiple clients without ever centralizing sensitive patient data.

 **[CACSC602_SusmitaHaldar_SiddhiKedia_KhushiYadav.pdf](./CACSC602_SusmitaHaldar_SiddhiKedia_KhushiYadav--.pdf)** 

## Key Architectural Highlights

* **Federated Learning Infrastructure:** Implements a decentralized training loop where clients train models locally on isolated data and only share encrypted weight updates with the central server, strictly adhering to medical data privacy constraints.
* **Adaptive Weighted Aggregation:** Replaces standard averaging (FedAvg) with a custom aggregation strategy that dynamically adjusts client weights based on local dataset size and real-time model performance, ensuring robustness against non-IID data.
* **Ensemble Transfer Learning:** Utilizes an integrated dual-architecture approach concatenating feature maps from pre-trained **VGG16** and **EfficientNetB0** models, passing them through custom fully connected layers for multi-class classification.
* **Clinical Explainability (XAI):** Solves the "black-box" AI problem by integrating **SHAP** (SHapley Additive exPlanations) and **Grad-CAM** (Gradient-weighted Class Activation Mapping) to provide instance-level, visual transparency for all diagnostic predictions.

## Performance & Results

The framework was evaluated across a multi-class dataset encompassing four diagnostic categories (COVID-19, Normal, Pneumonia, Tuberculosis). 

* **Baseline Accuracy:** 96.88%
* **Fine-Tuned Accuracy:** **97.8%**
* **Interpretability:** Grad-CAM heatmaps successfully validated that the model's high-confidence predictions actively targeted clinically relevant physiological regions (e.g., lung consolidations, lesion textures) rather than background noise.

## Repository Contents

* `CACSC602_SusmitaHaldar_SiddhiKedia_KhushiYadav--.pdf` - The comprehensive 9-page working paper detailing the complete system design, ablation studies, aggregation mathematics, and final statistical evaluations.

## 🛠️ Technology Stack
* **Core:** Python, TensorFlow, Keras
* **Federated Architecture:** Custom aggregation scripting
* **Explainable AI:** SHAP, Grad-CAM, OpenCV

---
*Developed as an independent academic research initiative.*
