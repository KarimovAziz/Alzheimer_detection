Alzheimer's Disease Classification from MRI Scans (EfficientNet-B0)
This project is a high-accuracy medical imaging solution designed to classify Alzheimer's Disease stages using MRI scans. It was developed not just as a research project, but as a pioneering MedTech Startup solution for the Uzbekistan market, tailored to meet specific client requirements.
🚀 Overview
Early detection of Alzheimer's is critical for effective patient management. This model leverages deep learning to categorize MRI scans into four distinct stages:
•	Non-Demented (Healthy)
•	Very Mild Demented
•	Mild Demented
•	Moderate Demented
📊 Dataset
The model was trained on the Alzheimer's Multiclass Dataset from Kaggle.
•	Volume: 44,000 JPG images.
•	Structure: Balanced and augmented across 4 classes to ensure robust performance and prevent model bias.
🧠 Technical Architecture & Training
I utilized the EfficientNet-B0 architecture, known for its optimal balance between computational efficiency and high accuracy—making it ideal for deployment in clinical environments.
•	Framework: PyTorch
•	Optimizer: Adam (lr=0.001)
•	Loss Function: CrossEntropyLoss
•	Scheduler: StepLR (step_size=2, gamma=0.1)
•	Training: 6 Epochs (Google Colab environment)
📈 Performance Results
The model achieved state-of-the-art results on the test set:
•	Test Accuracy: 99%
•	Test Loss: 0.033
•	Train Accuracy: 99.8%
Confusion Matrix Analysis
The confusion matrix demonstrates an exceptional classification performance with high precision across all stages:
•	Mild Demented: 2,494 correct predictions with only 6 minor misclassifications.
•	Moderate Demented: Near-perfect detection with 2,499 correct predictions out of 2,500.
•	Non-Demented: 2,456 correct predictions. A minor overlap of 32 cases is observed with Very Mild Demented, which is medically expected due to the subtle physiological transitions between healthy and early-stage Alzheimer's in clinical practice.
•	Very Mild Demented: 2,485 successful classifications, showing strong model robustness.
💻 Installation & Usage
1.	Clone the repository:
Bash
git clone https://github.com/KarimovAziz/Alzheimer_detection.git
2.	Install dependencies:
Bash
pip install -r requirements.txt
Quick Inference: Open the inference.ipynb file in Google Colab or Jupyter Notebook. This notebook allows you to load the pre-trained model and test it on new MRI scans without re-training.
✉️ Contact
If you are interested in this startup or have questions regarding the implementation, feel free to reach out via GitHub issues or direct message.
git clone https://github.com/KarimovAziz/Alzheimer_detection.git
