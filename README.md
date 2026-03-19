## **1.Project Title**

**Image Classification using Transfer Learning (Cats, Dogs & Pandas) with ResNet18**

## **2.Abstract / Introduction**

This project implements a **deep learning-based image classification system** using **ResNet18 (Transfer Learning)** in PyTorch.

Users can input images, and the model predicts whether the image belongs to:

* Cat
* Dog
* Panda

The system leverages a **pretrained ResNet18 model** trained on ImageNet, which improves performance and reduces training time.

The project includes:

* Image preprocessing and augmentation
* Transfer learning using ResNet18
* Model training and evaluation
* Confusion matrix visualization
* Prediction on test images

---

## **3.  Dataset Details**

### **Dataset: Cats vs Dogs vs Pandas (Kaggle)**

* Total Classes: 3
* Training Images: 204
* Testing Images: 34

### **Folder Structure**

```
data/
 ├── Train/
 │    ├── Cat/
 │    ├── Dog/
 │    ├── Pandas/
 │
 ├── Test/
      ├── Cat/
      ├── Dog/
      ├── Pandas/
```

---

## **4.Environment Setup**

Install dependencies:

```bash
pip install torch torchvision torchaudio
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## **5.GPU Installation Steps OR CPU Installation Steps**

### **GPU Setup**

(If you have NVIDIA GPU)

1. Install NVIDIA CUDA Toolkit
2. Install cuDNN
3. Install PyTorch with GPU support:

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

### **CPU Setup**

If no GPU available:

```bash
pip install torch torchvision torchaudio
```

---

## **6.How to Run in VS Code**

### **Step 1 — Open Project Folder**

Open your project folder in VS Code.

### **Step 2 — Run Notebook / Script**

```bash
python train.py
```

OR run the Jupyter notebook:

```
cat_dog_panda_transfer_learning.ipynb
```

### **Step 3 — Tips**

* Select correct Python interpreter
* Use terminal inside VS Code
* Ensure dataset path is correct

---

## **7.Model Details**

### **Base Model**

* ResNet18 (Pretrained on ImageNet)

### **Custom Classifier**

```
Linear(512 → 512)
ReLU
Dropout(0.4)
Linear(512 → 3)
LogSoftmax
```

### **Training Setup**

* Loss Function: CrossEntropyLoss
* Optimizer: Adam (lr = 0.001)
* Epochs: 3

---

## **8.Results & Output**

### **Results**

* Training Accuracy: ~90%
* Test Accuracy: ~47%

### **Model Performance**

* Model learns training data well
* Lower test accuracy due to overfitting

---

## **9.Confusion Matrix**

The confusion matrix is plotted using Seaborn to evaluate predictions.

(Add your screenshot here)

```
![Confusion Matrix](outputs/confusion_matrix.png)
```

---

## **10.Sample Outputs**

Include screenshots in your repository:

* Model prediction output
* Confusion matrix
* Training logs

---

## **11.Enhancements / Improvements**

* Train for more epochs (10–15)
* Use larger dataset
* Apply more data augmentation
* Fine-tune entire ResNet model
* Try other architectures (VGG, EfficientNet)

---

## **12.Conclusion**

This project successfully demonstrates **image classification using transfer learning**.

The ResNet18 model provides good training accuracy, but performance can be improved by:

* Increasing dataset size
* Fine-tuning deeper layers
* Training for more epochs

---

## **13.Repository Structure**

```
project/
 ├── notebooks/
 │    └── cat_dog_panda_transfer_learning.ipynb
 │
 ├── data/
 ├── outputs/
 │    └── confusion_matrix.png
 │
 ├── requirements.txt
 ├── README.md
```

---

## **14.Requirements**

```
torch
torchvision
numpy
pandas
matplotlib
seaborn
scikit-learn
```
