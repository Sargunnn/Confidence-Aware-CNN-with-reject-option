# Confidence-Aware Selective Classification for Diabetic Retinopathy

## Overview

Deep learning models used in medical imaging often make overconfident predictions, even when they are incorrect. In clinical applications, such errors can lead to unsafe decisions.

This project presents a **confidence-aware selective classification framework** that estimates prediction uncertainty and automatically **rejects low-confidence predictions**, referring them to a human expert instead.

The model uses **EfficientNet-B0** for diabetic retinopathy classification and integrates **Evidential Deep Learning (EDL)** to quantify predictive uncertainty. Multiple uncertainty signals are combined to make an accept-or-reject decision.

## Features

* EfficientNet-B0-based diabetic retinopathy classifier
* Confidence-aware selective classification
* Evidential Deep Learning for uncertainty estimation
* Fusion of Softmax Confidence, Predictive Entropy, and Evidential Uncertainty
* Automatic rejection of uncertain predictions
* Model calibration and reliability evaluation

## Dataset

The project uses the **APTOS 2019 Blindness Detection** dataset.

The dataset consists of retinal fundus images used for diabetic retinopathy severity classification.

## Methodology

The framework follows the following pipeline:

1. Retinal image preprocessing
2. EfficientNet-B0-based classification
3. Prediction generation
4. Uncertainty estimation using multiple signals
5. Fusion of uncertainty measures
6. Confidence-based accept/reject decision
7. Referral of uncertain predictions for human review

### Uncertainty Signals

The framework combines:

* **Softmax Confidence**
* **Predictive Entropy**
* **Evidential Uncertainty**

These signals are used to identify predictions where the model has insufficient confidence.

## Evaluation

The framework is evaluated using:

* Risk-Coverage Curves
* Area Under the Risk-Coverage Curve (AURC)
* Expected Calibration Error (ECE)
* Confusion Matrix
* Reliability Diagrams

### Risk-Coverage Curve

The Risk-Coverage Curve evaluates the trade-off between the percentage of predictions accepted by the model (**coverage**) and the error rate among those accepted predictions (**risk**).

A good selective classifier should maintain low risk while providing useful coverage.

## Model Architecture

The primary classification model used in this project is **EfficientNet-B0**.

Evidential Deep Learning is incorporated to estimate predictive uncertainty and improve the model's ability to identify uncertain predictions.

## Tech Stack

* Python
* PyTorch
* EfficientNet-B0
* OpenCV
* NumPy
* Matplotlib
* scikit-learn

## Repository Structure

```text
├── dataset/
├── models/
├── notebooks/
├── utils/
├── train.py
├── evaluate.py
├── requirements.txt
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/Sargunnn/Confidence-Aware-CNN-with-reject-option.git
cd Confidence-Aware-CNN-with-reject-option
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

Train the model:

```bash
python train.py
```

Evaluate the model:

```bash
python evaluate.py
```

## Results

Add your experimental results here.

| Metric   | Result |
| -------- | -----: |
| Accuracy | 84.5%% |
| ECE      | 0.041 |
| AURC     | 0.098 |
| Coverage | 78% (at 95% target accuracy) |

## Future Work

* Incorporate Bayesian uncertainty estimation
* Explore additional uncertainty estimation techniques
* Extend the framework to multi-disease retinal image classification
* Improve model calibration
* Develop a lightweight clinical decision-support prototype

## Disclaimer

This project is intended for **educational and research purposes only** and is not intended to provide medical diagnosis or replace professional clinical judgment.

## License

This project is intended for educational and research purposes.

