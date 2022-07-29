# AUT-Datamining-projects
Projects and pratical assignments for data mining course at AUT, spring 2022

## Projects:
- [Preprocessing iris flower dataset](https://github.com/hedzd/AUT-Datamining-projects/tree/main/Preprocess_IRIS_dataset)
- Neural network
     - [Circles classification](https://github.com/hedzd/AUT-Datamining-projects/blob/main/Neural_Network/circles_classification.ipynb)  
     - [Classification fashion mnist dataset ](https://github.com/hedzd/AUT-Datamining-projects/blob/main/Neural_Network/fashion_mnist.ipynb)
- [Clustring](https://github.com/hedzd/AUT-Datamining-projects/tree/main/Clustering)
-  [Assosiation rules](https://github.com/hedzd/AUT-Datamining-projects/tree/main/Association_Rules)
-  [Final project](https://github.com/hedzd/AUT-Datamining-projects/tree/main/Final_Project)

## Preprocessing iris flower dataset:
Various pre-processings were done in this project.
1. Missing values were recognized and dropped
2. **One-hot encoding** have been used for encoding _categorical features_
3. _Numerical features_ were normalized using **StandardScaler** 
4. **Principal Component Analysis (PCA)** have been used for dimensionality reduction (4D to 2D)
5. Reduced features have been visualized
6. Original Dataset(without NaN-values) have been visualized using Box plot
### Results:
**PCA output**  
![PCA output plot](Preprocess_IRIS_dataset/assets/PCA_plot.png)
  
  
**Features boxplot**  
![Features boxplot](Preprocess_IRIS_dataset/assets/boxplot.png)
## Circles classification:
The final goal of this project was to make and tune a suitable ANN for classifying 2D-data in form of circles.
Different steps were done in order to grasp a better understanding of ANNs. In each step, model accuracy and loss were plotted for both test and train datasets.
### Results:
**Accuracy and loss**  
![Accuracy](https://i.ibb.co/P46yNz1/plot3.png)
![loss](https://i.ibb.co/dQjfTd7/plot1.png)  

**Decision boundary**  
![Decision boundary](https://i.ibb.co/Cs1dDHS/plot2.png)

## Classification fashion MNIST dataset:
Simple ANN on Fashion MNIST dataset using tensorflow.
### Results:
**Train accuracy:** 0.8821  
**Test accuracy:** 0.8820  
**Confusion matrix**  
<img src="https://i.ibb.co/xmLfT0Z/plot4.png" width="450" height="450">

## Clustring:
Using k-means and DBSCAN for clustring given datasets  
### K-means
- **K-means** have been used to cluster a given dataset. 
- **The elbow method** have been used to obtain the optimal value of K in k-means algorithm
- K-means have been used on digits dataset, at first dimensionality reduction was done using **Isomap** then k-means was performed on redusced dataset.  
### DBSCAN
- **KNN** have been used to determine the optimal value for _epsilon_ in DBSCAN algorithm
- Different values for _MinPts_ and _epsilon_ have been tested in order to find the best hyperparameters for DBSCAN on the dataset  

**Results:**
k-means performs well when the data is linearly separable. But in other cases, due to the linearity of k-means clustering, the result is not desirable.
The DBSCAN algorithm is a density-based clustering algorithm that performs better than k-means when our dataset is not linearly separable.
## Assosiation rules:
In this assignment, **association rules** have been extracted from a given dataset using **apriori algorithm**.  

## Final project
The general purpose of this project was to implement a classifier which finds symptoms of diabetes or pre-diabetes for the given patients information based on a CDC dataset. **XGBoost** was used to implement classification model.
- Preprocessing
     - Null values / meaningless values have been removed
     - Numerical features were normalized
     - Categorical features have been changed to one-hot-encoding
     - train/test dataset have been created
- Model creation
     - classification model was defined using **XGBClassifier**
- Model evaluation
     - **Accuracy**, **persicion** and **recal**  have been calculated for train and test datasets
     - **ROC-AUC score** has been calculated
     - Confusion matrix has been plotted

- Hyperparameter tuning 
     - Best hyperparameters for our XGBClassifier have been found using **GridSearchCV**
     - Hyperparameter changes have been plotted 
     
### Results:  
Best hyperparameters: {'colsample_bytree': 0.8, 'learning_rate': 0.05, 'max_depth': 3, 'n_estimators': 300}  
Test Accuracy: 75.70%  
Train Accuracy: 76.13%  
Test precision:  0.759  
Train precision:  0.763  
Test recall:  0.757  
Train recall:  0.761  
ROC score:  0.840  
  
Plot of mean score and its standard deviation for each hyperparameter:
![hyperparameters](https://i.ibb.co/JkqKL8J/plot5.png)
