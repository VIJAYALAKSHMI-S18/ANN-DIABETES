# ANN-DIABETES
# 🩺 Diabetes Prediction using Artificial Neural Network (ANN)

A beginner-friendly Deep Learning project that predicts whether a person has diabetes using an Artificial Neural Network (ANN) built with [TensorFlow](https://www.tensorflow.org?utm_source=chatgpt.com) and [Keras](https://keras.io?utm_source=chatgpt.com).

---

# 📌 Project Overview

This project demonstrates how to build and train a simple ANN model for **binary classification** using the **Pima Indians Diabetes Dataset**.

The model learns patterns from medical data and predicts whether a patient is likely to have diabetes.

### ✅ What This Project Covers

* 📂 Loading the dataset
* 🧹 Data preprocessing
* ⚖️ Feature scaling
* 🧠 Building the ANN model
* ⚙️ Model compilation
* 🚀 Model training
* 📊 Model evaluation

---

# 🛠️ Technologies Used

* 🐍 Python
* [TensorFlow](https://www.tensorflow.org?utm_source=chatgpt.com)
* [Keras](https://keras.io?utm_source=chatgpt.com)
* [NumPy](https://numpy.org?utm_source=chatgpt.com)
* [Pandas](https://pandas.pydata.org?utm_source=chatgpt.com)
* [Matplotlib](https://matplotlib.org?utm_source=chatgpt.com)
* [Scikit-learn](https://scikit-learn.org?utm_source=chatgpt.com)

---

# 📊 Dataset Information

The dataset contains **8 medical input features** and **1 target output**.

## 📥 Input Features

* Pregnancies
* Glucose
* BloodPressure
* SkinThickness
* Insulin
* BMI
* DiabetesPedigreeFunction
* Age

## 🎯 Target Variable

* `0` → Non-Diabetic
* `1` → Diabetic

---

# 🧹 Data Preprocessing

Before training the neural network:

✅ The dataset is split into training and testing sets
✅ Feature scaling is applied using `StandardScaler`
✅ Scaling helps the ANN learn faster and improve accuracy

---

# 🧠 ANN Model Architecture

The model is built using the Sequential API.

## 🏗️ Network Structure

| Layer          | Neurons | Activation Function |
| -------------- | ------- | ------------------- |
| Input Layer    | 8       | —                   |
| Hidden Layer 1 | 12      | ReLU                |
| Hidden Layer 2 | 8       | ReLU                |
| Output Layer   | 1       | Sigmoid             |

---

# ⚙️ Model Compilation

The model is compiled using:

* ⚡ Optimizer → `adam`
* 📉 Loss Function → `binary_crossentropy`
* 📈 Evaluation Metric → `accuracy`

---

# 🚀 Model Training

The ANN model is trained for:

* 🔁 Epochs → `100`

During training:

* 📉 Loss decreases gradually
* 📈 Accuracy improves over time
* 🧠 The model learns patterns from the dataset

---

# 📊 Model Performance

## ✅ Results

* 🎯 Training Accuracy → **~82%**
* 🧪 Testing Accuracy → **~77%**

The model performs well on unseen test data and provides a solid introduction to Deep Learning concepts.

---

# 🔄 Project Workflow

```text id="m8w3zr"
1️⃣ Import Libraries
2️⃣ Load Dataset
3️⃣ Preprocess Data
4️⃣ Scale Features
5️⃣ Build ANN Model
6️⃣ Compile Model
7️⃣ Train Model
8️⃣ Evaluate Model
```

---

# 💻 Sample Model Code

```python id="vm0kq1"
model = keras.Sequential([

    keras.layers.Dense(12, activation='relu', input_shape=(8,)),

    keras.layers.Dense(8, activation='relu'),

    keras.layers.Dense(1, activation='sigmoid')
])

model.compile(
    optimizer='adam',
    loss='binary_crossentropy',
    metrics=['accuracy']
)

model.fit(X_train, y_train, epochs=100)

loss, accuracy = model.evaluate(X_test, y_test)

print("Accuracy:", accuracy)
```

---

# 🚀 Future Improvements

Some possible enhancements:

* 🔧 Hyperparameter tuning
* 🛡️ Adding Dropout layers
* 📚 Using larger datasets
* 📊 Cross-validation
* 🧠 Building deeper neural networks

---

# 🎓 Conclusion

This project provides a clear introduction to:

* Artificial Neural Networks (ANN)
* Deep Learning basics
* Binary Classification
* TensorFlow and Keras workflows

It is a great beginner project for learning how neural networks can be used in real-world healthcare prediction systems.
