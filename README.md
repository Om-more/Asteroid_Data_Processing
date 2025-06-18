# Asteroid_Data_Processing

## Asteroid Data Processing using PySpark (ETL + ML)
This project is an end-to-end data processing and machine learning pipeline built using Apache Spark (PySpark). The dataset contains asteroid-related information (e.g., orbital parameters, hazardous status), and the pipeline performs cleaning, transformation, exploratory analysis, regression, and classification.
Note: While this project reflects solid data engineering and machine learning practices, it is not fully production-ready. Further modularization, optimization, and deployment packaging would be necessary for real-world applications.

Link for datasets: https://drive.google.com/drive/folders/1n8-TUJYZemdQN5LdeAW7NgR7-c-9hGT2?usp=sharing
________________________________________
 ### Components
1. Data Loading and ETL
•	Load raw CSV data using Spark
•	Drop rows with missing values
•	Type conversion and feature selection
•	Feature engineering: extraction of meaningful fields
•	Outlier removal using IQR method
•	Export cleaned dataset to CSV
2. Exploratory Data Analysis (EDA)
•	Visual analysis using matplotlib/seaborn (after converting to Pandas)
•	Scatter plots between orbital features and target variables (e.g., MOID, NEO status)
3. Machine Learning Pipeline
A. Regression Task
•	Goal: Predict Minimum Orbit Intersection Distance (MOID)
•	Features Used: Diameter, H (magnitude), q (perihelion distance), semi-major axis, eccentricity, etc.
•	Models:
o	Random Forest Regressor
o	Gradient Boosted Tree Regressor
•	Metrics: RMSE, R-squared
B. Classification Task
•	Goal: Predict if an asteroid is a Near-Earth Object (NEO)
•	Target: Binary label (Y = NEO, N = not NEO)
•	Models:
o	Random Forest Classifier
o	Gradient Boosted Tree Classifier
•	Metrics: Accuracy, F1 Score
4. Modeling Tools and Techniques
•	VectorAssembler for combining features
•	MinMaxScaler for normalization
•	Pipeline to structure the ML workflow
•	MulticlassClassificationEvaluator and RegressionEvaluator for evaluation
5. Export and Final Output
•	Cleaned and transformed dataset is saved as CSV for downstream use
________________________________________
Feel free to reach out or fork this repository if you’d like to build upon or contribute!
