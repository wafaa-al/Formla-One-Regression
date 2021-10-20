# Formula 1 Regression
###### Ahad Almutairi, Wafaa Alharbi

### 
##### Goal of the project
The core objective of this project is to predict what identifies a winner at the Formula One race through the _result points_.

After performing the initial EDA which includes:
1. Web Scarpping of the Formula One website which resulted into 3 different data frames based on each year the race occured from 2010 to 2021 which were later on concatenated into one data frame.
2. Dropped all duplicated and uneeded columns.
3. Removed & handled nulls.
4. Converting object-type columns into numeric.
5. Converting Time-formatted values into the total number of seconds.

The number of columns and rows before cleaning were **53 and 9413**
After cleaning up the data the number of columns and rows are **28 and 3294**

<img src="https://github.com/AhadAl977/Formula-one-Regression/blob/main/Images/heatmap.png" width="400"/>

The correlation between all numeric columns was calculated. As shown in the heatmap graph there are a lot of columns that are highly correlated with another for example Qualifying Pos with Starting Grid Pos. 

<img src="https://github.com/AhadAl977/Formula-one-Regression/blob/main/Images/regression%20models.PNG" width="350"/> 
Several models have been tested to generate the best Rˆ2 value possible to start building on. As seen in the table above the best Rˆ2 value was in the Polynomial Regression which resulted in 0.75 in both training set and validation set which further indicates the absence of overfitting. This model has been chosen for the regression probelm of this project.


<img src="https://github.com/AhadAl977/Formula-one-Regression/blob/main/Images/aftermodeling.png" width="350"/> 
<img src="https://github.com/AhadAl977/Formula-one-Regression/blob/main/Images/ResandPredicted.png" width="350"/> 

The first model that was tested and played with was OLS with the Rˆ2 value **=0.727** (as shown previously in the table above). Using this initial model two simple graphs were made to paint the picture clearly. The first graph was done to plot the values of the __true target__ & the __predicted target__ which shows some linearity with much added noise.
In the second graph though, a plot was done to depict the relationship between the __error__ & the __predicted target__. A lot of residiuals are shown across the __predicted target__ values. Given that the OLS is the second-worse in terms of Rˆ2 value there's no doubt that there's plenty of errors and the __predicted target__ values didn't fit well once compared with the __true target__ values.


##### Futrue Work
1. Betterment of Rˆ2 value through building upon the **Polynomial Regression Model**.
2. Introducing Categorical features such as car type with dummy variables.



