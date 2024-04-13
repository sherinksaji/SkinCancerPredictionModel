
# Project Title
Detection of Melanoma via Skin Lesion Images (Theory and Practice of Deep Learning, SUTD)



## Run Locally

Clone the project

```bash
    git clone https://github.com/sherinksaji/SkinCancerPredictionModel.git
```

Download the dataset from Kaggle

```bash
    https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000
```

Add channels on conda

```bash
    conda config --add channels pytorch
    conda config --add channels conda-forge
    conda config --add channels nvidia
```

Adjust Repository Priorities to allow packages from lower-priority channels when necessary

```bash
    conda config --set channel_priority flexible
```

Create new conda environment from requirements.txt

```bash
    conda create --name dl_test --file requirements.txt
```


## Datasets Utilized

Please download the dataset on HAM10000 skin lesion images from:
https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000
  

## Model Architecture

![alt text](https://github.com/sherinksaji/SkinCancerPredictionModel/blob/main/model_architecture.png)



## Model Inputs and Outputs

•	Model's inputs : png image of the skin lesion of concern

•	Model output: label of 0 or 1, indicating whether a person has healthy skin or is at the onset of skin cancer. 
  - '0' means malignancy of melanoma
  - '1' means benign of melanoma

## Table Of Contents

- Project Notebook:
    - Deep Learning Project.ipynb


- metadata
    - data
        - HAM10000_metadata.csv
        - HAM10000_images (Image directory)
    
    - models
        - combined_model_epoch_10.pth 
            - Checkpoint at 10th epoch
        - combined_model_epoch_20.pth
            - Checkpoint at 20th epoch
        - combined_model_epoch_30.pth
            - Checkpoint at 30th epoch
        - combined_model_epoch_40.pth
            - Checkpoint at 40th epoch
        - combined_model_epoch_50.pth
            - Checkpoint at 50th epoch

    - train folder
        - mel folder: Contains images of melanoma
        - no_mel folder: Contains images of no melanoma

    - validation folder
        - mel folder: Contains images of melanoma
        - no_mel folder: Contains images of no melanoma
    
    - test folder
        - mel folder: Contains images of melanoma
        - no_mel folder: Contains images of no melanoma
     
          
## Requirements

The Jupyter Notebook is written in Python (3.12.2 version required).

This project requires you to install the listed libraries in the requirement.txt file and Anaconda distribution Python 3.12

The main packages used are:


- numpy - Fundamental package for scientific computing with Python. It provides support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.

- pandas - Powerful data structures for data analysis, time series, and statistics.

- matplotlib - Comprehensive library for creating static, animated, and interactive visualizations in Python.

- scipy - Library used for scientific and technical computing.

- scikit-learn - Simple and efficient tools for predictive data analysis.

- torch - Deep learning framework and scientific computing package.

- torchvision - Package consists of popular datasets, model architectures, and common image transformations for computer vision.

- jupyter, ipykernel, notebook, ipywidgets - Packages related to Jupyter Notebooks which provide an interactive computational environment for combining code execution, rich text, mathematics, plots, and rich media.

- pytorch - The PyTorch library itself, specified with CUDA support.



## Core Dependencies and Libraries

- cudatoolkit 11.8 - NVIDIA CUDA Toolkit, essential for GPU-accelerated PyTorch operations.

- libnpp, libcublas, libcusparse, etc. - Various CUDA libraries that provide GPU-accelerated operations for different types of computing.

- mkl - Intel Math Kernel Library, highly optimized for mathematical operations on Intel architectures.

## Results

The model trained achieved an F1-score of 94%; recall of 97%; accuracy of 90% and precision of 91% on evaluation dataset.
