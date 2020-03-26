# Baltimore-Children-Population-DATA



## Step-by-Step Instructions for Excel Data Manipulation
1. Begin by obtaining the csv files for Number of Children, Fraction Married, Household Income, and Job Density.
2. Starting with the Fraction Married file use a VLOOKUP function to match each of the other files.  We use the tract number as the lookup value.
3. Once all data is on same sheet, notice that there will be some cells that are blank or contain the value #N/A.  So we must apply filters to all the columns and filter out these values for each column to clean the data for analysis.
4. Copy and paste this filtered data to a new worksheet so that we can work with it.
5. We now want to create the following scatter plots: Fraction Married vs Number of Children, Household Income vs Number of Children, Job Density vs Number of Children.  For each of these be sure that Number of Children is the y-value.  We will also add trend lines to each of these charts and display the equation and R-squared value on the chart.
6. Create a multiple regression using Fraction Married, Household Income, and Job Density as the x-values and Number of Children as the y-value.  We will use the Data Analysis Toolpack Regression function to do this.
7. Create a multiple regression using just Fraction Married and Job Density as the x-values and Number of Children as the y-value.  Once againe we use the Data Analysis Toolpack Regression function to do this.
8. Create a correlation using the Data Analysis Toolpack Correlation function.  For the selected range select all of the values in the columns for all 4 variables.

