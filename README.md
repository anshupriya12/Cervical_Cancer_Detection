# Cervical Cancer Detection

A Pap smear classification project for detecting cervical cancer using deep learning and transfer learning.

## Overview
This project applies a transfer learning approach to classify Pap smear images into five cervical cell categories. The model is built using a pre-trained ResNet101V2 backbone and fine-tuned for this classification task.

## Dataset
The dataset used in this project contains multiple cervical cell image folders, organized by class. The model is trained on five classes:

- im_Dyskeratotic
- im_Koilocytotic
- im_Metaplastic
- im_Parabasal
- im_Superficial-Intermediate

## Model Architecture
The notebook implements a transfer learning model based on ResNet101V2:

- Base model: ResNet101V2 (ImageNet pre-trained weights)
- Input shape: (128, 128, 3)
- Output classes: 5
- Activation: softmax
- Loss: categorical crossentropy
- Optimizer: Adam
- Metric: accuracy

## Training Workflow
The notebook includes the following core steps:

1. Loading image datasets from class folders
2. Resizing images to 128x128
3. Normalizing pixel values to the range [0, 1]
4. Preparing one-hot encoded labels
5. Training a transfer learning model using ResNet101V2
6. Evaluating the model on a test set

## Image Preprocessing
The project uses the following preprocessing pipeline for training and inference:

- Resize images to 128 x 128
- Convert images to RGB
- Scale pixel values by dividing by 255.0
- Use image folders for class-based loading via `ImageDataGenerator.flow_from_directory()`

## Requirements
To run the notebook and related scripts, install the necessary dependencies:

```bash
pip install tensorflow numpy pandas opencv-python scikit-learn keras pillow matplotlib tqdm
```

## Repository Contents
- `TransferLearning_papsmeartest.ipynb` — main notebook containing training, preprocessing, and evaluation logic
- `LICENSE` — project license
- `README.md` — project documentation

## Running the Notebook
Open the notebook in Jupyter or JupyterLab:

```bash
jupyter notebook TransferLearning_papsmeartest.ipynb
```

or

```bash
jupyter lab
```

Then run the cells in order to train and evaluate the model.

## Notes
This project is intended for research and experimentation with cervical cell classification using transfer learning. The notebook demonstrates the complete model-building and evaluation workflow.
