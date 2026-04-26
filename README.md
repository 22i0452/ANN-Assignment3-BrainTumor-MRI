# Brain Tumor MRI Classification - ANN Assignment 3

This repository contains the code and report for ANN Assignment 3: Experimentation and Expansion.

## Project Title
Experimental Expansion of Brain Tumor MRI Classification Using EfficientNetB0, Multi-Dataset Training, and Grad-CAM Explainability

## Authors
- Shazil - 22i-0452
- Sarim - 22i-0532

## Objective
The objective of this assignment is to extend the reproduced work from Assignment 1 and 2 by conducting new experiments on brain tumor MRI classification.

## Datasets
Two brain tumor MRI datasets were used:

1. Brain Tumor MRI Dataset by Masoud Nickparvar
2. MRI Brain Tumor Dataset 4-Class by Mohamad Abouali

Classes:
- glioma
- meningioma
- notumor
- pituitary

## Experiments

| Experiment | Model | Dataset | Strategy |
|---|---|---|---|
| Exp 1 | ResNet50 | Dataset 1 | Frozen backbone |
| Exp 2 | ResNet50 | Dataset 1 | Fine-tuned last 50 layers |
| Exp 3 | EfficientNetB0 | Dataset 1 + Dataset 2 | Fine-tuned last 30 layers |

## Main Results

| Experiment | Accuracy | Macro-F1 |
|---|---:|---:|
| ResNet50 Frozen | 91.50% | 91.30% |
| ResNet50 Fine-tuned | 93.88% | 93.71% |
| EfficientNetB0 + Combined Dataset | 94.50% | 94.34% |

Dataset 2 held-out test result:

| Model | Accuracy | Macro-F1 |
|---|---:|---:|
| EfficientNetB0 | 98.67% | 98.58% |

## Key Findings
- Fine-tuning improved ResNet50 performance over the frozen baseline.
- EfficientNetB0 achieved the highest numerical result.
- EfficientNetB0 used fewer trainable parameters and trained faster than fine-tuned ResNet50.
- Glioma and meningioma remained the most difficult classes.
- McNemar's test showed that EfficientNetB0 was not statistically significantly better than fine-tuned ResNet50.

## Files
- `ANN_Assignment3_Final.ipynb`: main notebook
- `ANN_Assignment3_Final_Report.pdf`: final report
- `results/`: saved graphs and outputs

## Environment
- TensorFlow 2.19.0
- Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy

## How to Run
1. Open the notebook in Kaggle or Google Colab.
2. Add both Kaggle datasets.
3. Run all cells in order.
4. Saved outputs include training curves, confusion matrices, F1 comparison, Grad-CAM, and experiment results CSV.

## Note
Dataset paths may need to be updated depending on the runtime environment.
