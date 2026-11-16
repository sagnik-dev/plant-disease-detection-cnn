# 🌱 Plant Disease Detection Using Image Processing

**InternID:** `CITS6320`

## 📌 Project Overview

Plant diseases can significantly affect crop quality and agricultural productivity. Early identification of plant diseases can help farmers take appropriate preventive and corrective measures.

This project focuses on developing a **Plant Disease Detection system using Image Processing and Deep Learning**. The trained machine learning model analyzes images of plant leaves and predicts the corresponding plant disease.

The project uses a trained **Keras/TensorFlow `.h5` model** for image classification.

---

## 🎯 Objectives

The main objectives of this project are:

* Detect diseases from plant leaf images.
* Apply image processing techniques for plant disease classification.
* Use a deep learning model for image-based prediction.
* Classify input leaf images into their respective disease categories.
* Demonstrate how Artificial Intelligence can support agricultural applications.
* Develop a foundation for an automated plant disease detection system.

---

## 🧠 Technologies Used

| Technology                   | Purpose                            |
| ---------------------------- | ---------------------------------- |
| Python                       | Programming language               |
| TensorFlow                   | Deep learning framework            |
| Keras                        | Model development and loading      |
| Jupyter Notebook             | Model implementation and testing   |
| Image Processing             | Leaf image preprocessing           |
| Convolutional Neural Network | Image classification               |
| Google Colab                 | Model training/testing environment |

---

## 📂 Project Structure

```text
plant/
│
├── best_model.h5
├── plant_app.ipynb
└── README.md
```

### Files Description

**`best_model.h5`**

Contains the trained deep learning model used for plant disease prediction.

**`plant_app.ipynb`**

Jupyter Notebook containing the implementation for loading the trained model, processing plant images, and performing disease predictions.

**`README.md`**

Project documentation containing information about the project, technologies, usage, and objectives.

---

## 🔬 Methodology

The overall workflow of the project is:

```text
Input Plant Leaf Image
          ↓
     Image Preprocessing
          ↓
      Image Resizing
          ↓
    Pixel Normalization
          ↓
   Trained Deep Learning Model
          ↓
   Feature Extraction
          ↓
    Disease Classification
          ↓
     Predicted Disease
```

### 1. Image Input

A plant leaf image is provided as input to the system.

### 2. Image Preprocessing

The input image is prepared for the model by applying the required preprocessing operations such as resizing and normalization.

### 3. Model Prediction

The preprocessed image is passed to the trained deep learning model stored in `best_model.h5`.

### 4. Disease Classification

The model generates prediction probabilities for the available disease classes.

### 5. Final Prediction

The class with the highest prediction probability is selected as the predicted plant disease.

---

## 🤖 Machine Learning Model

The project uses a deep learning-based image classification model.

A trained model is saved in:

```text
best_model.h5
```

The model can be loaded using TensorFlow/Keras:

```python
from tensorflow.keras.models import load_model

model = load_model("best_model.h5")
```

The model then accepts a preprocessed plant leaf image and produces a prediction for the corresponding disease class.

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/sagnik-dev/plant.git
```

```bash
cd plant
```

### Step 2: Install Required Libraries

Install the required Python packages:

```bash
pip install tensorflow numpy pillow matplotlib jupyter
```

### Step 3: Open the Notebook

Run:

```bash
jupyter notebook
```

Then open:

```text
plant_app.ipynb
```

Alternatively, the notebook can be opened directly in **Google Colab**.

### Step 4: Load the Trained Model

Make sure `best_model.h5` is available in the notebook's working directory.

```python
from tensorflow.keras.models import load_model

model = load_model("best_model.h5")
```

### Step 5: Provide a Plant Image

Upload or provide a plant leaf image and run the prediction cells in the notebook.

The system will process the image and return the predicted disease class.

---

## 📊 Prediction Process

A typical prediction pipeline can be represented as:

```python
import numpy as np
from PIL import Image

image = Image.open("plant_image.jpg")

image = image.resize((224, 224))

image_array = np.array(image)
image_array = image_array / 255.0

image_array = np.expand_dims(image_array, axis=0)

prediction = model.predict(image_array)

predicted_class = np.argmax(prediction, axis=1)[0]

print("Predicted Class:", predicted_class)
```

> **Note:** The image size and preprocessing steps should match the preprocessing used while training the model.

---

## 🌾 Applications

This type of system can be useful in:

* Smart agriculture
* Crop monitoring
* Early disease detection
* Precision agriculture
* Agricultural decision-support systems
* Automated plant health monitoring
* AI-assisted farming

---

## 🔮 Future Improvements

The project can be further improved by:

* Developing a web-based user interface.
* Creating a mobile application for disease detection.
* Adding more plant species and disease classes.
* Improving model accuracy using data augmentation.
* Using transfer learning models such as MobileNet, EfficientNet, or ResNet.
* Adding confidence scores to predictions.
* Deploying the model using Flask, FastAPI, or Streamlit.
* Adding recommendations for disease management.
* Deploying the application to a cloud platform.

---

## ⚠️ Limitations

The prediction performance depends on:

* Image quality.
* Lighting conditions.
* Leaf orientation.
* Dataset diversity.
* Number of disease classes.
* Training data quality.
* Similarity between real-world images and training images.

Therefore, predictions should be treated as an **AI-assisted classification result** rather than a definitive agricultural diagnosis.

---

## 👨‍💻 Internship Information

**InternID:** `CITS6320`

**Project:** Plant Disease Detection Using Image Processing

**Repository:**
https://github.com/sagnik-dev/plant

---

## 📜 License

This project is intended for **educational and internship purposes**.

---

## ⭐ Acknowledgement

This project demonstrates the application of **Artificial Intelligence, Deep Learning, and Image Processing** to the field of agriculture and plant disease detection.
