# DynaGraph

This repository is an implementation of DynaGraph: Dynamic Contrastive Graph for Interpretable Multi-label Prediction using Time-Series EHR Data. 

## Requirements

To install requirements:

```setup
pip install -r requirements.txt
```
## Data

We have included notebooks detailing parts of the extraction procedure for the patient subcohorts for eICU and MIMIC-III. We have also included the pre-processing steps as relevant. We have also included the .npy files to reproduce the results for eICU but because of the size of the MIMIC III cohorts, the size of the files for MIMIC III cannot be uploaded. We will provide them in a separate hosting service later on. Please note that these rely on access to large .csv files from PhysioNet which you can obtain after certification here: https://physionet.org/content/eicu-crd/2.0/ and https://physionet.org/content/mimiciii/1.4/

For HiRID ICU please follow guidance from the official providers on obtaining the imputed dataset: https://github.com/HIRID/HiRID_v1

EHRSHOT data can be accessed after making a request here: https://redivis.com/datasets/53gc-8rhx41kgt

## Training

To train the model(s) in the paper, run the notebook in the Train.ipynb file. You can adjust number of layers, graphs, slices in the model definition. The learning rate and parameters can be adjusted accordingly in the function calls.

## Evaluation

To evaluate the model and retrieve the results for a particular seed, run the Evaluate.ipynb notebook.

The dataset samples are located in the Data folder and are loaded in the notebook accordingly. The ones for MIMIC-III are labeled with an 'X' in the title. The numbers at the end correspond to the respective seeds under which the data splits were generated.

The pre-trained models for the benchmarks are in the models folder. Due to the size limitations, we only include one of the seed runs: 1992 on eICU.

## Interpretability

To obtain the interpretability figures, please run the Explainability_Figures.ipynb notebook. We have included examples of how to visualise the weights on the test set, but the same can be done for the training weights. The weights are saved in the Interpretability Weights folder for eICU and MIMIC III respectively.
