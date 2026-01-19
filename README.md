# Alzheimer's Disease Classification from MRI Scans (EfficientNet-B0)

This project is a high-accuracy medical imaging solution designed to classify Alzheimer's Disease stages using MRI scans. It was developed not just as a research project, but as a pioneering MedTech Startup solution for the Uzbekistan market, tailored to meet specific client requirements.

## 🚀 Overview

Early detection of Alzheimer's is critical for effective patient management. This model leverages deep learning to categorize MRI scans into four distinct stages:

•	**Non-Demented** (Healthy)

•	**Very Mild Demented**

•	**Mild Demented**

•	**Moderate Demented**

## 📊 Dataset

The model was trained on [the Alzheimer's Multiclass Dataset](https://www.kaggle.com/datasets/aryansinghal10/alzheimers-multiclass-dataset-equal-and-augmented) from Kaggle.

•	Volume: 44,000 JPG images.

•	Structure: Balanced and augmented across 4 classes to ensure robust performance and prevent model bias.

## 🧠 Technical Architecture & Training

I utilized the EfficientNet-B0 architecture, known for its optimal balance between computational efficiency and high accuracy—making it ideal for deployment in clinical environments.

•	**Framework**: PyTorch

•	**Optimizer**: Adam (lr=0.001)

•	**Loss Function**: CrossEntropyLoss

•	**Scheduler**: StepLR (step_size=2, gamma=0.1)

•	**Training**: 6 Epochs (Google Colab environment)

## 📈 Performance Results

The model achieved state-of-the-art results on the test set:

•	**Test Accuracy**: 99.4%

•	**Test Loss**: 0.019

•	**Train Accuracy**: 99.8%

## Confusion Matrix Analysis

This Confusion Matrix demonstrates that the model operates with exceptionally high precision across all stages:

•	**Mild Demented**: 2,496 cases were correctly predicted. Only 4 instances of misclassification were observed (1 as Moderate and 3 as Very Mild).

•	**Moderate Demented**: Perfect result. All 2,500 cases were identified without error. This indicates that the model excels at distinguishing the specific features unique to this stage.

•	**Non-Demented**: 2,478 cases were correctly identified. A confusion with "Very Mild Demented" occurred in 22 cases. This is medically expected, as the physiological transitions from a healthy state to the early stages of dementia are often very subtle.

•	**Very Mild Demented**: 2,477 successful classifications. Minor overlaps were primarily identified with "Non-Demented" (19 cases) and "Mild Demented" (4 cases).
