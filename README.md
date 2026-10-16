# 🍎 Fruit Image Reconstruction Using Variational Autoencoders (VAE)

## 📌 Project Overview

This project explores image reconstruction using Variational Autoencoders (VAE) on fruit images. It implements and evaluates convolutional encoder-decoder architectures to learn latent representations and reconstruct input images.

The project compares a baseline VAE with a modified VAE architecture and evaluates reconstruction quality using training and validation loss, as well as Fréchet Inception Distance (FID).

## 🎯 Project Objectives

- Build a baseline convolutional VAE.
- Develop a modified VAE architecture.
- Learn latent representations of fruit images.
- Reconstruct images from latent representations.
- Compare training and validation loss.
- Evaluate reconstruction quality using FID scores.

## 📂 Dataset

The fruit image dataset was provided through Google Drive as part of an academic assignment. Due to its large file size and access restrictions, the dataset is not included in this repository.

To reproduce the experiment, users must obtain the dataset from an authorized source and update the dataset path in the notebook accordingly.

## 🧹 Data Preprocessing

The preprocessing pipeline includes:

- Removing unwanted `.DS_Store` metadata files.
- Resizing images to 100 × 100 pixels.
- Converting images from BGR to RGB.
- Normalizing pixel values to the range [0, 1].
- Preparing image datasets for training, validation, and testing.

## 🧠 Model Development

### 1. 🔹 Baseline VAE

The baseline model uses a convolutional encoder to learn a latent representation and a decoder to reconstruct images from that representation.

### 2. 🔹 Modified VAE

The modified architecture introduces architectural changes, including batch normalization and a larger latent dimension, to explore their effect on training behavior and image reconstruction.

## 📊 Evaluation Metrics

### 📉 Training and Validation Loss

Training and validation loss are monitored to examine the model's learning behavior and reconstruction performance.

### 🖼️ Fréchet Inception Distance (FID)

FID is used to evaluate the similarity between feature distributions of reference images and reconstructed images. Lower FID scores generally indicate greater similarity between the distributions.

The notebook reports FID scores for the modified model (`vae_c`) across six fruit categories.

| Fruit Category | FID Score |
|---|---:|
| Fresh apples | 384.84 |
| Fresh banana | 525.28 |
| Fresh oranges | 421.48 |
| Rotten apples | 404.32 |
| Rotten banana | 411.39 |
| Rotten oranges | 374.32 |

These values are the results recorded in the notebook and should be interpreted in the context of its specific FID implementation and evaluation setup.

## 🛠️ Tools and Technologies

- Python
- TensorFlow / Keras
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn
- Computer Vision
- Variational Autoencoders (VAE)

## 📁 Project Structure

- `README.md` — Project overview, methodology, and evaluation results.
- `vae-fruit-image-reconstruction.ipynb` — Notebook containing preprocessing, VAE model development, training, and evaluation code.

## 🚀 How to Run

1. Clone or download this repository.
2. Open the notebook in Google Colab or a compatible Jupyter environment.
3. Make the fruit image dataset available in the environment.
4. Update dataset paths if necessary.
5. Run the notebook cells in sequence.
6. Review training curves and FID evaluation results.

The notebook requires the relevant Python libraries and access to the dataset.

## 👩‍💻 Author
**Amanda Sugito**

Deep Learning academic project at BINUS University.

## 🔗 Connect with Me
- LinkedIn: Amanda Sugito | www.linkedin.com/in/amanda-sugito
- GitHub: amandasugito | https://github.com/amandasugito

## ⚠️ Limitations

- Reconstruction quality varies across fruit categories.
- FID scores depend on the implementation and the images used for evaluation.
- The reported FID values evaluate the modified model and do not represent a direct FID comparison between both VAE architectures.
- Further experiments may be needed to assess generalization and improve reconstruction quality.

This project was developed for academic purposes as a deep learning and computer vision exercise.
