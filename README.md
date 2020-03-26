# Addressing Baltimore's Aging Population
  The city of Baltimore has notoriously faced negative population growth rates, but this has also led to an aging population for the city. This is further compounded by the fact that household size in Baltimore is quickly declining. As someone working for the mayor’s office, we would like to know: what policy areas we must reinforce to increase the number of children in the city and combat the aging population issue?  We considered the factors of household income, fraction of the population married, and job density as possible factors contributing to this issue.  Our end result demonstrated that fraction of the population married and job density were the two factors having the highest impact on the number of children, suggesting that policy should focus on these two areas.

## Why is this a challenge for Baltimore?
  This business question is crucial for the city of Baltimore to address, because a declining population has serious economic consequences. For context, since 2010, Baltimore City has lost 3% of its population, or 18,500 residents, and its population just fell below 600,000 for the first time in over a century. Moreover, the city is aging, with the Baltimore City Department of Aging predicting that 25% of the city would be a senior by 2020, outnumbering school children in that year. In addition to this, the average household size has dropped steadily to about 2.23, with an influx of millenials unable to curb the population loss. 
  
  For a city with a debt of over $3billion dollars, having to allocate more funds towards pension programs and retirement funds can be burdensome, especially when there is a decline in the labor force whose taxes would pay for these programs. Losing children and family households means a  potential brain drain for Baltimore, and a drop of outside investment into the city, reducing economic stimulus. For both the senior citizens and families in question, this loss translates to less investment in infrastructure such as transportation and public education and facilities, furthering the cycle of depopulation. Essentially, today’s generation in Baltimore runs the risk of not having enough children to replace itself, placing further strain on an already burdened urban economy. In order to tackle this, the city government must figure out what is contributing to the decline in number of children in the city. 
  
  ## Our Solution
  
  



## Step-by-Step Instructions for Excel Data Manipulation
1. Begin by obtaining the csv files for Number of Children, Fraction Married, Household Income, and Job Density.
2. Starting with the Fraction Married file use a VLOOKUP function to match each of the other files.  We use the tract number as the lookup value.
3. Once all data is on same sheet, notice that there will be some cells that are blank or contain the value #N/A.  So we must apply filters to all the columns and filter out these values for each column to clean the data for analysis.
4. Copy and paste this filtered data to a new worksheet so that we can work with it.
5. We now want to create the following scatter plots: Fraction Married vs Number of Children, Household Income vs Number of Children, Job Density vs Number of Children.  For each of these be sure that Number of Children is the y-value.  We will also add trend lines to each of these charts and display the equation and R-squared value on the chart.
6. Create a multiple regression using Fraction Married, Household Income, and Job Density as the x-values and Number of Children as the y-value.  We will use the Data Analysis Toolpack Regression function to do this.
7. Create a multiple regression using just Fraction Married and Job Density as the x-values and Number of Children as the y-value.  Once againe we use the Data Analysis Toolpack Regression function to do this.
8. Create a correlation using the Data Analysis Toolpack Correlation function.  For the selected range select all of the values in the columns for all 4 variables.

