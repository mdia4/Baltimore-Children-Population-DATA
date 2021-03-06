# Addressing Baltimore's Aging Population
  The city of Baltimore has notoriously faced negative population growth rates, but this has also led to an aging population for the city. This is further compounded by the fact that household size in Baltimore is quickly declining. As someone working for the mayor’s office, we would like to know: what policy areas we must reinforce to increase the number of children in the city and combat the aging population issue?  We considered the factors of household income, fraction of the population married, and job density as possible factors contributing to this issue.  Our end result demonstrated that fraction of the population married and job density were the two factors having the highest impact on the number of children, suggesting that policy should focus on these two areas.

## Why is this a challenge for Baltimore?
  This business question is crucial for the city of Baltimore to address, because a declining population has serious economic consequences. For context, since 2010, Baltimore City has lost 3% of its population, or 18,500 residents, and its population just fell below 600,000 for the first time in over a century. Moreover, the city is aging, with the Baltimore City Department of Aging predicting that 25% of the city would be a senior by 2020, outnumbering school children in that year. In addition to this, the average household size has dropped steadily to about 2.23, with an influx of millenials unable to curb the population loss. 
  
  For a city with a debt of over $3 billion, having to allocate more funds towards pension programs and retirement funds can be burdensome, especially when there is a decline in the labor force whose taxes would pay for these programs. Losing children and family households means a  potential brain drain for Baltimore, and a drop of outside investment into the city, reducing economic stimulus. For both the senior citizens and families in question, this loss translates to less investment in infrastructure such as transportation and public education and facilities, furthering the cycle of depopulation. Essentially, today’s generation in Baltimore runs the risk of not having enough children to replace itself, placing further strain on an already burdened urban economy. In order to tackle this, the city government must figure out what is contributing to the decline in number of children in the city. 

## Our Solution
  We began by investigating the individual connection between the input variables of household income, job density, and fraction of the population that is married.  By running linear regressions with each of our  input variables to determine which had the greatest impact on the number of children, we found that, individually, none of the variables could explain the number of children in a given census tract.  The regression with household income and number of children had the lowest R-squared value of  just 0.0298, meaning just 2.98% of the data was explained by this model.  The regressions with the inputs of fraction of the population married and job density respectively had R-squared values of 0.0422 and 0.0534.  These results were surprising, since logically one could assume that each of the three inputs (household income, job density, and fraction married) would be heavily correlated with the number of children in a census tract.  The charts below demonstrate this information.
  
![marriage chartimage](https://github.com/mdia4/Baltimore-Children-Population-DATA/blob/master/Charts/Fraction%20Married%20v%20Number%20of%20Children.png)

![income chartimage](https://github.com/mdia4/Baltimore-Children-Population-DATA/blob/master/Charts/Household%20Income%20v%20Number%20of%20Children.png)

![jobs chartimage](https://github.com/mdia4/Baltimore-Children-Population-DATA/blob/master/Charts/Jobs%20vs%20Number%20of%20Children.png)


  We ran a multiple linear regression with all three input factors and the resulting model had an R-squared value of just 0.1092, which means that just 10.92% of the data could be explained by this model.  In spite of the unimpressive R-squared value, the model had a Significance F value that was very close to zero.  This told us that our three inputs in conjunction do have an impact on the number of children.  When looking at the p-values, however, we did notice that household income had a p-value of 0.435, which was higher 0.018 for fraction married and almost 0 for job density.  Since a p-value below 0.05 tells us that the variable was a meaningful input, we chose to create a new model without household income. Perhaps this new model would have a higher R-squared value once the most insignificant variable was eliminated.

  Our second multiple linear regression had the inputs of job density and fraction of the population married.  Given the results of our previous multiple linear regression, we believed that this model would be more accurate.  With a R-squared value of just 0.107, however, this model was slightly less accurate than the first.  Once again, however, the Significance F value was extremely low and each of the input variables had p-values that were practically 0.  

  This trend of low R-squared values and low p-values was initially confusing, but upon further research we concluded that these models still contained relevant findings.  The low p-values for job density and fraction of the population married mean that these variables are important predictors for the output, even when the entire model has a low R-squared value.  Thus, a low R-squared value does not entirely discount the predictive power of the input variables. This data analysis leads us to conclude that when looking to solve Baltimore’s aging population, policymakers should consider policies that either promote marriage in the city or bring married couples to the city and policies to increase job density throughout the city. 

## Future Suggestions Addressing Our Solution
  The first solution we found was to bring and/ or retain married couples in Baltimore city. This conclusion makes even more sense when looking at some of the reasons why families are a large proportion of those moving out of Baltimore. (as mentioned previously, household sizes are on the decline.)  A number of factors can be credited for pushing away married couples and families wishing to settle down. Baltimore unfortunately still holds a reputation for being a dangerous city, and despite a decline in homicide rates, it still has the second highest murder rate in the country (343 murders reported last year.) The city also has high property tax rates, more than double surrounding jurisdictions. This causes the city to have many more rentors than owners, meaning families who want to own a home are pushed out to neighboring counties. Additionally, the public school system is notably problematic, with students performing at record lows for literacy/math evaluations and teachers condemning systemic underfunding and lack of facilities. Crime rates, high property taxes and poor public school education all make other counties more attractive to families, contributing to the depopulation of the city.

  Our second solution was to increase job density in Baltimore. Research demonstrates that  high degrees of entrepreneurship, work-place development, robust infrastructure, and trust in city finances all help promote this metric. Job density in turn is linked to economic growth and mobility, all of which contribute to attracting people to Baltimore. In order to expand job density in the city, Baltimore should seek to invest in its public infrastructure (such as transportation) as well as look into funding entrepreneurial endeavors. Additionally, pushing for full transparency in city government is essential to garnering the trust of  potential employers- particularly for a city plagued with numerous mismanagement scandals in the past years.

  Ultimately, as policy makers, we suggest that to bolster the number of children and families in the city, Baltimore fund and focus the issues that cater the most to them. Investing in public goods and setting up Baltimore to be economically attractive is essential to abating depopulation.

  
## Step-by-Step Instructions for Excel Data Manipulation
1. Begin by obtaining the csv files for Number of Children, Fraction Married, Household Income, and Job Density.
2. Starting with the Fraction Married file use a VLOOKUP function to match each of the other files.  We use the tract number as the lookup value.
3. Once all data is on same sheet, notice that there will be some cells that are blank or contain the value #N/A.  So we must apply filters to all the columns and filter out these values for each column to clean the data for analysis.
4. Copy and paste this filtered data to a new worksheet so that we can work with it.
5. We now want to create the following scatter plots: Fraction Married vs Number of Children, Household Income vs Number of Children, Job Density vs Number of Children.  For each of these be sure that Number of Children is the y-value.  We will also add trend lines to each of these charts and display the equation and R-squared value on the chart.
6. Create a multiple regression using Fraction Married, Household Income, and Job Density as the x-values and Number of Children as the y-value.  We will use the Data Analysis Toolpack Regression function to do this.
7. Create a multiple regression using just Fraction Married and Job Density as the x-values and Number of Children as the y-value.  Once againe we use the Data Analysis Toolpack Regression function to do this.
8. Create a correlation using the Data Analysis Toolpack Correlation function.  For the selected range select all of the values in the columns for all 4 variables.


## Sources
https://www.opportunityatlas.org/
https://www.brookings.edu/research/are-the-promises-of-job-density-taking-hold-in-cities/
https://www.forbes.com/sites/nextavenue/2019/08/25/is-an-aging-population-hurting-the-u-s-economy/#86d1df83aa10
https://nypost.com/2019/04/19/census-estimates-show-baltimores-population-continues-to-plummet/
https://www.baltimoresun.com/maryland/baltimore-county/cng-co-at-to-senior-alone-aging-20190916-xz5utajnmvc73btcdtwsofdazy-story.html
https://www.bizjournals.com/baltimore/news/2019/01/29/baltimores-debt-shakes-out-to-14k-per-taxpayer.html
https://www.government.nl/topics/population-decline/causes-and-effects-of-population-decline
https://www.baltimoresun.com/opinion/readers-respond/bs-ed-rr-rodricks-small-households-population-decline-letter-20190613-story.html
https://www.washingtonpost.com/local/baltimore-sees-biggest-population-loss-in-single-year-since-2001-census-estimates-show/2019/04/21/f601f560-62b9-11e9-9ff2-abc984dc9eec_story.html
https://www.baltimoresun.com/opinion/columnists/dan-rodricks/bs-md-rodricks-column-population-0612-story.html
https://comebackcity.us/2013/12/09/millennials-lead-baltimore-forward/
https://www.baltimoresun.com/maryland/baltimore-city/bs-md-census-estimate-population-20190416-story.html
https://www.towncharts.com/Maryland/Demographics/Baltimore-city-MD-Demographics-data.html


