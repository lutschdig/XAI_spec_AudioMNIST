# XAI_spec_AudioMNIST
This repository was created for the Master-Thesis with the title:
***Explainable artificial intelligence (XAI) for spectrogram-based classification of univariate time series data: A survey and experimental study***

## Description

The folder structure is as follows:

Note: some code snippets were adopted or are based on other repositories/sources, which is stated in the concerned cells. 

## Requirements
* All experiments were conducted Google Colab (recommended Pro+ high Ram and GPU)
* Script 2 requires the outputs of script 1

* python
* tensorflow
* numpy
* pandas
* Matplotlib
* h5py
* sklearn
* Keras
* skimage
* lime-0.2.0.1
* scipy
* librosa
* multiprocessing
* glob

* Please refer to the Import sections of the two ipynb notebooks for a list of all necessary packages

## Usage
1. Clone or download this repository into your Google Drive root folder (if you use a subfolder, you have to adjust the root_path in the ipynb notebooks)
2. Run all cells of the first script  [`01_Preprocessing_Training_Evaluation.ipynb`](01_Preprocessing_Training_Evaluation.ipynb) within Google Colab* in order to:
- Download dataset
- Create spectrograms
- Train models (K-Fold for two labels digit and gender)
- Evaluate models (accuracy, confusion matrix and loss plots)
3. Run all cells above the section "Set parameters and run script" of the second script [`01_Preprocessing_Training_Evaluation.ipynb`](01_Preprocessing_Training_Evaluation.ipynb) within Google Colab
4. 


Afterwards the explanations can be created and explored with the second script [`01_Preprocessing_Training_Evaluation.ipynb`](01_Preprocessing_Training_Evaluation.ipynb)

*it is highly recommended to use Google Colab Pro+ with GPU runtime and high RAM setup, more information in the script!

## Results
Due to the large amount of data, the results are not synchronized in this repository. However, the results are presented and discussed in the Master-Thesis.





