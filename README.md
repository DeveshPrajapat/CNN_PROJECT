# 🥔 Potato Leaf Classification Using CNN

An image classification project that uses a **Convolutional Neural Network (CNN)** built with TensorFlow and Keras to classify potato leaf images. The project includes a simple interactive web interface developed using Streamlit.

## 🚀 Project Overview

This project uses Deep Learning to identify potato leaf categories from uploaded images.

Users can upload a JPG image through the Streamlit application and get:
- Predicted potato leaf class.
- Prediction confidence score.
- Probability scores for all classes.

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Pillow (PIL)
- Streamlit

## 📁 Project Structure

```text
archive/
│
├── data/
│   ├── Potato___Early_blight/
│   ├── Potato___healthy/
│   └── Potato___Late_blight/
│
├── dev/                       # Virtual environment
│
├── app.py                     # Streamlit application
│
├── cnn_code.ipynb             # CNN model training notebook
│
├── potato_cnn_model.keras     # Saved trained CNN model
│
└── classification_report.txt  # Saved class names
```

**Note:** The model and class-name files are generated after running the training notebook. They must be present in the project root to run the Streamlit prediction application.

## 🧠 CNN Model Architecture

The project uses a Sequential CNN architecture with three main components:

### 1. Feature Extraction
- Conv2D (16 filters)
- MaxPooling2D
- Conv2D (32 filters)
- MaxPooling2D
- Conv2D (64 filters)
- MaxPooling2D

### 2. Flatten Layer
- Converts extracted feature maps into a one-dimensional vector.

### 3. Classification
- Dense (64 neurons, ReLU)
- Dropout (0.2)
- Dense (3 neurons, Softmax)

## ⚙️ Model Configuration

| Parameter | Value |
|---|---|
| Input Image Size | 128 × 128 |
| Color Mode | RGB |
| Batch Size | 32 |
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Activation | ReLU, Softmax |
| Epochs | 8 |
| Data Split | 80% Training, 20% Validation |
| Data Augmentation | Horizontal Flip, Rotation |
| Output Classes | 3 |

Class weights are also used during training to help address class imbalance.

## 🖥️ Streamlit Application

The Streamlit frontend provides a simple interface for image classification.

### Features

- Simple user interface.
- Home and About navigation.
- JPG/JPEG image upload.
- Uploaded image preview.
- CNN model integration.
- Predicted class display.
- Confidence percentage.
- Class-wise probability visualization.

## 🔄 Application Workflow

```text
User Uploads Image
        |
        v
Streamlit Interface
        |
        v
Image Preprocessing
(128 × 128 RGB)
        |
        v
Load Trained CNN Model
        |
        v
CNN Model Prediction
        |
        v
Softmax Probabilities
        |
        v
Predicted Class
        |
        v
Display Result in Streamlit
```

## 💻 Installation and Setup

### 1. Clone Repository

```bash
https://github.com/DeveshPrajapat/CNN_PROJECT
```

### 2. Navigate to Project Folder

```bash
cd archive
```

### 3. Create Virtual Environment

```bash
python -m venv dev
```

### 4. Activate Virtual Environment

**Windows PowerShell:**

```powershell
.\dev\Scripts\Activate.ps1
```

### 5. Install Dependencies

```bash
pip install tensorflow streamlit numpy pillow matplotlib
```

### 6. Run CNN Training Notebook

Open `cnn_code.ipynb` in Jupyter Notebook or VS Code and execute the training cells.

After training, the following files should be generated:

```text
potato_cnn_model.keras
classification_report.txt
```

### 7. Run Streamlit Application

```bash
streamlit run app.py
```

The application will open in your browser.

## 📊 Model Evaluation

The CNN notebook includes:

- Training and validation accuracy.
- Training and validation loss graphs.
- Confusion matrix.
- Unseen image prediction.
- Class-wise prediction probabilities.

Validation accuracy is evaluated using the validation dataset. It should not be interpreted as test accuracy.

## 🔮 Future Improvements

- Hyperparameter tuning.
- Batch Normalization.
- Model Checkpointing.
- Early Stopping.
- Learning rate optimization.
- Improved model generalization.
- Deployment of the Streamlit application.

## 👨‍💻 Author

**Devesh Prajapat**

GitHub: [DeveshPrajapat](https://github.com/DeveshPrajapat)

LinkedIn: [Devesh Prajapat](https://www.linkedin.com/in/devesh-prajapat-696162335/)

---

⭐ If you find this project useful, consider giving it a star!
