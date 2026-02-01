# Denoising Autoencoder (DAE)

A **Denoising Autoencoder (DAE)** implemented using **TensorFlow/Keras** to remove noise from images. This project demonstrates how an autoencoder can learn robust feature representations by reconstructing clean images from noisy inputs, making it useful for **image denoising, preprocessing, and enhancement tasks**.

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Architecture](#architecture)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [References](#references)

---

## Introduction

Autoencoders are a type of neural network designed to learn efficient representations of data, typically for **dimensionality reduction or feature learning**. A **Denoising Autoencoder** extends this concept by training the network to **reconstruct clean data from noisy input**, improving its robustness to corrupted data.

This project demonstrates a DAE applied to image data, showing how it can restore noisy images while preserving important details.

---

## Features

- Removes Gaussian and salt-and-pepper noise from images
- Built with **TensorFlow 2.x** and **Keras**
- Easy-to-train architecture suitable for small to medium-sized datasets
- Provides reconstruction visualization for noisy vs. denoised images
- Can be extended for grayscale or RGB image denoising

---

## Architecture

The Denoising Autoencoder consists of:

- **Encoder:** Compresses the input image into a latent representation
- **Bottleneck:** Encodes the essential features in a compressed form
- **Decoder:** Reconstructs the clean image from the latent representation

Typical architecture example:

Input Image (28x28)
│
Conv2D + ReLU
│
MaxPooling2D
│
Conv2D + ReLU
│
Flatten → Dense (Latent Space)
│
Dense → Reshape
│
Conv2DTranspose + ReLU
│
UpSampling2D
│
Output Image (Denoised)

---

## Dataset

- You can use datasets like **MNIST**, **CIFAR-10**, or your custom image dataset.
- Images are normalized to [0,1] and Gaussian or salt-and-pepper noise is added before training.

---

## Installation

1. Clone this repository:

```bash
git clone https://github.com/yourusername/dae-image-denoising.git
cd dae-image-denoising
Create a virtual environment (optional but recommended):

```
2. Create a virtual environment (optional but recommended):
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```
3.Install dependencies:
```bash
pip install -r requirements.txt
```

## Results

Sample denoising results:


<img width="794" height="394" alt="image" src="https://github.com/user-attachments/assets/e017decd-2f39-4fd0-b6be-b75e468dcf66" />
<img width="872" height="2352" alt="image" src="https://github.com/user-attachments/assets/2d18652e-01f0-408e-82c8-20e83339c168" />


The autoencoder successfully removes noise while preserving key features of the original image.

## Contributing
Contributions are welcome! Please follow these steps:

-Fork the repository
-Create a new branch (git checkout -b feature/YourFeature)
-Commit your changes (git commit -m 'Add feature')
-Push to the branch (git push origin feature/YourFeature)
-Open a Pull Request

## License

This project is licensed under the MIT License. See the LICENSE
 file for details.
