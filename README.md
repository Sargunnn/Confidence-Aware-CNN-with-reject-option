#Confidence-Aware CNN with Reject Options for Medical Image Classification
Overview
Deep learning models used in medical imaging often make overconfident predictions, even when they are incorrect. In clinical applications, such errors can lead to unsafe decisions. This project presents a confidence-aware selective classification framework that estimates prediction uncertainty and automatically rejects low-confidence predictions, referring them to a human expert instead.

The model uses EfficientNet-B0 for diabetic retinopathy classification and integrates Evidential Deep Learning (EDL) to quantify predictive uncertainty. Multiple uncertainty signals are combined to make a reliable accept-or-reject decision.

Features
EfficientNet-B0-based diabetic retinopathy classifier
Confidence-aware selective classification
Evidential Deep Learning for uncertainty estimation
Fusion of Softmax Confidence, Predictive Entropy, and Evidential Uncertainty
Automatic rejection of uncertain predictions
Model calibration and reliability evaluation
Dataset
APTOS 2019 Blindness Detection dataset
Evaluation
The framework is evaluated using:

Risk–Coverage Curves
Area Under the Risk–Coverage Curve (AURC)
Expected Calibration Error (ECE)
Confusion Matrix
Reliability Diagrams
Tech Stack
Python
PyTorch
EfficientNet-B0
OpenCV
NumPy
Matplotlib
scikit-learn
Repository Structure
├── dataset/
├── models/
├── notebooks/
├── utils/
├── train.py
├── evaluate.py
├── requirements.txt
└── README.md
Future Work
Incorporate Bayesian uncertainty estimation.
Extend to multi-disease retinal image classification.
Deploy as a lightweight clinical decision support system.
License
This project is intended for educational and research purposes.
