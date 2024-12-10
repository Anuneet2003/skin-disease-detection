# Skin Cancer Detection and Classification

This project uses a DenseNet121 model to detect and classify 9 different types of skin lesions cancer from images.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model](#model)
- [Training](#training)
- [Evaluation](#evaluation)

## Installation

1. Make sure you have Python 3.x installed.
2. Install the required libraries:
   bash pip install tensorflow tensorflow-datasets kagglehub tqdm matplotlib
3. Install Kaggle API:
   - Install Kaggle library `pip install kaggle`.
   - Create a Kaggle API token by following instructions [here](https://www.kaggle.com/docs/api).
   - Place `kaggle.json` file inside `~/.kaggle` directory.

## Usage

1. Download the dataset using the provided code.
2. Run the code to train and evaluate the model.
3. Visualize the training and validation accuracy and loss.

## Dataset

The dataset used in this project is the "Multiple Skin Disease Detection and Classification" dataset from Kaggle. It contains images of 9 different skin diseases. The dataset is automatically downloaded by the code.

## Model

The model used in this project is a DenseNet121 pre-trained on ImageNet. The top layers are removed and replaced with custom layers for classification. The last 10 layers of the base model are fine-tuned.

## Training

The model is trained using an `ImageDataGenerator` to augment the training data. The training is performed for 10 epochs using the Adam optimizer and categorical cross-entropy loss.

## Evaluation

The model's performance is evaluated on the validation set. The accuracy and loss are plotted to visualize the training progress.
