# Facial Recognition System

**Author: Sunkireddy Barath**

A complete and intuitive Face Recognition project using OpenCV and Python. This repository provides everything you need to train a face recognizer using your own images and identify subjects in test images.

## Features

- Uses **Local Binary Patterns Histograms (LBPH)** for accurate face recognition.
- Includes preconfigured `training-data` and `test-data` directories.
- Demonstrates how to detect faces using OpenCV's `CascadeClassifier`.
- Includes both a modular `.py` script and an interactive `.ipynb` Jupyter Notebook for exploration.
- Supports extending to other recognizers available in OpenCV like EigenFaces and FisherFaces.

## Project Structure

```text
/home/barath/-Facial-Recognition
└── opencv-face-recognition-python-master/
    ├── OpenCV-Face-Recognition-Python.py         # Main Python script for face recognition
    ├── OpenCV-Face-Recognition-Python.ipynb      # Interactive Jupyter notebook
    ├── README.md                                 # Original detailed tutorial README
    ├── training-data/                            # Directory containing training images
    │   ├── s1/                                   # Subject 1 images
    │   └── s2/                                   # Subject 2 images
    ├── test-data/                                # Directory for testing images
    ├── opencv-files/                             # Pre-trained Haar & LBP cascades
    └── output/                                   # Example output images
```

## How It Works

The system operates in three main steps:
1. **Training Data Preparation:** The system reads images from the `training-data` folder. Each subfolder (e.g., `s1`, `s2`) represents a unique individual. The images are processed to detect the facial boundaries.
2. **Model Training:** The detected faces and their respective labels are fed into the OpenCV LBPH Face Recognizer `cv2.face.createLBPHFaceRecognizer()`.
3. **Prediction:** A test image is provided to the system. It detects the face and predicts the label of the subject based on the trained model, outputting the predicted name visually on the image.

## Setup & Usage

### Dependencies

Make sure you have the following Python libraries installed:
- `opencv-contrib-python` (Required for the `cv2.face` module)
- `numpy`
- `matplotlib` (For Jupyter notebook visualizations)

```bash
pip install opencv-contrib-python numpy matplotlib
```

### Running the Python Script

Navigate to the project source directory and run the main script:

```bash
cd opencv-face-recognition-python-master
python OpenCV-Face-Recognition-Python.py
```

### Running the Jupyter Notebook

For an interactive tutorial experience, open the notebook:

```bash
cd opencv-face-recognition-python-master
jupyter notebook OpenCV-Face-Recognition-Python.ipynb
```

## License

This project is licensed under the MIT License. Copyright (c) 2017 Sunkireddy Barath.
