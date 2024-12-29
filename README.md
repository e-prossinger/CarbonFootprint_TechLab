# [Picturing Carbon Footprints](https://techlabs-ms.framer.website/projects/picturing-carbon-footprints)

This repository contains the data analysis and modelling code for the data science project "Picturing Carbon Footprints" developed at TechLabs that estimates and visualizes individual carbon footprints.
A full description of the aims and contents of this project can be found in the  [accompanying blog post](https://techlabs-ms.framer.website/projects/picturing-carbon-footprints).

The project includes various machine learning models trained on a [Kaggle dataset](https://www.kaggle.com/datasets/dumanmesut/individual-carbon-footprint-calculation), along with an [interactive web application](https://carbonfeet.streamlit.app) built with Streamlit that provides data visualizations and allows users to explore model predictions. 

## Modelling code
The main analysis and modelling code is contained in the folder [`shared_notebooks`](shared_notebooks) and they correspond to the modelling approaches as follows (compare [Modelling](https://techlabs-ms.framer.website/projects/picturing-carbon-footprints#:~:text=Modelling) in the blog post).
> **Linear Regression**: Testing the model's assumptions we identified problems with heteroscedasticity caused probably by a bias for underestimating extreme values. All other assumptions were satisfied. We achieved an R² 93.3% using all 19 variables.
- [`model_linearRegression and EDA.ipynb`](shared_notebooks/model_linearRegression%20and%20EDA.ipynb)

> **Decision Tree Regression**: We used GridSearchCV with RepeatedKFold cross-validation to fine-tune hyperparameters and select the best model configuration. We achieved an R² 85% using all 19 variables.
- [`model_DecisionTree_GridSearchCV.ipynb`](shared_notebooks/model_DecisionTree_GridSearchCV.ipynb)

> **LightGBM Regression Model**: Answering 20 questions is time-consuming for the user, so we aimed to reduce the variables and select a better-performing model to maintain prediction accuracy.
- [`model_LightGBM and Feature Selection.ipynb`](shared_notebooks/model_LightGBM%20and%20Feature%20Selection.ipynb)
- [`Lazy_Predict, LGBM_Regress,Feature_Select, Over_Fitt.ipynb`](shared_notebooks/Lazy_Predict,%20LGBM_Regress,Feature_Select,%20Over_Fitt.ipynb)

> **Decision Tree Classification:** To create a binary classification model, we median split the carbon emission data. The model achieved an accuracy of 85% using 18 variables.
- [`model_DecisionTreeClassifikation.ipynb`](shared_notebooks/model_DecisionTreeClassifikation.ipynb)


## Team members
We also collect further files from individual team members, partly from the initial modelling phase as well as side-projects like image classification.
### Mahboubeh Abdighara
*Tasks*: Modeling; model selection, evaluation, and feature analysis
- [Notebooks](individual_notebooks/Mahboub-cmyk)

### Prashant Kumar
*Tasks*: Data Visualization
- [Notebooks](individual_notebooks/Prashant/)

### Falko Mecklenbrauck
*Tasks*: Research of background information, Streamlit App
- [Code for Streamlit app in separate github repository](https://github.com/FalkMeck/CarbonFootprint_Group4)

### E. Prossinger
*Tasks*: Data Preprocessing, Modeling, Image Classification, Creative Director
- [Notebooks](individual_notebooks/Prossinger)