## EDA, feature engineerging y pipeline de Machine Learning de Mercado Inmoviliario en COLOMBIA
### EDA, feature engineerging y pipeline de Machine Learning de Mercado Inmoviliario en COLOMBIA

According to the datasets provided by the SOY HENRY bootcamp, which is about the Colombian real estate market:
- 'properties_colombia_train.csv': Contains 197549 records and 26 dimensions, which includes numerical price information.
- 'propiedades_colombia_test.csv': Contains 65850 records and 25 dimensions, which does not include price information.

This project consists of making a predictive model that predicts the price of a real estate between expensive and cheap, the average of the price column (643605091.0064613) was calculated, where "1" was assigned to those that are greater than the average of "price" = expensive and "0" was assigned to those less than the average of "price" = cheap.

## For this, the EDA (Exploratory Data Analysis), feature engineering and Market Machine Learning pipeline was carried out, the following steps were taken into account:

- **1. Analysis of the data from the datasets**

For this stage, various Python libraries and modules were used such as: pandas, numpy, the .head() modules, .info() and among others.
![11](https://user-images.githubusercontent.com/103965538/199861223-864d1ed0-0b40-4cb7-b24f-9fe22d1e51b2.PNG)

- **2. Data visualization**

Here the data was visualized with "matplotlib" which is used to plot graphs in python, the folium and heatmap libraries were imported to perform the geospatial coordinates.
![222](https://user-images.githubusercontent.com/103965538/199860332-9facfb23-ff9c-464e-bb36-18fc418f130a.PNG)

- **3. Data cleaning and normalization**

Here the dataset was cleaned, data normalization was done with the modules .replace(), drop() and among others.

- **4. Data imputation**

We used .fillna(), replace(), mean() to impute the data.

- **5. Elimination of irrelevant columns of input variables first part**

It is important to have a good critical analysis since here, according to the analysis and previous observation in the datasets, as a data engineer I eliminated some irrelevant columns.

- **6. Data transformation with LabelEncoder :) an ease**

Here I imported the preprocessing and LabelEncoder library that helps to transform categorical values ​​to numeric with incredible order. "LabelEncoder": assigns a different number to each categorical variable.

- **7. Feature selection or also called irrelevant column removal part 2**

The "seaborn" library is imported using correlation statistics, it was carried out thanks to the correlation filters to the input variables of the training dataset, that is, which characteristics have a greater correlation with the variable to be predicted.
![333](https://user-images.githubusercontent.com/103965538/199861476-96d001c0-9d95-49f5-a731-351204c38b57.PNG)

- **8. Classification models**

The type of automatic learning is supervised where they already give us the variable to predict, that is, labeled, so for this reason these two classification algorithms Decision Trees and K nearest neighbors were used, which is very suitable for this type of data.

![444](https://user-images.githubusercontent.com/103965538/199860696-3842dc85-e9d0-4c7b-af2c-dabfd034af66.PNG)

- **9. Training**

The classification model and the training dataset (X_train = df_train) are trained.
Here "fit" was used to train the training dataset, in the case of Decision Trees, a tree depth of 6 was used according to the calculation made in the script.

- **10. With the KNN classification algorithm**

![66](https://user-images.githubusercontent.com/103965538/199860980-90199c2a-d440-40cd-b92a-8318fdcd5dea.PNG)

- **11. Assessment of evaluation metrics**

With the decision tree algorithm
![55](https://user-images.githubusercontent.com/103965538/199860907-d74a973e-dcab-45a6-a7d3-7709e6692c99.PNG)

To conclude, in the Evaluation of the metrics, accuracy and recall were taken into account.
It can be seen that the Decision Tree Classification algorithm is the most optimal algorithm to predict if the price of a real estate company is expensive or cheap with this project with data from the Real Estate Market in COLOMBIA.
