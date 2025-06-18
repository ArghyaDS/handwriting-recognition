# Handwritten vs Printed Character Classifier (Binary)

## Description
This project builds a deep learning classifier to distinguish between handwritten and printed characters. It’s a foundational binary classification project under the Deep Learning Learning Path.

## Features
- Binary classification: Handwritten (1) vs Printed (0)
- Convolutional Neural Network (CNN)
- Evaluation with accuracy, confusion matrix, classification report
- Trained model saved for deployment or experimentation

## Dataset
- Custom dataset combining:
  - Handwritten: EMNIST Letters dataset
  - Printed: Programmatically generated printed letters using standard fonts (e.g., Arial, Times New Roman)

## Installation
```bash
pip install -r requirements.txt
```

## Steps in Code:
1️⃣ Binary Classification Setup

Unlike multiclass classification (A-Z), here we framed the problem as binary:

Label 1 → Handwritten

Label 0 → Printed (synthetic fonts or printed images)

2️⃣ Data Preparation Challenges

Need to align data dimensions across datasets before concatenation.

Proper reshaping (e.g., 3D → 4D) is critical for CNN input.

3️⃣ Model Architecture Simplicity

CNN structure works well for distinguishing texture/pattern differences between handwriting and printed forms.

Binary output → sigmoid activation & binary_crossentropy loss.

4️⃣ Importance of Data Variety

Better results need varied samples for both handwritten and printed datasets.

Synthetic printed fonts alone may not generalize fully to all printed forms.

5️⃣ Evaluation Focus

Binary classifiers → use metrics like accuracy, confusion matrix, precision-recall curves, depending on use case.

6️⃣ Real-world Application Insight

This project is a foundation for document processing pipelines:

E.g., automatically detect hand-filled vs. printed sections in scanned forms or receipts.
