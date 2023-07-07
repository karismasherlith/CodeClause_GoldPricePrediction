# Gold Price Prediction
Python Code for Gold Price Prediction

1. IMPORTING MODULES
   - pandas: This library is used for data manipulation and analysis on structured datasets such as CSV files.
   - numpy: Numerical Python is a library used for numerical functions such as the use f multidimensional arrays and matrices.
   - matplotlib.pyplot: Used for implementing graphs, plots and charts on datasets.
   - train_test_split: Used for splitting a large data frame into training and testing subsets.
   - Linear Regression: Used for getting the linear relationship between a dependent variable and one or more independent variables.
   - mean_squared_error: Evaluates the performance of the regression models and finds the mean squared error between the true and predicted values.
     
2. LOADING DATASET
   - The dataset is loaded into the 'gold_data' data frame using the read_csv function.
     
3. STRUCTURE OF DATASET
   - .head() function helps to get the 1st 5 rows of the data frame.
     
4. SHAPE OF DATASET
   - The .shape() function helps you to get the number of rows and columns in the data frame.
     
5. INFORMATION
   - The .info() function helps you to get the summary of the entire data frame including names of columns, number of null values, memory usage etc.
   - It helps to understand the composition of the data frame.
     
6. CONVERT DATE TO DATETIME
   - Converts the string datatype data 'date' to a datetime datatype using the to_datetime() function.
     
7. SORTING
   - We then sort the data frame based on the date values.
     
8. DROP NULL VALUES
   - The empty valued rows within the data frame are removed from the data frame by using the dropna() function.
     
9. EXTRACTING COLUMNS
    - We create a new data frame named 'Data' by selecting only the 'Date' and 'Close' columns from the existing data frame 'gold_data'.
      
10. PLOTTING CLOSING PRICES
    - We create a figure of size 10 (width) and 6 (height).
    - We then plot a line graph with the Date column values as the x-axis and Close column values as the y-axis and label them respectively.
    - After setting the title for the graph we display it using the 'show' function.
      
11. NUMERICAL REPRESENTATION OF DATA
    - We first create a copy of the 'Data' data frame and store it in the same variable so as to avoid modifying the original data set.
    - We then create a new column named 'Days' which represents values of the number of days between two dates.
    - dt.days is used to get the number of days from the resulting time data.
      
12. SPLITTING SUBSETS
    - We create 2 data frames named 'X' and 'Y' which store the days and close column values respectively.
    - We then create the training and testing subsets by allocating 20% of the data frame for training and 80% for testing with the help of test_size=0.2.
    - We also set the random state to 42 so as to ensure the reproducibility of the split each time program is run.
      
13. LINEAR REGRESSION MODEL
    - We create a variable named 'model' which stores the linear relationship between the independent variables (X) and dependent variable (Y).
    - We then fit the model to reduce the squared difference between true and predicted values.
      
14. PREDICTING VALUES
    - We then predict the output values (Y) for the input value (X).
      
15. EVALUATING THE MODEL
    - We calculate the mean_squared_error value between the true values (Y_test) and predicted values (Y_pred) obtained from the regression model.
      
16. VISUALIZING THE RESULT
    - We plot 2 line graphs containing true and predicted values to compare.
    - We plot a scatter plot of true values and a line graph of predicted values.
    - The true values are in blue colour while the predicted values are in red colour.
       
17. MANUAL TESTING
    - We create a function which takes a model as the input.
    - The function asks the user to enter the date in the YYYY-MM-DD format.
    - This string is converted to datetime datatype and then to 'Days' which is nothing but the number of days between the given date and the minimum date.
    - A new data frame is then created with only the 'Days' column.
    - A new variable then stores the predicted value of the given data frame with the help of the trained model.
    - When the function is called by passing the name of the trained model, it asks the user for the date and then displays the predicted gold price for that day.
