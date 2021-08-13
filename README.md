# 21-Machine-Learning-Challenge
## About
This repository was built to test machine learning models from a dataset acquired from NASA's Kepler space telescope.  The model will be a supervised classification model that will predict whether a potential planet is indeed a planet.

In this project, I utilized several sciket-learn libraries to test different classification models including K nearest neighbors, logistic regression, random forest and support vector machine.  For each model, the data was preprocessed by splitting into training and testing data plus scaling the numerical data.  The models were then tuned using GridSearch. Pandas and matplotlib were also used to import, clean and visualize the data. All of this was done inside of Jupyter Notebook.  

## Results
The model I believe to be the most accurate is KNN. This belief is based both the classification report and model score.  It slightly edged out the SVM and LR models in model score, but it also performed better on the classification report.  Specifically for the "CONFIRMED" class, it had a higher Precision score, which indicates that this model has a higher percent of correct predictions and Recall score indicating a higher percent of positive cases were caught by the model. My RFC model predicted zero candidates or confirmed clases which could be a sign of overfitting the model.

I used the features listed below to test my models.  While running my random forest classifier these features ranged in importance from 10% - 23% with the planet's radius being the most important.  I believe this is a strong list of features due to the high importance of each feature. However, there are many more features available in the dataset that could be added to this in the future to create a more accurate model. 

#### Selected Features:
* koi_period: The interval between consecutive planetary transits
* koi_impact: The sky-projected distance between the center of the stellar disc and the center of the planet disc at conjunction, normalized by the stellar radius.
* koi_duration: The duration of the observed transits. Duration is measured from first contact between the planet and star until last contact. 
* koi_prad: The radius of the planet. Planetary radius is the product of the planet star radius ratio and the stellar radius.
* koi_teg: Approximation for the temperature of the planet.
* koi_steff: The photospheric temperature of the star.
* koi_slogg: The base-10 logarithm of the acceleration due to gravity at the surface of the star.


## Built With
* Joblib
* Jupyter Notebook
* Matplotlib
* Pandas
* Python
* scikit-learn

## Sources
* https://www.kaggle.com/nasa/kepler-exoplanet-search-results
* https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html
