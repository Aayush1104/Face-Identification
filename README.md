# Facial Recognition using Siamese Neural Networks

Facial Recognition project that utilizes Siamese Neural Networks for verification and identification of faces.

## Introduction

This project demonstrates the implementation of facial recognition using Siamese Neural Networks. The Siamese architecture is utilized for face verification and identification tasks. The project captures real-time images, processes them, and verifies their authenticity based on a trained model. It provides a foundation for building facial recognition systems that can be used in various applications, such as access control, security systems, and more.

## Installation

1. Clone the repository:

    ```bash
   git clone https://github.com/your-username/facial-recognition.git
   cd facial-recognition
    ```
2. Install the required dependencies:
    ```bash
    pip install tensorflow==2.12.0 opencv-python matplotlib
    ```
3. Download the pre-trained model weights and place them in the project directory.

## Usage

1. **Collect Images:**
   - Run the script to capture images using your webcam.
   - Press 'a' to collect anchor images.
   - Press 'p' to collect positive (verified) images.
   - Press 'q' to exit the image collection.

2. **Train the Model:**
   - Run the training script to train the Siamese Neural Network.
   - Modify parameters in the training script to suit your needs.

3. **Verification:**
   - Run the verification script.
   - Press 'v' to capture an input image for verification.
   - The script will display whether the verification is successful.

## Model Overview
The Siamese Neural Network consists of two identical subnetworks, both sharing weights. It computes a distance metric between the input and validation images. This distance is then used to determine whether the images belong to the same person (verification).

The network architecture is defined in build_embedding_layer(). The Siamese model is created using the embedding model and make_siamese_model().

## Results
The trained model's performance can be evaluated using precision and recall metrics. Test data predictions are compared against ground truth labels to assess the model's accuracy in verifying faces.

To visualize the results, the precision and recall metrics are calculated and displayed using Precision() and Recall() classes from TensorFlow.
