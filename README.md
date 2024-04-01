# Blood-Brain Barrier Penetration Prediction

## Project Overview

This project focuses on predicting the likelihood of compounds penetrating the blood-brain barrier (BBB) through an analysis of various chemical descriptors. Leveraging a dataset of compounds categorized by their BBB penetration status (`p` for penetrating, `n` for non-penetrating) alongside melatonin receptor ligands sourced from ChEMBL, molecular descriptors such as molecular weight (MW), partition coefficient (LogP), topological polar surface area (tPSA), number of hydrogen bond acceptors (HBA), and donors (HBD) are calculated using RDKit.

## Dataset

The dataset consists of compounds with known BBB penetration statuses and melatonin receptor ligands. Molecular descriptors are computed to facilitate analysis and modeling.

## Methodology

- **Data Preparation**: Initial steps include cleaning and preprocessing the data, where necessary molecular descriptors are calculated and salts are removed with the help of RDKit.
- **Exploratory Data Analysis (EDA)**: The chemical space of the dataset is explored through clustering and principal component analysis (PCA) to visualize the distribution of compounds in relation to their BBB penetration capability.
- **Model Building**: The dataset is divided into training and testing sets. Features are standardized, and a RandomForestClassifier is employed to predict BBB penetration. Evaluation metrics include accuracy, precision, recall, and AUC-PR.
- **Prediction and Validation**: BBB penetrance for a new set of compounds is predicted using the trained model. This set includes melatonin receptor ligands and selected compounds from the ZINC chemical library.

## Results

The developed model demonstrates a high degree of accuracy in predicting BBB penetration, underscoring the potential of machine learning in pharmaceutical research. Despite the challenges in distinguishing between BBB-penetrating and non-penetrating compounds, t-SNE visualization reveals distinct clusters within the chemical space.

## Installation

The project requires Python 3.x along with several libraries such as pandas, RDKit, scikit-learn, matplotlib, seaborn, and Jupyter Notebook/Lab.

```bash
pip install pandas rdkit scikit-learn matplotlib seaborn notebook
