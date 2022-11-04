## EDA, feature engineerging y pipeline de Machine Learning de Mercado Inmoviliario en COLOMBIA
Segun a los datasets proporcionados por el bootcamp SOY HENRY, que es acerca del mercado inmoviliario de Colombia:
- 'properties_colombia_train.csv': Contiene 197549 registros y 26 dimensiones, el cual incluye la información numérica del precio.
- 'propiedades_colombia_test.csv': Contiene 65850 registros y 25 dimensiones, el cual no incluye la información del precio.

Este proyecto consiste en realizar un modelo predictivo que prediga el precio de una inmoviliaria entre caro y barato, se calculó el promedio de la columna price (643605091.0064613), donde se asignó "1" a los mayores al promedio de "price" = caro
y se asignó "0" a los menores al promedio de "price" = barato.

## Para esto se hizo el el EDA (Análisis Exploratorio de datos), feature engineerging y pipeline de Machine Learning de MercadoSe para esto se tuvo en cuenta los siguientes pasos:

- 1. Análisis de los datos de los datasets.
Para esta etapa se utilizó diversós librerias y módulos de python como: pandas,  numpy, los módulos de .head(), .info() y entre otros.
![11](https://user-images.githubusercontent.com/103965538/199861223-864d1ed0-0b40-4cb7-b24f-9fe22d1e51b2.PNG)

- 2. Visualización de datos.
Aquí se visualizó los datos con "matplotlib" que sirve para graficar graficos en python, mporté la librería folium y heatmap para realizar las coordenadas geoespaciales.
![222](https://user-images.githubusercontent.com/103965538/199860332-9facfb23-ff9c-464e-bb36-18fc418f130a.PNG)

- 3. Limpieza y normalización de datos
Aquí se limpió el dataset, se hizo normalizacion de datos con los mpodulos de .replace(), drop()  y entre otros.
- 4. Imputación de datos 
Se utilizó .fillna(), replace(), mean().
- 5. Eliminación de columnas irrelevantes de las variables de entrada primera parte
Es importante que se tenga un buen análisis crítico ya que aquí segun al análisis y observación previa en los datasets yo como data engineer se eliminaron algunas columnas irrelevantes.
- 6. Transformación de datos con LabelEncoder :) una facilidad.
Aquí Importé la librería preprocesing y LabelEncoder que ayuda a transformar los valores categóricos a numéricos con un orden increíble. "LabelEncoder": va asignádo con un número diferente a cada varible categórica 
- 7. Selección de características o tambien eliminación de columnas irrelevantes parte 2.
Se importa la librería "seaborn" para graficar y usar estadísticos como la correlación, se realizó gracias a los filtros de correlacion a los atributos, osea que características tienen mayor correlación con la variable a predecir.
![333](https://user-images.githubusercontent.com/103965538/199861476-96d001c0-9d95-49f5-a731-351204c38b57.PNG)

- 8. Modelos de clasificación: El tipo de aprendizaje automático es supervisado donde ya nos dan la variable a predecir osea etiquetadas, entonces por tal razón se usó estos dos algortimos de clasicación Árboles de decisiones y K vecinos más cercanos o cual es muy adecuado para este tipo de datos. 
![444](https://user-images.githubusercontent.com/103965538/199860696-3842dc85-e9d0-4c7b-af2c-dabfd034af66.PNG)

- 9. Entrenamiento: Se entrena el modelo de clasificación y el dataset de entrenamiento (X_train= df_train).
Aquí se uso "fit" para entrenar al dataset de entrenamiento, en caso de Árboles de decisiones se uso una profundidad del arbol de 6 según al cálculo realizado en el script.
- 10. Con el algoritmo de clasificación de KNN
![66](https://user-images.githubusercontent.com/103965538/199860980-90199c2a-d440-40cd-b92a-8318fdcd5dea.PNG)

- 11. Evaluacíon de las métricas de evaluación.
![55](https://user-images.githubusercontent.com/103965538/199860907-d74a973e-dcab-45a6-a7d3-7709e6692c99.PNG)

Para concluir, en la Evaluacion de las métricas se tuvo en cuenta el accuracy y el recall.
Se puede ver que el algoritmo de Clasificación de Árboles de decisiones es el algoritmo mas óptimo para predecir si es caro o barato en este proyecto de Mercado Inmoviliario en COLOMBIA.

