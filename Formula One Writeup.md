# Formula 1 Regression
###### Ahad Almutairi, Wafaa Alharbi

### 
##### Abstract
The main goal of this project is to predict the number of points each driver will gain after competeting in the Formula One race depending on pre-race and in-race features that will affect the scoring of points for all racers.   

##### Design
Formula One is concidered to be one of the complicated games in a sense that it has a rigrious set of rules that must be followed in order to grant points. In order to determine these points, data was scraped from the Formula 1 website. Then, multiple models were implemented to get the best fitted one to make a clear prediction.

##### Data
Data was scraped from F1 website and it included races from 2010-2021 in all locations the race has been held at so far. The data contained nearly 9000 rows and 28 columns before EDA and feature engineering. Most notable columns include: Fastest Lap Speed, Qualifying Position, Starting Grid Position and Fastest Lap Position. The data then was properly cleaned and handlened in the EDA phase to get a better use of it when fitting it into the suited model.

##### Algorithms
- Data Scraping to pull almost 9000 rows and 28 columns.
- Exploratory Data Analysis was done to the dataset.
- Building multple models and finding out the well-suited one for this specific dataset.


__F1 Scraped Dataset:__

Cleaning:
- dropped unnecessary that caused duplicated data and duplicated rows caused by merging datasets.
- Getting total number of seconds for time related columns.
- Replacing odd values with none then getting rid of all null values in the dataset.
- Transform object-type columns to numeric to incorporate in the model.
- Perform a sanity check to make sure theres no duplicated driver for the same race, location and year.
- Filling in Qualifying Q2 null values with Qualifying Q1 and Filling in Qualifying Q3 null values with Qualifying Q2.

Exploring: the data was explored by performing the correlation calculations to establish a relationship between all the features.

__Model Building:__
Around 8 models were tried and played with to get the best model that goes hand in hand with the dataset. After performing simple train and validation on the 7 models one was chosen for further investigation.
The eliminitaed models (gave poor Rˆ2 results):
1. Linear Regression.
2. Polynomail Degree 2 Regression.
3. Polynomial Degree 3 Regression. 
4. Random Forest Regression.
5. Bernoulli Regression.
6. Guassian Regression.
7. Descision Tree Regression.

The chosen model: __Gradient Boosted Regression__
- Train Rˆ2: 0.80
- Validate Rˆ2: 0.70
- Whole Data Rˆ2: 0.78
- Test Rˆ2: 0.72
- MAE: 2.2

Feature Engineering: in order to solve the overfitting and to ditch some uneeded features, feature engineering was performed on the chosen model.
1. Eliminating some features based on OLS coefficients that were nearing the zero with high P values.
2. Scaling Data.
3. Performing Lasso for feature selection.
4. Performing Cross Validatoin.
5. Introducing dummy variables.

Visualizing: graphs that depict the relationship between the predicted target and the actual target were made as well as graphs that show most important features that impact the prediction of the target. Diagnostic plot was also made before and after building the final model.

##### Tools
Numpy
Pandas
Matplotlib
Seaborn
SqlAlchemy
Jupyter
Sklearn
Statsmodel
Scipy
Flask
BeautifulSoup
Selenium


