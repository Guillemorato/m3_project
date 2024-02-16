ih_datamadpt0923_project_m3

## Modelo XGBoost para la predicción de precios de diamantes

Este repositorio contiene un modelo de regresión XGBoost entrenado para predecir el precio de diamantes. A continuación, se describe brevemente el propósito de cada función utilizada en el notebook XGBoost_Model.ipynb:

Carga de Datos: Se utilizó la función pd.read_csv() de la biblioteca pandas para cargar el conjunto de datos de diamantes. Luego, se eliminaron columnas innecesarias utilizando el método drop().

Preprocesamiento de Datos: Se aplicó el método pd.get_dummies() para codificar las variables categóricas del conjunto de datos, convirtiéndolas en variables dummy. Esto facilita el procesamiento de las características categóricas en el modelo.

División de Datos: Se utilizó la función train_test_split() de scikit-learn para dividir el conjunto de datos en conjuntos de entrenamiento y prueba. Esto se hizo con el fin de entrenar el modelo en una parte de los datos y evaluar su rendimiento en otra parte no vista.

Entrenamiento del Modelo: Se utilizó el modelo XGBoost implementado en la biblioteca xgboost. Se especificaron los hiperparámetros del modelo (por ejemplo, colsample_bytree, gamma, learning_rate, max_depth, n_estimators, etc.) y se ajustó el modelo a los datos de entrenamiento utilizando el método fit().

Predicción y Evaluación: Se realizaron predicciones en el conjunto de datos de prueba utilizando el método predict(). Se evaluó el rendimiento del modelo utilizando la métrica de error cuadrático medio (RMSE) y se calcularon los puntajes de validación cruzada utilizando la función cross_val_score().

Generación de Predicciones: Se aplicó el modelo entrenado a un conjunto de datos de prueba separado (diamonds_test.csv) para generar predicciones sobre los precios de los diamantes. Estas predicciones se guardaron en un archivo CSV.

## Dependencias
El código en el notebook requiere las siguientes bibliotecas de Python:

- numpy

- pandas

- matplotlib

- scikit-learn

- xgboost
