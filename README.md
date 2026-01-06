# Dog vs Cat Image Classification using CNN

This project implements a **binary image classification system** using **Convolutional Neural Networks (CNN)** to classify images of **Dogs and Cats**.  
The model is trained using TensorFlow/Keras and the dataset is downloaded directly from Kaggle.

---

## 📌 Dataset
- Source: Kaggle  
- Dataset Name: Dog and Cat Classification Dataset
- Structure:

PetImages/

├── train/
│ ├── Cat/
│ └── Dog/
├── test/
│ ├── Cat/
│ └── Dog/
---

## ⚙️ Project Workflow

### 1. Dataset Download & Setup
- Kaggle API used to download dataset
- Dataset extracted and organized
- Train/Test split performed manually (80/20)

### 2. Data Cleaning
- Corrupted images removed
- All images converted to RGB format
- Image resizing to **256 × 256**

### 3. Data Loading
- Used `image_dataset_from_directory`
- Labels inferred automatically
- Normalization applied (`image / 255`)

---

## 🧠 Model Architecture (Baseline CNN)

- Conv2D (16 filters)
- MaxPooling
- Conv2D (32 filters)
- MaxPooling
- Flatten
- Dense (64 neurons)
- Output layer (Sigmoid)

**Loss:** Binary Crossentropy  
**Optimizer:** Adam  
**Metric:** Accuracy

---

## 📊 Results (Baseline Model)

- **Training Accuracy:** ~99%
- **Validation Accuracy:** ~75%
- Clear signs of **overfitting**

---

## 🔧 Overfitting Reduction Techniques Applied

To improve generalization, the following techniques were applied:

### ✔ L2 Regularization
- Applied to convolution layers to penalize large weights

### ✔ Dropout
- Dropout added after convolution and dense layers

### ✔ Reduced Model Complexity
- Limited number of filters and dense units

---

## 📉 Results (Regularized Model)

- Training accuracy reduced slightly (expected)
- Validation loss improved but overfitting still exists
- Shows need for further improvement techniques

---

## 🚀 Possible Improvements (Future Work)

- Data Augmentation (rotation, zoom, flip)
- Batch Normalization
- Early Stopping
- Learning Rate Scheduling
- Image size reduction (128×128)

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- PIL
- Kaggle API

---

## 📌 Conclusion

This project demonstrates:
- CNN fundamentals
- Dataset preprocessing
- Overfitting detection
- Regularization techniques

---

## 👤 Author

**Hamza Amjad**  
**AI, Machine Learning, NLP & Deep Learning Enthusiast**
