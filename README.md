# Breast Cancer Classification Project

## Overview
A machine learning classification system to predict breast cancer diagnosis using cell nucleus measurements from the Wisconsin Breast Cancer Dataset. This project demonstrates the complete data science workflow from statistical analysis through model evaluation, achieving 93.86% accuracy with 90% sensitivity for malignant cases.

## Key Results
- **Best Model**: Logistic Regression
- **Accuracy**: 93.86%
- **AUC Score**: 98.61%
- **Clinical Performance**: 90% cancer detection rate (missed only 4 out of 42 malignant cases)
- **False Positive Rate**: 4.2% (3 out of 72 benign cases)

## Dataset
- **Source**: Wisconsin Breast Cancer Dataset
- **Samples**: 569 patients
- **Features**: 30 numerical measurements of cell nuclei
- **Target**: Binary classification (Malignant/Benign)
- **Class Distribution**: 357 benign (62.7%), 212 malignant (37.3%)

## Methodology

### 1. Exploratory Data Analysis
- Statistical analysis using independent t-tests
- Feature correlation analysis
- Outlier detection and analysis
- Data visualization with histograms and box plots

### 2. Feature Selection
Selected 5 most significant features based on statistical testing (p < 0.000001):
- `concave_points_mean` - Number of concave portions of contour
- `radius_mean` - Mean of distances from center to perimeter
- `texture_mean` - Standard deviation of gray-scale values
- `compactness_mean` - Perimeter² / area - 1.0
- `concavity_mean` - Severity of concave portions

### 3. Model Development
- **Data Split**: 80% training, 20% testing with stratification
- **Preprocessing**: StandardScaler normalization for scale-sensitive algorithms
- **Models Tested**: 
  - Logistic Regression
  - Random Forest
  - Support Vector Machine (planned)

### 4. Model Evaluation
- Accuracy, Precision, Recall, F1-score
- ROC curves and AUC analysis
- Confusion matrices with clinical interpretation
- Feature importance analysis

## Clinical Insights

### Feature Importance Rankings
1. **Concave Points** (strongest predictor) - Irregular tumor borders
2. **Radius** - Tumor size correlation
3. **Texture** - Surface roughness indication
4. **Concavity** - Shape irregularity measure
5. **Compactness** - Geometric properties

### Medical Validation
Results align with established medical knowledge:
- Irregular, indented borders (concave points) are classic cancer indicators
- Larger tumor size correlates with malignancy
- Surface texture provides additional diagnostic information

## Technologies Used
- **Python**: pandas, numpy, scikit-learn
- **Visualization**: matplotlib, seaborn
- **Statistical Analysis**: scipy
- **Environment**: Google Colab
- **Version Control**: Git, GitHub

## Project Structure
breast-cancer-classification/
├── README.md
├── notebooks/
│   └── breast_cancer_analysis.ipynb
├── data/
│   └── data_breast_cancer.csv
└── requirements.txt

## Model Performance Comparison

| Model | Accuracy | AUC Score | Malignant Recall | False Negatives |
|-------|----------|-----------|------------------|-----------------|
| Logistic Regression | 93.86% | 98.61% | 90% | 4 |
| Random Forest | 93.86% | 98.14% | 88% | 5 |

## Clinical Impact
- **High Sensitivity**: 90% detection rate for malignant cases
- **Low False Alarm Rate**: Only 4.2% false positives
- **Potential Application**: Decision support tool for radiologists
- **Ethical Consideration**: 10% miss rate requires human oversight

## Future Enhancements
- Cross-validation for more robust evaluation
- Ensemble methods combining multiple models
- Feature engineering from additional measurements
- Deployment considerations for clinical settings

## Installation & Usage

### Requirements
pandas==1.5.3
numpy==1.24.3
scikit-learn==1.3.0
matplotlib==3.7.1
seaborn==0.12.2
scipy==1.10.1

### Running the Analysis
1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Open `notebooks/breast_cancer_analysis.ipynb` in Jupyter/Colab
4. Run all cells to reproduce the analysis

## Contact
For questions about this project, please open an issue or contact [syed.sajjadali114@gmail.com/https://www.linkedin.com/in/sajjadali114/].

---
*This project is for educational and portfolio purposes. It should not be used for actual medical diagnosis without proper clinical validation and regulatory*
