
# Protein Classification

## Overview
This project addresses the problem of **protein classification** using supervised machine learning techniques.  
The objective is to predict the **classification of proteins** based on their structural, physical, and chemical features.  
The study explores multiple models and compares their performance in terms of **accuracy** and **F1-score**.

---

## Dataset
- **Source**: [shahir/protein-data-set](https://www.kaggle.com/datasets/shahir/protein-data-set)  
- **Goal**: predict the `classification` attribute of proteins.  
- **Features used**:
  - *Categorical*:  
    - `macromoleculeType`  
    - `experimentalTechnique`  
    - `crystallizationMethod`
  - *Numerical*:  
    - `resolution`  
    - `structureMolecularWeight`  
    - `densityPercentSol`  
    - `phValue`
  - *Sequential*:  
    - `sequence` (encoded as integer indices with padding/truncation up to length 200)

---

## Preprocessing
1. **Categorical encoding**:  
   Each categorical attribute was transformed using `LabelEncoder`.  
2. **Numerical scaling**:  
   Numerical attributes were standardized with `StandardScaler`.  
3. **Sequence handling**:  
   Protein sequences were mapped to integer indices using a character-level dictionary.  
   All sequences were truncated or padded to a maximum length of 200.  
4. **Target encoding**:  
   The `classification` column was encoded with `LabelEncoder`.  
5. **Data split**:  
   Stratified train-test split with 80% training and 20% testing.

---

## Models
Three models were implemented and compared:
- **Logistic Regression**  
  Baseline linear model for multi-class classification.  
- **Random Forest**  
  Ensemble of decision trees with bagging and random feature selection.  
- **Neural Network**  
  A feed-forward architecture with embeddings for the sequence data and dense layers for classification.

---



