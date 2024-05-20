# DynaGraph

This repository is an implementation of DynaGraph: Dynamic Contrastive Graph for Interpretable Multi-label Prediction using Time-Series EHR Data. 

<p align="center">
<img src="DynaGraph2.png" width="700">
</p>

## Requirements

To install requirements:

```setup
pip install -r requirements.txt
```
## Training

To train the model(s) in the paper, run the notebook in the Train.ipynb file. You can adjust number of layers, graphs, slices in the model definition. The learning rate and parameters can be adjusted accordingly in the function calls.

## Evaluation

To evaluate the model and retrieve the results for a particular seed, run the Evaluate.ipynb notebook.

The dataset samples are located in the Data folder and are loaded in the notebook accordingly. The ones for MIMIC-III are labeled with an 'X' in the title. The numbers at the end correspond to the respective seeds under which the data splits were generated.

The pre-trained models for the benchmarks as well as for DynaGraph under models. Due to the size limitations, we only include one of the seed runs, but can provide more if requested.

## Results

Our model achieves the following performance on eICU:

| Model name         | Balanced Accuracy  |   Sensitivity  |
| ------------------ |----------------    | -------------- |
| LSTM               |       59.67%       |     36.85%     |
| Transformer        |       57.75%       |     25.51%     |
| GAT                |       63.48%       |     34.22%     |
| GCN                |       55.64%       |     26.78%     |
| GIN                |       68.37%       |     70.65%     |
| DynaGraph          |       73.52%       |     86.00%     |
