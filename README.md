# CNN for CIFAR-10 Image Classification

This project builds a Convolutional Neural Network using PyTorch to classify images from the CIFAR-10 dataset into 10 categories.

## Project Overview

CIFAR-10 contains 60,000 color images of size 32x32 across 10 classes. The goal of this project is to train a CNN model that can learn visual features from these images and predict the correct class for unseen test images.

## Tech Stack

- Python
- PyTorch
- TorchVision
- Jupyter Notebook

## Dataset

This project uses the CIFAR-10 dataset from `torchvision.datasets.CIFAR10`.

The dataset is not included in this repository because it is large and publicly available. It will be downloaded automatically when the notebook is run:

```python
from torchvision.datasets import CIFAR10

trainset = CIFAR10(root="./data", train=True, download=True, transform=transform)
testset = CIFAR10(root="./data", train=False, download=True, transform=transform)
```

## Model Architecture

The CNN model contains:

- 3 convolutional blocks
- ReLU activation functions
- Max pooling layers
- Fully connected layers
- Final output layer with 10 classes

## Results

The model was trained for 10 epochs and achieved approximately 75% test accuracy.

## How to Run

1. Clone this repository.
2. Install the dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook CNN_for_CIFAR10.ipynb
```

4. Run all cells.

## Project Files

- `CNN_for_CIFAR10.ipynb` - main notebook containing model training and evaluation
- `requirements.txt` - Python dependencies
- `.gitignore` - excludes dataset files, checkpoints, virtual environments, and model artifacts
- `images/` - optional folder for result screenshots such as accuracy/loss curves or sample predictions

## Future Improvements

- Add training and validation accuracy/loss visualization
- Add confusion matrix
- Use data augmentation
- Save and reload the trained model
- Tune hyperparameters for better accuracy
