
![DALI logo](./dali.png)

This repository contains all the necessary material to perform feature learning with deep autoencoders in an unsupervised manner. Specifically, we focus on the task of sortign apoptotic from non-apoptotic cells. Each cell corresponds to a two-channel image (Brightfield/Fluorescence) acquired with Image Flow Cytometry.

**Standalone executable**:

A Standalone executable graphical user interface (only for Microsoft Windows) is available by [clicking this link](https://hmgubox.helmholtz-muenchen.de/f/1b59ca53ec1c4d159734/?dl=1).
Download, double-click and follow the onscreen instructions (might take some time to load). Will ask for a trained autoencoder file (provided in ./data/cae_M1.hdf5). Will also ask for a trained random forest (provided in ./sorting_results/test_experimenttrained_classifer.pkl).

The table of contents is as follows:

Jupyter notebooks:
- load_experiment.ipynb: Demonstrates how to load an experiment exported with the IDEAS software into Python and save it as an .hdf5 file.
- train_CAE.ipynb: Demonstrates how to train a deep Convolutional AutoEncoder (CAE).
- sort_experiment.ipynb: Demonstrates how to train a Random Forest classifier to sort cells into their respective categories (apoptotic/non-apoptotic) using the CAE features.

Directories:
- ./data: Includes the necessary image data, as well as the trained CAE model.
- ./sorting_results: Includes all the metadata generated from the cell-sorting process (e.g. predicted cell-categories).
- ./decafx: includes helper code, such as the architecture of the CAE, and data loading helper functions.
