# PHEME Rumour Propagation and Graph Learning

## Overview

This repository provides research notebooks and supporting experimental results for the manuscript **“Structural Patterns of Rumour Propagation and Hybrid Graph Learning in Multi-Event Social Networks”**, prepared for *Applied Network Science*.

The study investigates rumour propagation structures and graph-based classification using the PHEME dataset.

## Dataset

The experiments use four PHEME events:

- Charlie Hebdo
- Ferguson
- Germanwings
- Sydney Siege

A total of 4,072 cascades were retained for structural analysis after applying the minimum cascade-size criterion of five nodes.

The original PHEME dataset is available at:

https://figshare.com/articles/dataset/PHEME_dataset_of_rumours_and_non-rumours/4010619

The dataset is not redistributed through this repository.

## Research Notebooks

**Applied Network Science-final.ipynb**

Contains code associated with PHEME data preparation, cascade reconstruction, and structural analysis.

**PHEME_Final_Revision_Strict_LOEO.ipynb**

Contains code associated with graph neural network experiments and strict Leave-One-Event-Out (LOEO) evaluation, including GCN, GAT, GraphSAGE, hybrid graph models, and comparison experiments involving TF-IDF, frozen BERT representations, and an adapted Bi-GCN implementation.

## Experimental Protocol

The study evaluates cross-event generalization using strict LOEO evaluation, where one event is held out for testing and the remaining events are used for training.

The experiment manifest records random seed 42. TF-IDF representations use 5,000 features and are fitted using training events only within each LOEO fold.

## Supporting Results

The repository includes:

- `FINAL_EXPERIMENT_MANIFEST.json`
- `final_structural_metrics_4072_CORRECTED.csv`
- `TableIII_MannWhitney_FINAL_4072.csv`
- `Table_BERT_vs_TFIDF_macro_f1_difference.csv`
- `Table_eventwise_macro_f1_TFIDF_BERT_BiGCN.csv`
- `Table_mean_metrics_TFIDF_BERT_BiGCN.csv`

These files provide the final structural metrics, statistical analysis results, model-comparison summaries, and experimental configuration details.

## Execution Environment and Limitations

The research was developed using Jupyter Notebook and Google Colab.

The Colab notebook uses Google Drive paths such as `/content/drive/MyDrive/PHEME`. Researchers must adapt these paths to their own environment and obtain the PHEME dataset separately.

The notebooks retain portions of the original experimental development history, including some superseded cells, unsuccessful intermediate executions, and incomplete displayed outputs. The repository is therefore provided as research source code and supporting results rather than as a fully verified, one-click executable pipeline.

Large intermediate caches, pretrained model weights, and some environment-specific artifacts are not included.

## Reproducibility

The repository documents the research implementation and provides the final exported tables and experiment manifest. Reproducing the experiments requires preparing the PHEME data, installing the appropriate Python and machine-learning dependencies, configuring local paths, and identifying the final experiment cells.

The supplied results should not be interpreted as evidence that the complete notebooks have been independently rerun from a clean environment.

## Code Availability

The research notebooks and supporting experimental results are publicly available in this GitHub repository.
