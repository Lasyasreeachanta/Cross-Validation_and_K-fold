## Cross-Validation in Practice: Stabilising Model Performance with K-Fold

### Author: Vijaya Lasya Sree Achanta
### Student ID: 24180156

# Project Summary

This project explores how K-Fold cross-validation improves the reliability of machine learning model evaluation. Using the Breast Cancer Wisconsin dataset, the analysis compares traditional single train–test splits with cross-validation to highlight how performance estimates can vary and how CV reduces this uncertainty.

**Objectives**

The main goals of this project are to:

Evaluate the limitations of a single train–test split
Show how model accuracy changes with different random seeds
Apply K-Fold cross-validation for more consistent evaluation
Examine how varying the number of folds (K = 3, 5, 10) affects results
Compare Logistic Regression and Random Forest using a consistent CV framework
Visualise accuracy distributions across folds
## Dataset Details

**Breast Cancer Wisconsin Dataset**

Total samples: 569
Number of features: 30 numerical attributes (e.g., radius, texture, smoothness)
Task: Binary classification
0 → malignant tumour
1 → benign tumour
**Why this dataset?**
Commonly used benchmark in ML studies
Represents a real-world medical classification problem
Sufficient size to demonstrate variability in evaluation methods
Concepts Covered
**1. Single Train–Test Split**
Dataset is divided once into training and testing subsets
Performance depends heavily on the chosen split
Highlights inconsistency in evaluation
**2. K-Fold Cross-Validation**
Data is divided into K equal parts (folds)
Model is trained on K−1 folds and tested on the remaining fold
Process repeats K times so every data point is used for testing once
Produces both average performance and variation (std deviation)
**3. Effect of Different K Values**
Investigates K = 3, 5, and 10
Smaller K → faster computation but less stable estimates
Larger K → more reliable use of data but increased computational cost
**4. Model Comparison Using CV**
Logistic Regression vs Random Forest
Both evaluated using identical folds
Ensures a fair and unbiased comparison
Results visualised using boxplots and scatter overlays
**Setup Instructions**
Clone or download the repository
Install required libraries:
pip install -r requirements.txt
How to Run
Open notebook17.ipynb in Jupyter Notebook or JupyterLab
Execute all cells step by step
**The notebook includes:**
Data loading and preprocessing
Baseline model using a single split
Cross-validation experiments
Visualisations and comparisons
**Required Libraries**
numpy – numerical operations
pandas – data handling
matplotlib – basic plotting
seaborn – advanced visualisations
scikit-learn – ML models and utilities

(Refer to requirements.txt for versions)

## Folder Structure
.
├── notebook17.ipynb      # Main analysis notebook
├── README.md             # Project documentation
└── requirements.txt      # Dependency list
## Main Observations
**Instability of Single Split:**
Accuracy varies noticeably depending on the random split, showing that one evaluation is not enough.
Improved Reliability with CV:
K-Fold cross-validation provides a more dependable estimate by averaging results across multiple folds.
**Impact of K:**
Changing K slightly affects mean accuracy, but can influence variability and computational cost.
Model Performance Comparison:
Cross-validation allows fair comparison, showing how different models behave on the same data partitions.
## Visual Outputs

The notebook generates several plots, including:

Class distribution of the dataset
Accuracy variation across multiple random splits
Fold-wise scores in 5-Fold CV
Mean accuracy vs number of folds
Standard deviation vs number of folds
Boxplots comparing model performance
Approach
Preprocessing: StandardScaler applied for Logistic Regression
Pipeline: Combines scaling and model training
Cross-validation: KFold with shuffling and fixed seed
Metric: Accuracy for classification performance
Visualisation: Matplotlib and Seaborn
Additional Notes
Random seed set to 42 for reproducibility
Stratified sampling used to preserve class proportions
Logistic Regression uses LBFGS solver (max_iter=500)
Random Forest uses 200 trees with default depth
References
Breast Cancer Wisconsin Dataset (scikit-learn)
Scikit-learn documentation
Standard machine learning evaluation practices
## License

This project is submitted as part of an academic assignment for the Machine Learning Neural Networks course.

**Contact Information**

**Vijaya Lasya Sree Achanta**
**Student ID: 24180156**
