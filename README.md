
# Hi, I'm Narapureddy Durga Prasad Reddy! 👋

This project is a machine learning-based breast cancer prediction model developed using Logistic Regression (LR). The model was selected after rigorous comparison with multiple algorithms due to its superior accuracy. The project is implemented as a Flask application and deployed on the Render platform, allowing users to access the application via a web interface.
# BreastPredict: Early Breast Cancer Risk Assessment

Breast cancer is the most common type of cancer among women globally and ranks second in mortality rates. Early and accurate detection is vital to improving survival rates and reducing treatment costs. This project leverages machine learning techniques to develop an automated system for diagnosing breast cancer based on clinical data. By providing an accessible and accurate diagnostic tool, this project aims to aid healthcare professionals and contribute to the fight against breast cancer.

## About the Dataset


The dataset used in this project is the Breast Cancer Wisconsin (Diagnostic) dataset, obtained from the University of Wisconsin Hospitals, Madison. It was compiled by Dr. William H. Wolberg and contains a comprehensive set of patient demographics, clinical details, and histopathological information. Diagnosis in the dataset includes identification of malignant or benign tumors based on clinical examinations and imaging results.

The Breast Cancer Prediction dataset contains medical and demographic information of 570 patients. 

The Breast Cancer Wisconsin (Diagnostic) dataset includes the following features derived from clinical and histopathological analyses:

**Features**

**ID:** Unique identifier for each record.

**Diagnosis:** Indicates whether the tumor is malignant (M) or benign (B).

**Mean, Standard Error, and Worst (Maximum) Values for Each Feature:**

For each cell nucleus, the dataset provides three measurements: mean value, standard error, and the "worst" (maximum) value. These are calculated for ten characteristics:

**1. Radius:**

Mean of distances from the center to points on the perimeter.

Features: radius_mean, radius_se, radius_worst.

**2. Texture:**

Standard deviation of gray-scale values.

Features: texture_mean, texture_se, texture_worst.

**3. Perimeter:**

Perimeter of the nucleus.

Features: perimeter_mean, perimeter_se, perimeter_worst.

**4. Area:**

Area of the cell nucleus.

Features: area_mean, area_se, area_worst.

**5. Smoothness:**

Local variation in radius lengths.

Features: smoothness_mean, smoothness_se, smoothness_worst.

**6. Compactness:**

Perimeter² / Area - 1.0.

Features: compactness_mean, compactness_se, compactness_worst.

**7. Concavity:**

Severity of concave portions of the contour.

Features: concavity_mean, concavity_se, concavity_worst.

**8. Concave Points:**

Number of concave portions of the contour.

Features: concave_points_mean, concave_points_se, concave_points_worst.

**9. Symmetry:**

Symmetry of the nucleus.

Features: symmetry_mean, symmetry_se, symmetry_worst.

**10. Fractal Dimension:**

“Coastline approximation” - 1.

Features: fractal_dimension_mean, fractal_dimension_se, fractal_dimension_worst.

### Total Features:
30 numerical features (10 characteristics × 3 measurements).

1 target variable (diagnosis).

31 Columns in Total.



The dataset also includes the Breast Cancer status of each patient (Malignant or Benign), making it well-suited for classification tasks. Specifically:

Malignant Instances: 212

Benign Instances: 357

For more details, the dataset can be accessed https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

# Project Workflow

## Preprocessing

* Cleaned the dataset to remove irrelevant or redundant data.

* Standardized features to ensure consistency in scale.

## Model Training and Evaluation:

* Compared various algorithms including Neural Networks (NN), Support Vector Machines (SVM), Decision Trees (DT), Random Forests (RF), and K-Nearest Neighbors (KNN).

* Logistic Regression (LR) was selected for its accuracy and performance metrics.

* Evaluation metrics:

    * Accuracy: 0.9912

    * Log Loss: 0.3161
# Key Findings

Logistic Regression outperformed other models:

* Accuracy: 99.12%

* Log Loss: 0.3161

* Other models like NN, SVM, DT, RF, and KNN exhibited lower accuracy and higher losses.
## Deployment

The Logistic Regression model was deployed using Flask and hosted on the Render platform, making it accessible as a web application.

To access the website, use the link https://breastpredict.onrender.com


## 🛠 Skills

* Programming Language: Python

* Framework: Flask

* Libraries: Scikit-learn, NumPy, Joblib

* Deployment Platform: Render




## API Reference

#### Endpoint
* URL: /predict 
* Request Type: POST

```http
  Parameters
```

| Parameter              | Type     | Description                |
| :--------              | :------- | :------------------------- |
|mean_radius	|float	|Mean distance from center to points on the perimeter
mean_texture	|float	|Mean standard deviation of gray-scale values
mean_perimeter	|float	|Mean size of the perimeter
mean_area	|float	|Mean size of the cell area
mean_smoothness|	float	|Mean local variation in radius lengths
mean_compactness|	float	|Mean perimeter² / area - 1.0
mean_concavity|	float	|Mean severity of concave portions of the contour
mean_concave_points	|float	|Mean number of concave portions of the contour
mean_symmetry	|float|	Mean symmetry of the nucleus
mean_fractal_dimension|	float|	Mean coastline approximation - 1
radius_error	|float	|Standard error of the radius
texture_error	|float|	Standard error of the texture
perimeter_error|	float|	Standard error of the perimeter
area_error	|float|	Standard error of the area
smoothness_error|	float	|Standard error of the smoothness
compactness_error	|float	|Standard error of the compactness
concavity_error	|float	|Standard error of the concavity
concave_points_error	|float|	Standard error of the concave points
symmetry_error	|float	|Standard error of the symmetry
fractal_dimension_error|	float|	Standard error of the fractal dimension
worst_radius	|float	|Worst (largest) value for radius
worst_texture	|float	|Worst (largest) value for texture
worst_perimeter|	float	|Worst (largest) value for perimeter
worst_area|	float	|Worst (largest) value for area
worst_smoothness	|float	|Worst (largest) value for smoothness
worst_compactness	|float	|Worst (largest) value for compactness
worst_concavity	|float	|Worst (largest) value for concavity
worst_concave_points	|float	|Worst (largest) value for concave points
worst_symmetry	|float	|Worst (largest) value for symmetry
worst_fractal_dimension	|float|	Worst (largest) value for fractal dimension


```http
  Response
```

| Field     | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| prediction|	string|	Risk classification (Malignant or Benign)|



## Usage/Examples

    1. Navigate to the application homepage.

    2. Enter the clinical feature values in the provided form.

    3. Submit the form to receive the prediction.

    Example:

    * Input: Feature values from a patient’s clinical data.

    * Output: "The tumor is Malignant" or "The tumor is Benign."


## Conclusion

This project demonstrates the potential of machine learning in healthcare diagnostics. By deploying the model as a web application, it bridges the gap between advanced analytics and end-user accessibility. The high accuracy of Logistic Regression makes this solution reliable for early detection of breast cancer.


## Feedback

I welcome feedback to improve the application and expand its functionality. Please contact me via the project repository or please reach out to me at narapureddydurgaprasad818@gmail.com


## Acknowledgements

We extend our gratitude to the University of Wisconsin Hospitals, Madison, for providing the dataset, and to the developers and maintainers of the Flask and Scikit-learn libraries.


