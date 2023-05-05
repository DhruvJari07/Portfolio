# Project-3: Understanding Churn in SME Customers of Utility Company: Exploring the Role of Price Sensitivity and Developing a Predictive Model for Discount Incentive

Exploring churn in SME customers of Utility Company, we investigated the impact of price sensitivity and developed a predictive model to identify customers at risk. Our findings revealed the need for feature engineering and model optimization to improve churn prediction accuracy and guide targeted discount incentives.

Following are the proposed steps for addressing this challenge.

## **Hypothesis Formulation:**
The hypothesis we aim to test can be formulated as follows:

"Price changes significantly influence the likelihood of churn among SME customers of our client."

## **Major Steps to Test the Hypothesis:**

* **Data Collection:**
To effectively test the hypothesis, we would need access to the following data from the client:
   * **Customer information:** This includes demographics, such as age, gender, location, and business type as well as historical data on customer tenure and churn status.
   * **Usage patterns:** Data on energy consumption by customers over time can provide insights into their energy needs and potential correlations with churn.
   * **Contract details:** Information about the type of contracts customers have (e.g., fixed-term, variable, or rolling contracts), contract start and end dates, and any previous changes in contract terms.
   * **Price-related data:** This includes historical price levels, specific price changes (dates and amounts), and the duration of each price period.
   * **Competitor data:** If available, data on competitor offerings, such as price changes or promotions, can provide additional context for customer churn analysis.


* **Exploratory Data Analysis:** 
Conducting exploratory analysis on the relevant fields can provide valuable insights into customer churn behavior. Some potential analyses include:

  * **Churn rate calculation:** Calculate the overall churn rate and explore how it varies across different customer segments.
  * **Correlation analysis:** Identify correlations between churn and various factors such as price changes, customer tenure, usage patterns, and demographic information.
  * **Customer segmentation:** Group customers based on characteristics such as price sensitivity, usage patterns, or demographics, and analyze their churn behavior within each segment.


* **Feature Engineering:**
To enhance the predictive power of our models, we should consider feature engineering techniques, including:

  * **Calculating price change percentages:** Derive a new feature representing the percentage change in price between consecutive periods, as this may capture customers' response to price fluctuations.
  * **Price stability indicators:** Create features indicating the stability or volatility of prices experienced by each customer.
  * **Interaction terms:** Explore the interaction between different variables, such as customer tenure and price changes, to capture potential non-linear relationships.


* **Model Development:**
Selecting appropriate analytical models is crucial for accurate predictions. Potential models to consider include:

  * **Logistic regression:** A widely used model to predict binary outcomes like churn, providing interpretable insights into the factors influencing churn.
  * **Decision trees and random forests:** These models can handle non-linear relationships and capture interactions between variables.
  * **Gradient boosting:** Boosting algorithms, such as XGBoost or LightGBM, can effectively handle large datasets and provide high predictive performance.


* **Model Evaluation:**
To assess the performance of our models and validate the hypothesis, we should:

  * Split the dataset into training and testing sets to evaluate model performance on unseen data.
  * Utilize evaluation metrics such as accuracy, precision, recall, and F1-score to measure the model's effectiveness in predicting churn.
  * Conduct statistical tests to evaluate the significance of price changes on customer churn while controlling for other relevant factors.


* **Interpretation and Recommendations:**
Based on the results obtained, we can:

  * Interpret the findings and identify the key drivers of churn, specifically focusing on the impact of price changes.
  * Quantify the price sensitivity of customers by analyzing their response to price fluctuations.
  * Provide actionable recommendations, such as offering discounts to the customers that are more likely to churn due to price.

## 1. Data Collection: 
The client has sent over some data which includes:

  * Historical customer data: Customer data such as usage, sign up date, forecasted usage etc
  * Historical pricing data: variable and fixed pricing data etc
  * Churn indicator: whether each customer has churned or not

Description of all the data is as follows:

#### client_data.csv

  *	id = client company identifier
  *	activity_new = category of the company’s activity
  *	channel_sales = code of the sales channel
  *	cons_12m = electricity consumption of the past 12 months
  *	cons_gas_12m = gas consumption of the past 12 months
  *	cons_last_month = electricity consumption of the last month
  *	date_activ = date of activation of the contract
  *	date_end = registered date of the end of the contract
  *	date_modif_prod = date of the last modification of the product
  *	date_renewal = date of the next contract renewal
  *	forecast_cons_12m = forecasted electricity consumption for next 12 months
  *	forecast_cons_year = forecasted electricity consumption for the next calendar year
  *	forecast_discount_energy = forecasted value of current discount
  *	forecast_meter_rent_12m = forecasted bill of meter rental for the next 2 months
  *	forecast_price_energy_off_peak = forecasted energy price for 1st period (off peak)
  *	forecast_price_energy_peak = forecasted energy price for 2nd period (peak)
  *	forecast_price_pow_off_peak = forecasted power price for 1st period (off peak)
  *	has_gas = indicated if client is also a gas client
  *	imp_cons = current paid consumption
  *	margin_gross_pow_ele = gross margin on power subscription
  *	margin_net_pow_ele = net margin on power subscription
  *	nb_prod_act = number of active products and services
  *	net_margin = total net margin
  *	num_years_antig = antiquity of the client (in number of years)
  *	origin_up = code of the electricity campaign the customer first subscribed to
  *	pow_max = subscribed power
  *	churn = has the client churned over the next 3 months

#### price_data.csv

  *	id = client company identifier
  *	price_date = reference date
  *	price_off_peak_var = price of energy for the 1st period (off peak)
  *	price_peak_var = price of energy for the 2nd period (peak)
  *	price_mid_peak_var = price of energy for the 3rd period (mid peak)
  *	price_off_peak_fix = price of power for the 1st period (off peak)
  *	price_peak_fix = price of power for the 2nd period (peak)
  *	price_mid_peak_fix = price of power for the 3rd period (mid peak)
 
## 2. Exploratory Data Analysis:

After conducting a thorough analysis of the data, following are some patterns that were identified.




