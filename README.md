# Predicting Breast Cancer


## CONTENTS:

1. Breast Cancer Overview
2. Problem Statement
3. Data Overview
4. Data Preprocessing
5. Exploratory Analysis
6. Feature Selection
7. Model Selection
8. Conclusion


## BREAST CANCER OVERVIEW

Breast cancer is cancer that forms in the cells of the breasts

Breast cancer is the most common invasive cancer in women and the second leading cause of cancer death in women after lung cancer. Men can also be diagnosed with breast cancer but it is very rare.

![Alt Text](https://www.cancer.org/content/dam/cancer-org/images/illustrations/medical-illustrations/en/breast-cancer-images/normal-breast-tissue.gif/jcr:content/renditions/cq5dam.thumbnail.980.980.jpeg)

Source: https://www.cancer.org/cancer/breast-cancer/about/what-is-breast-cancer.html

According to the American Cancer Society (ACS), there are more than 3.1 million breast cancer survivors in the United States. The chance of any woman dying from breast cancer is around 1 in 38 (2.6%).

### Symptoms

1. A painless lump or thickening in your breast tissue
2. Pain in the armpits or breast that does not change with the monthly cycle
3. Pitting or redness of the skin of the breast, similar to the surface of an orange
4. A rash around or on one of the nipples
5. Discharge from a nipple, possibly containing blood
6. A sunken or inverted nipple
7. A change in the size or shape of the breast
8. Peeling, flaking, or scaling of the skin on the breast or nipple

### Risk Factors

The risk factors for breast cancer are due to a combination of factors that are not in our control and some that are in our control. 

There is a possibility of someone getting breast cancer without possesing any known risk factor (source: https://www.cdc.gov/cancer/breast/basic_info/risk_factors.htm)

1. Age
2. Genetics
3. A history of breast cancer or breast lumps
4. Dense breast tissue
5. Estrogen exposure and breastfeeding
6. Body weight
7. Alcohol consumption
8. 8. Radiation exposure
9. Hormone treatments

It’s important to understand that most breast lumps are benign and not cancer (malignant). Non-cancerous breast tumors are abnormal growths, but they do not spread outside of the breast. They are not life threatening, but some types of benign breast lumps can increase a woman's risk of getting breast cancer. Any breast lump or change needs to be checked by a health care professional to determine if it is benign or malignant (cancer) and if it might affect your future cancer risk. (:https://www.cancer.org/cancer/breast-cancer/about/what-is-breast-cancer.html)


## PROBLEM STATEMENT

Breast cancer is a leading form of cancer in women and although rare, affects men too. Early detection and accurately distinguishing between benign and malignant tumours increases a patient's chances of sruvival. Awareness, funding and technology have advanced the detection and treatment of breast cancer. This project aims to accurately predict whether a breast tumour is malignant or benign using machine learning classification algorithms.

##DATA OVERVIEW

### Data Set Information:

1. Title: Wisconsin Diagnostic Breast Cancer (WDBC)

2. Source: 
    The Dataset was made available by UCI Machine Learning Repository (https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/)
    For this project, a formatted copy of the Data was gotten from Kaggle Datasets (https://www.kaggle.com/uciml/breast-cancer-wisconsin-data)

5. Number of instances (Rows): 569 

6. Number of attributes (Columns): 32 (ID, diagnosis, 30 real-valued input features)

7. Attribute information

1) ID number
2) Diagnosis (M = malignant, B = benign)
3-32)

Ten real-valued features are computed for each cell nucleus:

	a) radius (mean of distances from center to points on the perimeter)
	b) texture (standard deviation of gray-scale values)
	c) perimeter
	d) area
	e) smoothness (local variation in radius lengths)
	f) compactness (perimeter^2 / area - 1.0)
	g) concavity (severity of concave portions of the contour)
	h) concave points (number of concave portions of the contour)
	i) symmetry 
	j) fractal dimension ("coastline approximation" - 1)

The mean, standard error, and "worst" or largest (mean of the three
largest values) of these features were computed for each image,
resulting in 30 features.  For instance, field 3 is Mean Radius, field
13 is Radius SE, field 23 is Worst Radius.

All feature values are recoded with four significant digits.

8. Missing attribute values: none

9. Class distribution: 357 benign, 212 malignant

### DATA PREPROCESSING

1. The data was read into a Pandas Dataframe
2. The number of rows and columns was checked:
	There were 569 rows and 33 columns
3. A check for missing values was done:
	The dataset contained a column called 'Unnamed: 32' with 100% missing values, this column was
	dropped.
	All other columns in the dataset had no missing value.
4. The data type of the columns was checked:
	The columns had appropriate data types, the feature columns were float64, id column int64 and
	dianosis an object datatype.
5. The distribution of tumor classes was checked:
	357 B(benign) and 212 M(malignant)
6. The 'ID' column was dropped
	
The data was mostly clean with all the data having the right data type and just one column 'Unnamed: 32' with missing values which was dropped.

## Exploratory Analysis
