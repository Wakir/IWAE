## IWAE

This repository contains a code and results for experiments conducted in paper "**Changing Lineup Classifier Ensemble for Drifting Imbalanced Data Streams**".

### Dependecies and setup

This work is done using Python 3.8.18 and stream_learn 0.8.21. Additional dependencies can be found in `requirements.txt` file. To setup the repository you need to simple run a command in existing Python enviroment:

```
pip install -r requirments.txt
```

### Running the Experiments

Running the experiment is done by calling function `src/experiment1.py` or `src/experiment2.py` with the desired input parameters. 

`src/experiment1.py` contains experiment for sudden drift MNIST
`src/experiment2.py` contains experiment for semantic Fashion MNIST

The hiperparameters uses in following experiments are:

* `random_seeds` - The seeds used by the random number generator.
* `chunk_size` - Size of chunks per datastream step.
* 'unlrealing_rate' - number used for balancing unlearning alghoritm
* `noise_precents` - starting Gaussian noise value (for sudden drift scenario).
* `new_noises` - Gaussian noise value after drift (for sudden drift scenario).
* `window_sizes` - length of the window sliding window.
* `semantic_cases_1` - startic semantic case
* `semantic_cases_1` - semantic case after the window
* `metrics` - List of metric functions or single metric function.
* `learning_rate` -Learning rate value for ResNet CNN.

### Results

Achived results are categoriased based on dataset and presented in the following folders:
* `figures` - visualised data on tables and plots.
* `results` - full results saved in MlFlow format.
