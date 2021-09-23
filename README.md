# XAI_spec_AudioMNIST
This repository was created for the Master-Thesis with the title:
***Explainable artificial intelligence (XAI) for spectrogram-based classification of univariate time series data: A survey and experimental study***

## Description

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
1. eins 
2. zwei


First the models must be trained and evaluated with the first script [`01_Preprocessing_Training_Evaluation.ipynb`](01_Preprocessing_Training_Evaluation.ipynb):
Just run all cells. If you run out of memory at a certain point, just rerun all cells.

Afterwards the explanations can be created and explored with the second script [`01_Preprocessing_Training_Evaluation.ipynb`](01_Preprocessing_Training_Evaluation.ipynb)

## Results
Due to the large amount of data, the results are not synchronized in this repository. However, the results are presented and discussed in the Master-Thesis.




