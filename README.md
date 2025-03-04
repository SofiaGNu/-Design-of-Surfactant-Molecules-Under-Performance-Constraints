# Design-of-Surfactant-Molecules-Under-Performance-Constraints
This repository contains the data and models necessary to ensure the reproducibility of the results presented in the paper.

The heads and tails are provided as pickle files, available both as bond matrices and in SMILES notation. The final surfactant structures are also shared in SMILES format.
Each property prediction model is stored in two files:
  .joblib – Contains the trained model; and
  .joblibparameters – Lists the molecular descriptors required for model usage.
Additionally, this repository provides a summary of the methods used to develop predictive models that estimate relevant properties based on Mordred molecular descriptors.
-	Synthetic Accessibility Score (SAscore): A multi layer perceptron (MLP) regression model is built with a single hidden layer,100 neurons and the ReLU activation function. A constant learning rate of 0.001 is used in training.  
-	log(CMC): Partial least squares regression (PLS regression) is applied with 7 principal components (PCs). 
-	Surface tension: A PLS regression model is built, using 5 PCs.
-	Krafft point: Lasso regression with 5-fold cross validation is used.
-	log(LC50): Lasso regression with 5-fold cross validation is used.
-	Biodegradability: Lasso regression with 5-fold cross validation is used.

