# RenoSmart : Personalised Strategies for Property Value Enhancement for Homeowners

### GROUP 1 MEMBERS :
- ABIGAIL MWENDWA
- IAN NZANGI
- ESTHER TERRY MUNENE
- WILLIAM ITOIA

## Project Overview

RenoSmart is a renovations company that aims to assist homeowners in King County, Washington, in strategically enhancing the estimated value of their properties through targeted renovations. 

Leveraging multiple linear regression modeling, our project focuses on helping RenoSmart give personalized advice to homeowners, empowering them to make informed decisions about renovation investments that maximize property value.

## Business Understanding

### Stakeholder Identification

1. Homeowners in King County: These individuals own residential properties and are seeking ways to maximize their property value. They are the primary beneficiaries of the project's outcomes, receiving tailored recommendations for renovation strategies.

2. RenoSmart: The construction company offers renovation services and plays a central role in providing personalized advice to homeowners. RenoSmart aims to enhance its reputation and business success by delivering effective renovation recommendations.

### Business Objective 

Offer tailored recommendations to homeowners on how to strategically increase the estimated value of their properties through renovations.

Identify renovation strategies that have the highest potential to enhance property value, leading to higher selling prices and greater returns on investment.

Provide homeowners with the knowledge and resources needed to make informed decisions about renovation investments, ultimately enhancing their property's value and marketability.

Drive customer satisfaction and loyalty by delivering impactful renovation advice, leading to increased recommendations and future engagements with RenoSmart

### Business Problem 

RenoSmart, a renovation expert, recently expanded to King County but lacks familiarity with local renovation needs. They seek assistance in understanding King County's unique renovation requirements and market dynamics to provide tailored renovation solutions. 

Through data-driven analysis and stakeholder engagement, the project aims to bridge this knowledge gap, enabling RenoSmart to offer informed and effective renovation services that meet the specific needs of homeowners in King County.

### Data Understanding

- King County House Dataset
  The dataset contained information about the houses in King County.
  The dataset has 21,597 entries and 20 columns
  The dataset includes a combination of data types, including objects (strings), floats, and integers.
  
- Column Name Dataset
  The dataset has 25 entries and 2 columns
  The dataset has brief descriptions of each column in the kc_house_data dataset. 
  The dataset data type is objects (strings).

### Data Visualization
![image](https://github.com/whareverr/dsc-phase-2-project-v2-3/blob/main/Visual1.png)
![image](https://github.com/whareverr/dsc-phase-2-project-v2-3/blob/main/Visual2.png)
![image](https://github.com/whareverr/dsc-phase-2-project-v2-3/blob/main/Visual3.png)
![image](https://github.com/whareverr/dsc-phase-2-project-v2-3/blob/main/Visual4.png)

### Data Analysis

Initial steps included understanding the data structure, handling missing values, and exploring column descriptions to gain insights into housing features.

Exploratory data analysis  was conducted, employing techniques like box plots to identify outliers and bar plots to visualize the impact of categorical variables on housing prices.

Modeling began with a simple linear regression to predict prices based on square footage, followed by multiple linear regression incorporating additional variables like bathrooms and bedrooms.

Models were refined iteratively, evaluating their performance using metrics such as R-squared and Root Mean Squared Error.

## Recommendations

 **Model Summary**
 
![image](https://github.com/whareverr/dsc-phase-2-project-v2-3/blob/main/Visual5.png)

From the provided OLS regression results, we can analyze the coefficients of the independent variables and their corresponding p-values to understand their impact on the dependent variable (price). Here's a breakdown:

1. **Interpretation of Coefficients**:
   - `sqft_living`: For every one-unit increase in square footage of living space, the price is estimated to increase by $134.83.
   - `sqft_living15`: Similarly, for every one-unit increase in square footage of living space in 2015, the price is estimated to increase by $100.88.
   - `sqft_above`: An increase in square footage above the ground level is associated with a decrease in price by $24.65.
   - `bathrooms`: Each additional bathroom adds approximately $39,090 to the price.
   - `bedrooms`: Each additional bedroom decreases the price by approximately $24,280.
   - `floors`: Each additional floor adds about $72,570 to the price.
   - `sqft_lot` and `sqft_lot15`: Changes in lot size (both current and in 2015) have smaller impacts on price, with coefficients of 0.1542 and -0.3512, respectively.
   - `yr_built`: Each year added to the age of the house decreases the price by $2,355.26.
   - `yr_renovated`: The effect of renovation on price is positive, with each unit increase in renovation year adding $9.89 to the price.

2. **Significance of Coefficients**:
   - All the coefficients have very low p-values (close to 0), indicating that they are statistically significant in predicting the house price.

3. **Model Fit**:
   - The R-squared value of 0.494 indicates that approximately 49.4% of the variance in the dependent variable (price) is explained by the independent variables in the model.
   - The F-statistic and its associated p-value suggest that the overall model is statistically significant.

4. **Diagnostic Tests**:
   - The Omnibus test and the Jarque-Bera test are used to check the normality assumption of the residuals. A low p-value (< 0.05) indicates that the residuals are not normally distributed.
   - Durbin-Watson statistic is used to detect the presence of autocorrelation in the residuals. A value close to 2 suggests no autocorrelation.

5. **Concerns**:
   - The condition number is large, indicating potential multicollinearity issues among the independent variables. This suggests that some variables may be highly correlated, which could affect the stability and interpretation of the coefficients.

Based on our analysis and evaluation of the multiple linear regression models, we recommend utilizing Model 4 for predicting house prices in your project. Here's why:

1. **Higher R-squared Value**: Model 4 demonstrated the highest R-squared value among all the models, indicating that it explains a greater proportion of the variance in housing prices compared to the other models. This suggests that Model 4 provides a better fit to the data by capturing more variation in the dependent variable through the independent variables.

2. **Lower RMSE Value**: The Root Mean Squared Error (RMSE) for Model 4 was the lowest among all the models, signifying that its predictions are, on average, closest to the actual house prices. This indicates higher accuracy in predicting house prices compared to the other models.

3. **Statistical Significance of Independent Variables**: All independent variables included in Model 4 were statistically significant, as evidenced by their p-values being less than 0.05. This means that each independent variable contributes significantly to explaining the variation in house prices.

By using Model 4, you can make more accurate predictions of house prices. Additionally, the model provides insights into which factors most strongly influence house prices, enabling informed decision-making when it comes to renovations.
