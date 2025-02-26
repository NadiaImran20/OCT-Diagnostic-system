# OCT Image Classification

## Project Overview

This project implements a deep learning model for classifying Optical Coherence Tomography (OCT) images into four categories: CNV, DME, DRUSEN, and NORMAL.  The model leverages transfer learning with pre-trained architectures (ResNet50, DenseNet121, or InceptionV3) to achieve accurate and efficient classification.  A Gradio interface provides an easy-to-use platform for uploading OCT images and receiving predictions.


## Description

The model undergoes a two-phase training process:

1. **Initial Training:** The base model's weights are frozen, and only the top layers are trained to adapt to the OCT dataset.
2. **Fine-tuning:**  A subset of the top layers of the base model are unfrozen and trained with a lower learning rate to further refine the model's performance.


## Dataset

The dataset used for training and evaluation is an OCT image dataset (OCT.rar).  The dataset is expected to be placed in your Google Drive.  Make sure to adjust the `DATASET_RAR_PATH` variable in the script to reflect the correct path on your drive.  The dataset is organized into folders, each corresponding to a disease class.


## Usage

1. **Setup:** Ensure you have the required libraries installed (see `requirements.txt`).  You can install them using `pip install -r requirements.txt`.
2. **Data Preparation:**  Upload the OCT.rar file to your Google Drive and update the `DATASET_RAR_PATH` variable.
3. **Run the Notebook:** Execute the Jupyter Notebook. This will mount your Google Drive, extract the dataset, train the model, and launch the Gradio interface.
4. **Classification:** Use the Gradio interface to upload an OCT image and receive the model's classification prediction.


## Future Work

* **Data Augmentation:** Implement more advanced data augmentation techniques to improve model robustness.
* **Hyperparameter Tuning:** Perform a more thorough hyperparameter search to optimize model performance.
* **Ensemble Methods:** Explore ensemble methods to combine multiple models for improved accuracy.


## Acknowledgments

This project was inspired by Kaggle datasets and community contributions. Special thanks to those who provided public OCT image datasets.


## Downloading the README

This README.md file can be downloaded directly from the Colab environment.

