# Mitotic phase classification from microscopy images

This repository contains a workflow for classifying mitotic phases of nuclei in a microscopy image using image processing, feature extraction and unsupervised learning. It is part of a university module called research software engineering within my master studies computational modeling and simulation.

## Overview

The pipeline includes:

- **segmentation** of nuclei using [stardist](https://github.com/stardist/stardist)
- **image processing** and **feature extraction** (size, shape, intensity) using [skimage](https://github.com/scikit-image/scikit-image)
- **Phase classification** using KMeans clustering
- **Expert annotations** for a subset of nuclei to provide ground-truth labels
- **Quality assurance** using UMAP, classification metrics, and visual inspection

## Goal

Automatically assign a mitotic phase (prophase, metaphase, anaphase, or telophase) to each nucleus in the image and evaluate the clustering accuracy using expert annotations.

## Technologies used

- [`stardist`](https://github.com/stardist/stardist) for deep-learning-based segmentation
- [`skimage`](https://github.com/scikit-image/scikit-image) for preprocessing and feature extraction
- [`pandas`](https://github.com/pandas-dev/pandas) and [`numpy`](https://github.com/numpy/numpy) for data handling
- [`sklearn`](https://github.com/scikit-learn/scikit-learn) (`KMeans`, `classification_report`) for clustering and validation
- [`umap`](https://github.com/lmcinnes/umap) for dimensionality reduction
- [`seaborn`](https://github.com/mwaskom/seaborn), [`matplotlib`](https://github.com/matplotlib/matplotlib), [`stackview`](https://github.com/haesleinhuepf/stackview) for data visualization

## Contents

- `notebooks/RSE_assignment.ipynb`: Main notebook with the complete analysis pipeline
- `data/`: Folder for annotation TIFF image
- `README.md`: This file
- `LICENSE-CC-BY`: License of this repository (CC-BY 4.0 International License)
- `requirements.txt`: includes all necessary libraries used within the analysis pipeline

## Status

This project serves as a prototype for evaluating unsupervised classification of mitotic phases. 
