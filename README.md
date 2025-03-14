# TOPIC: PREDICTING MOVIE BOX OFFICE REVENUE
This study aims to build a machine learning model using python to predict box office revenue using factors such as genre, budget and popularity. The dataset used for this project is the TMDB movie dataset from kaggle, which contains movie-related attributes such as budget, revenue,genre,release date,popularity score,production company...
## Data Preprocessing
### Data Cleaning
The dataset contained missing values, which were handled through removal, we dropped the missing values.
We also identified and addressd outliers in key numerical variables like budget.
### Feature Engineering
   -  Extracted date-related features from the release date column to analyze the impact of release timing on revenue.
   *  Compared revenue trends across different months.
   +  Performed frequency encoding on the genre feature to convert categorical vaalues into numerical format.
### Data Distribution Analysis
  - Both budget revenue were found to be left_skewed, indicating a concentration of movies with higher budgets abd lover revenues.
  * A log transformation was applied to normalize the skewed distributions and improve model performace.
### Correlation and Linearity.
  - Checked the linearity between budget and revenue and found our data was non-linear
  * Conducted a correlation analysis to identify relationship between features and revenue. Budget and Revenue showed strong correlation
## Model Selection and Trainig
### Model choice
Given the presence of outliers and non-linearity in the data, we selected a **Random Forest Regressor** as our predictive model. This model is robust to outliers and can capture complex, non-linear relationships in the data.
### Feature scaling
To ensure consistency in fature values, numerical features wre scaled using standardization techniques.
### Model Traing
The dataset was split into training and test sets, and Random Forest Regressor was trained using the processed features.
## Model Evaluation
### Performance Metrics
The model was evaluated using the following metrics:
      - Mean Squared Error(MSE): 4.6
      * R_Squared score: 0.67, indicating that 67% of the variance was explained by the model.
### Residual Analysis
   - A histogram of resduals showed a bell-shaped curve, indicating that the residuals were normally distributed.
   - This suggests that the model captured most of the underlying patterns in the data without major systematic errors

The **Random Forest Regressor** provided a reasonable prediction accuracy for movie box office revenue, with an R-squared score of 0.67.







