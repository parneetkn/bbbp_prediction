# Blood-Brain Barrier Permeability Prediction  

## 📌 Overview  
This repository demonstrates the prediction of **Blood-Brain Barrier (BBB) permeability** using a **Random Forest model**. The model is trained on molecular descriptor data derived from **SMILES** representations of compounds. The dataset was sourced from the following research article:  

🔗 **Dataset Source**: [MDPI - Blood-Brain Barrier Permeability Study](https://www.mdpi.com/1420-3049/26/24/7428)  

## 📊 Dataset Information  
The dataset consists of molecular structures in **SMILES format** along with permeability labels (0 or 1), which were converted into **RDKit descriptors** for machine learning analysis. These descriptors capture key chemical properties of the molecules, aiding in BBB permeability classification.  

## ⚙️ Methodology  
1. **Data Preprocessing**  
   - Molecular descriptors were extracted using **RDKit**.
   - Checking for na values and removing the columns which have all the values as zero
   - Min-Max Scaling was applied for normalization.  
2. **Model Training (Random Forest)**  
   - A **Random Forest classifier** was trained to predict BBB permeability.  
   - Model performance was evaluated using **accuracy, precision, recall, F1-score, and ROC-AUC**.  
3. **Feature Importance Analysis**  
   - Feature importance was analyzed using:  
     - **Random Forest feature importances**  
     - **SelectKBest (ANOVA F-score)**  

## 📈 Results & Visualization  
- **Feature Importance Plots**:  
  - Top 10 important features were visualized from **Random Forest** and **SelectKBest**.  
- **Performance Metrics**:  
  - Confusion Matrix, Accuracy, Precision, Recall, F1-Score, and ROC-AUC Score were calculated.  

## 🛠️ Dependencies  
Ensure you have the following Python libraries installed:  
```bash
pip install pandas numpy rdkit scikit-learn matplotlib seaborn
