# BrainTumor-Detection using DeepLearning

## Overview

This project presents a deep learning-based hybrid stacking ensemble model for multi-class brain tumor MRI classification.

The proposed model combines:

- MobileNetV2
- EfficientNetB0
- Meta-Learner (Dense Neural Network)

to classify MRI images into four categories:

1. Glioma
2. Meningioma
3. Pituitary
4. No Tumor

---

## Dataset

The dataset was created by merging multiple Kaggle brain tumor MRI datasets.

### Classes

| Class | Description |
|------|------|
| Glioma | Brain glioma tumor |
| Meningioma | Meningioma tumor |
| Pituitary | Pituitary tumor |
| No Tumor | Healthy MRI images |

---

## Dataset Structure

```text
final_merged_dataset/
├── Training/
│   ├── glioma/
│   ├── meningioma/
│   ├── notumor/
│   └── pituitary/
│
└── Testing/
    ├── glioma/
    ├── meningioma/
    ├── notumor/
    └── pituitary/
```

---

## Models Used

### Base Models

- MobileNetV2
- EfficientNetB0

### Meta-Learner

```text
Dense(128) → Dropout(0.3) → Dense(4)
```

---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Training Configuration

| Parameter | Value |
|------|------|
| Image Size | 224 × 224 |
| Batch Size | 16 |
| Epochs | 8–20 |
| Optimizer | Adam |
| Learning Rate | 0.0001 |
| Dropout | 0.3 |

---

## Evaluation Metrics

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC Curve
- Confusion Matrix

---

## Results

The hybrid stacking ensemble achieved high classification performance on the merged MRI dataset.

---

## Output Examples

### Confusion Matrix

(Add image here)

### ROC Curve

(Add image here)

### Sample MRI Images

(Add image here)

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Run Project

```bash
python train_stacking_model.py
```

---

## Future Improvements

- Add Grad-CAM visualization
- Deploy using Streamlit
- Use Vision Transformers
- Add explainable AI techniques

---

## Author

Abhishek Yadav

---

## License

This project is for educational and research purposes.
requirements.txt

Create requirements.txt

tensorflow
numpy
matplotlib
seaborn
scikit-learn
pillow
opencv-python
jupyter

Add Dataset Links in README
## Dataset Sources

1. https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

2. https://www.kaggle.com/datasets/abdallahwagih/brain-tumor