# 🔍 Face Swap Deepfake Image Detection using CNN

An AI/ML-based project that aims to identify face-swapped deepfake images using deep learning techniques.

This project uses **PyTorch and a pre-trained ResNet50 model** to classify facial images into two categories: Real and Fake. The model uses image preprocessing and transfer learning to learn visual patterns that help distinguish authentic images from manipulated images.

## 🎯 Project Objective

The main objective is to develop a deep learning-based solution for detecting face-swap deepfake images and helping improve the authenticity of digital media.

The project focuses on:
- Classifying images as Real or Fake.
- Applying image preprocessing techniques.
- Using a pre-trained CNN architecture for binary classification.
- Exploring face detection and extraction using MTCNN.
- Providing predictions for individual images.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| PyTorch | Deep learning framework |
| ResNet50 | Pre-trained CNN architecture |
| Torchvision | Image transformations and model utilities |
| MTCNN | Face detection utility |
| PIL | Image loading and processing |
| NumPy | Numerical operations |
| Jupyter Notebook | Development environment |

## ⚙️ Project Workflow

1. **Image Dataset:** Use real and fake facial images as input.
2. **Preprocessing:** Resize images to 224 × 224 pixels, convert them into tensors, and normalize pixel values.
3. **Dataset Preparation:** Assign labels to real and fake images using a custom PyTorch Dataset class.
4. **Model Development:** Load a pre-trained ResNet50 model and modify its final fully connected layer for binary classification.
5. **Training:** Train the model using Binary Cross Entropy with Logits Loss and the Adam optimizer.
6. **Prediction:** Pass an image through the trained model and classify it as Real or Fake using a 0.5 probability threshold.

## 🧠 Model Architecture

**ResNet50 – Transfer Learning**

ResNet50 is a Convolutional Neural Network architecture that uses residual connections to learn image features effectively.

In this project:
- A pre-trained ResNet50 model is loaded.
- The final classification layer is modified for one-output binary classification.
- The model is trained to distinguish real and fake images.
- Sigmoid activation is used to convert model output into a probability.

## 📂 Project Structure

```text
Face-Swap-Deepfake-Detection/
│
├── IPL Project.ipynb
├── requirements.txt
├── README.md
├── .gitignore
│
└── images/
    └── screenshots/
```

## 💻 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/BrundaShankar/Face-Swap-Deepfake-Detection.git
```

### 2. Navigate to the Project Folder

```bash
cd Face-Swap-Deepfake-Detection
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `IPL Project.ipynb` and execute the notebook cells.

**Note:** The current notebook uses local Windows dataset paths. Update the image paths to match your own dataset before running it. The dataset itself is not included in this repository.

## 📊 Model Training

The notebook currently demonstrates:
- Image resizing and normalization.
- Dataset creation using PyTorch.
- ResNet50 model initialization.
- Binary classification using `BCEWithLogitsLoss`.
- Adam optimization.
- Training over five epochs.
- Training loss and accuracy output.

## 🔎 Image Prediction

The notebook includes a `predict_image()` function that:
1. Loads an input image.
2. Applies the required transformations.
3. Passes the image through the trained model.
4. Calculates the prediction probability.
5. Displays the result as Real or Fake.

## ⚠️ Current Limitations

- The current notebook uses a small hard-coded sample of image paths.
- A separate test dataset and complete evaluation pipeline are not yet included.
- The trained model is not currently saved as a reusable model file.
- MTCNN face extraction is defined separately and is not integrated into the current training pipeline.
- Video-based deepfake detection is not implemented.

## 🚀 Future Enhancements

- Integrate a larger and more diverse real/fake image dataset.
- Implement proper training, validation, and testing splits.
- Evaluate the model using accuracy, precision, recall, F1-score, and a confusion matrix.
- Save and reload trained model weights.
- Integrate MTCNN face detection into the image preprocessing pipeline.
- Develop a user interface for uploading and classifying images.
- Extend the system to video-based deepfake detection.

## 📚 Project Domain

Artificial Intelligence | Machine Learning | Deep Learning | Computer Vision | Digital Media Security

## 👩‍💻 Contributors

Developed as an academic project at BNM Institute of Technology.

## ⚠️ Disclaimer

This project is an academic prototype for deepfake image classification. Predictions should not be treated as definitive proof of image authenticity. Further testing on diverse and unseen datasets is required before real-world use.
