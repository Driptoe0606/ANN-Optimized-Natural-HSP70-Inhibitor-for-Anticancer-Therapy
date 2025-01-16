# ANN-Optimized Natural HSP70 Inhibitors for Anticancer Therapy

This repository contains the implementation of an artificial neural network (ANN) model designed to identify and optimize natural compounds targeting the HSP70 family of heat shock proteins. The aim of this project was to contribute to anticancer therapy by leveraging computational techniques to discover effective inhibitors. Below, you will find an overview of the project, methodology, and usage instructions.

![image alt](https://github.com/Driptoe0606/ANN-Optimized-Natural-HSP70-Inhibitor-for-Anticancer-Therapy/blob/master/058-1.png?raw=true)
## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Methodology](#methodology)
- [Data Sources](#data-sources)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Future Work](#future-work)
- [License](#license)

## Introduction
Heat shock proteins (HSP70 family) play a critical role in cancer cell survival and resistance to therapy. This project focuses on identifying natural compound inhibitors of HSP70 using an ANN trained on curated datasets, molecular descriptors, and similarity searches. The model was optimized to predict potential inhibitors with improved binding affinity and drug-like properties.

## Features
- Natural compound screening from multiple databases.
- Molecular similarity searches using Apoptozole as a reference.
- Integration with the NPASS database for activity predictions.
- ANN model for IC50 prediction and inhibitor optimization.
- Structural refinement of lead compounds using machine learning.

## Methodology
1. **Data Curation:**
   - Collected data from SANCDB and other natural product databases.
   - Filtered for entries with relevant activity against HSP70.
   - Used molecular docking and IC50 predictions to refine initial hits.

2. **Similarity Search:**
   - Performed a similarity search using Apoptozole as a benchmark inhibitor.
   - Identified structurally similar compounds with drug-like properties.

3. **ANN Development:**
   - Extracted molecular descriptors for dataset entries.
   - Trained an ANN using TensorFlow and optimized for accuracy and generalizability.

4. **Validation and Optimization:**
   - Evaluated IC50 predictions for lead compounds.
   - Improved model performance using additional training data and hyperparameter tuning.

## Data Sources
- **SANDCDB Database(South African Natural Compound Data Base):** Primary database for natural compounds.
- **Other Natural Compound Repositories:** Supplementary datasets used for diversity.
- **Apoptozole:** Reference compound for similarity-based screening.

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ANN-HSP70-Inhibitors.git
   cd ANN-HSP70-Inhibitors
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure your environment includes Python 3.8+ and TensorFlow 2.x.

## Usage
1. **Data Preparation:**
   - Place the curated datasets in the `data/` directory.
   - Run the preprocessing script to generate molecular descriptors:
     ```bash
     python preprocess_data.py
     ```

2. **Model Training:**
   - Train the ANN model using the following command:
     ```bash
     python train_model.py
     ```

3. **Predict IC50 Values:**
   - Use the trained model to predict IC50 values for new compounds:
     ```bash
     python predict_ic50.py --input new_compounds.csv
     ```

4. **Similarity Search:**
   - Run a similarity search with Apoptozole:
     ```bash
     python similarity_search.py --reference apoptozole.sdf
     ```

## Results
- The ANN achieved high accuracy in predicting IC50 values.
- Identified several promising lead compounds for further experimental validation.
- Highlighted limitations of existing natural product databases, emphasizing the need for larger datasets.

## Future Work
- Expand the model to include additional protein targets beyond HSP70.
- Incorporate experimental validation for top-predicted compounds.
- Develop a more comprehensive natural product database for training.

---

For questions or contributions, feel free to open an issue or submit a pull request. Thank you for your interest in ANN-Optimized Natural HSP70 Inhibitors for Anticancer Therapy!
