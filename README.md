# Facies Classification Using Machine Learning

## Project Overview
This project implements various machine learning techniques to classify rock facies using well log data. The classification is performed on data from the Council Grove gas reservoir in Southwest Kansas, one of North America's largest gas-producing areas.

## Dataset
The dataset includes well log data from 10 wells with the following features:
- **Wireline Log Measurements:**
  - Gamma Ray (natural radioactivity measurement)
  - Resistivity (ILD - Induction log)
  - Photoelectric Effect
  - Neutron-density porosity difference
  - Average neutron-density porosity
- **Geologic Constraining Variables:**
  - Nonmarine/marine indicator
  - Relative position (depth)

## Facies Classes
The model classifies rocks into nine distinct facies types that can blend into neighboring facies:
1. Nonmarine sandstone
2. Nonmarine coarse siltstone
3. Nonmarine fine siltstone
4. Marine siltstone and shale
5. Mudstone
6. Wackestone
7. Dolomite
8. Packstone-grainstone
9. Phylloid-algal bafflestone

## Implemented Models
The project implements and compares several machine learning classifiers:
- Support Vector Machine (SVM)
- Gaussian Process Classifier
- Random Forest Classifier
- Neural Network Classifier
- K-Nearest Neighbors
- Decision Tree Classifier
- Logistic Regression

## Evaluation Metrics
Performance is measured using:
- Jaccard Index
- Precision
- Recall
- F1 Score
- Adjacent Accuracy (custom metric for neighboring facies)

## Key Findings
- SVM, Neural Network, and K-Nearest Neighbors showed the best performance
- Adjacent accuracy is significantly higher than standard accuracy, confirming facies blending
- Performance correlates with sample frequency - facies with more samples showed better prediction
- Neural Network classifier performed best on blind test data (Nolan well)

## Future Improvements
1. Increase training data samples
2. Further optimize model parameters
3. Incorporate geological constraints using a priori information about rock formation

## Usage
The main implementation is in `facies_classification.ipynb` Jupyter notebook. The notebook includes:
- Data preprocessing and visualization
- Model training and evaluation
- Cross-plots and correlation analysis
- Blind testing on the Nolan well
- Visualization of results

## Dependencies
- Python
- Pandas
- Scikit-learn
- Seaborn
- NumPy
- Jupyter Notebook

## Data Source
The dataset uses publicly available well log data from the Council Grove gas reservoir in Southwest Kansas.
