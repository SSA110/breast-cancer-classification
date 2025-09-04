# Dataset Information

## Wisconsin Breast Cancer Dataset

This folder contains the breast cancer dataset used in the classification project.

### File Description
- `data_breast_cancer.csv` - The complete dataset with 569 patient records

### Dataset Details
- **Source**: Wisconsin Breast Cancer Dataset (UCI Machine Learning Repository)
- **Samples**: 569 patients
- **Features**: 30 numerical measurements + diagnosis
- **Target**: Binary classification (M = Malignant, B = Benign)
- **Class Distribution**: 357 benign (62.7%), 212 malignant (37.3%)

### Feature Categories
- **Mean values** (`_mean`): Average measurements
- **Standard error** (`_se`): Variability in measurements
- **Worst values** (`_worst`): Largest/most severe measurements

### Key Features Used in Analysis
1. `concave_points_mean` - Number of concave portions of contour
2. `radius_mean` - Mean distances from center to perimeter
3. `texture_mean` - Standard deviation of gray-scale values
4. `compactness_mean` - Perimeter² / area - 1.0
5. `concavity_mean` - Severity of concave portions

### Data Quality
- No missing values
- Clean numerical data
- Ready for machine learning analysis

### Citation
If using this dataset, please cite the source from the UCI Machine Learning Repository.
  
