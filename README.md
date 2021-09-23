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
1. Clone or download this repository into your Google Drive root folder (if you use a subfolder, you have to adjust the root_path in the ipynb notebooks)
2. Run all cells of the first script  [`01_Preprocessing_Training_Evaluation.ipynb`](01_Preprocessing_Training_Evaluation.ipynb) within Google Colab* in order to:
- Download dataset
- Create spectrograms (.hdf5 files)
- Create splits
- Train models (K-Fold for two labels digit and gender)
- Evaluate models (accuracy, confusion matrix and loss plots)
3. Run all cells above the section "Set parameters and run script" of the second script [`01_Preprocessing_Training_Evaluation.ipynb`](01_Preprocessing_Training_Evaluation.ipynb) within Google Colab
4. Use the three possibilites of section "Set parameters and run script" to create explanations (detailed information on the options are explained in the script):
a) For several spectrograms: Output examples for each model (see options in the script)
b) For a specific spectrogram/model: Outputs for one spectrogram 
c) For filtered spectrograms: Outputs for several spectrograms, filtered by wrongly or correctly predicted
5. Additionally, section "Input information" can be used to:
- print a table with wrongly or correctly predicted spectrograms of a specific model
- print which participants are in the test split of a specific model
- print the gender of one or more participants



*it is highly recommended to use Google Colab Pro+ with GPU runtime and high RAM setup, more information at the beginning of the script!

## Results
Due to the large amount of data, the results are not synchronized in this repository. However, the results are presented and discussed in the Master-Thesis.


## Folder structure (will be created with the scripts):

    XAI_spec_AudioMNIST				# root folder of the repository
    ├──AudioMNIST-master				# downloaded dataset
    |	├──data
    |	|	├──01				# contains .wav files (raw data) of participant 01
    |	|	├──...				# same for each of the participants
    |	|	└──audioMNIST_meta.txt		# contains meta information on the participants							
    |	└──...					# other files and folders are irrelevant
    ├──results
    |	├──evaluation
    |	|	├──confusionMatrix_digit_0.csv	# contains the confusion matrix for label digit and fold 0
    |	|	├──...				# same for each label and fold, additionally mean for each label
    |	|	├──evalutation_digit_0.csv	# contains performance indicators (accuracy) for label digitand fold 0	
    |	|	└──...				# same for each label and fold, additionally mean for each label
    |	├──history
    |	|	├──AlexNet_digit_0.pkl		# contains the history of label digit and fold 0
    |	|	└──...				# same for each label and fold
    |	├──models
    |	|	├──AlexNet_digit_0.h5		# contains the model of label digit and fold 0
    |	|	└──...				# same for each label and fold
    |	├──plots
    |	|	├──loss				# contains the loss plots as .png files
    |	|	├──spectrograms			# contains the spectrograms as .png files
    |	|	├──waveform			# contains the waveform plots as .png files
    |	|	└──xai				# contains the explanations as .png files for Grad-CAM and LIME
    |	└──predictions
    |		├──predictions_digit_0.csv	# contains the predictions of label digit and fold 0
    |		└──...				# same for each label and fold	
    ├──spectrograms
    |	├──01					# contains .hdf5 files (spectrograms) of participant 01
    |	└──...					# same for each of the participants
    ├──splits					# here: split = fold
    |	├──AlexNet_digit_0_test.txt		# contains paths to spectrograms (.hdf5 files) for label digit, fold 0 and testsplit
    |	└──...					# same for each label, fold and split
    ├──01_Preprocessing_Training_Evaluation.ipynb	# script 1 contains code for downloading dataset, creating spectrograms (.hdf5 files), training models, 
    ├──02_XAI_methods.ipynb				# script 2 contains code for creating outputs as .png files (waveform plots, spectrograms, Grad-CAM, LIME) 
    ├──events.log					# contains logs, produced while running the code
    ├──LICENSE
    └──README.md

