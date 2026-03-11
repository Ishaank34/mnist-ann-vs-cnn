# MNIST ANN vs CNN Digit Classifier

This project compares the performance of two neural network architectures — **Artificial Neural Network (ANN)** and **Convolutional Neural Network (CNN)** — for handwritten digit recognition using the **MNIST dataset**.

The implementation is built using **TensorFlow** and **Keras** and demonstrates how CNNs outperform traditional fully connected neural networks on image classification tasks.

---

## Project Overview

The MNIST dataset contains **70,000 grayscale images** of handwritten digits (0–9).

Each image:

* Size: **28 × 28 pixels**
* Grayscale image
* Label: digit from **0–9**

The project trains two models:

1. **ANN (Fully Connected Neural Network)**
2. **CNN (Convolutional Neural Network)**

Their performance is then compared using test accuracy.

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib

---

## Dataset

Dataset used: **MNIST Handwritten Digit Dataset**

It is automatically loaded using TensorFlow:

```python
from tensorflow.keras.datasets import mnist
```

Dataset split:

* **Training images:** 60,000
* **Testing images:** 10,000

---

## Model Architectures

### Artificial Neural Network (ANN)

Architecture:

Input Layer (Flatten 28×28)
↓
Dense Layer (100 neurons, ReLU)
↓
Output Layer (10 neurons, Softmax)

---

### Convolutional Neural Network (CNN)

Architecture:

Conv2D (32 filters, 3×3 kernel)
↓
MaxPooling (2×2)
↓
Flatten
↓
Dense Layer (100 neurons, ReLU)
↓
Output Layer (10 neurons, Softmax)

---

## Training

ANN Model:

* Optimizer: Adam
* Loss: Sparse Categorical Crossentropy
* Epochs: 10

CNN Model:

* Optimizer: Adam
* Loss: Sparse Categorical Crossentropy
* Epochs: 5

---

## Results

The CNN model typically achieves **higher accuracy** because convolutional layers are better at capturing spatial patterns in images.

Typical results:

ANN Accuracy: ~97%
CNN Accuracy: ~99%

---

## How to Run the Project

### 1 Install dependencies

```bash
pip install tensorflow matplotlib numpy
```

### 2 Run the script

```bash
python mnist_model.py
```

The script will:

* load the dataset
* train ANN
* train CNN
* evaluate both models
* display sample images

---

## Example Output

Example digit image from MNIST:

28×28 grayscale handwritten digit displayed using Matplotlib.

---

## Future Improvements

Possible enhancements:

* Add confusion matrix visualization
* Plot training accuracy and loss curves
* Implement deeper CNN architecture
* Add model saving and loading
* Add prediction visualization for test images

---

## Author

**Ishaan Kapoor**

Computer Science Engineering Student
VIT Vellore
