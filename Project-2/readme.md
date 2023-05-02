# Project-2: Predicting Successful Landings of SpaceX Falcon 9 Rocket

This project focused on predicting the successful landings of SpaceX Falcon 9 rockets using machine learning techniques. The goal was to develop a model that could accurately predict whether a Falcon 9 rocket launch would result in a successful landing.

Following are the steps by step detail of the each phase of the project.

* Executive Summary
* Introduction
* Methodology
* Results
* Conclusion


## **Executive Summary:**

* **Web Scraping:** The project involved web scraping Falcon 9 launch records using a RESTful API and BeautifulSoup, a Python library for web scraping. This allowed the collection of relevant data related to SpaceX Falcon 9 rocket launches.

* **Data Parsing and Dataframe Creation:** The scraped data was parsed and transformed into a structured format. Python's Pandas library was used to create a dataframe, enabling efficient data manipulation and analysis.

* **Exploratory Data Analysis:** The project utilized both SQL and Python for exploratory data analysis (EDA). SQL queries were employed to extract relevant information from the dataset, while Python was used for data manipulation and statistical analysis. EDA techniques were applied to gain insights into the data and identify patterns or correlations.

* **Data Visualization:** The project involved visualizing successful and failed launches on a map using Folium, a Python library for creating interactive maps. This visualization provided a geographical perspective on the outcomes of Falcon 9 rocket launches.

* **Dashboard Application:** A dashboard application was built using Plotly Dash, a Python framework for building interactive web-based dashboards. The application showcased SpaceX launch records by site, payload, and other relevant parameters. It provided users with a comprehensive view of the Falcon 9 rocket launch history.

* **Machine Learning Models:** The project implemented three machine learning models, namely Support Vector Machines (SVM), Logistic Regression, and K-nearest neighbor (KNN). These models were trained and tested using the dataset, with the goal of predicting the success or failure of Falcon 9 rocket landings.

* **Machine Learning Pipeline:** A machine learning pipeline was built to streamline the process of training and evaluating the models. The pipeline included steps such as data preprocessing, feature selection, model training, and model evaluation. This enabled efficient experimentation and comparison of different models.

## **Introduction:**

* **Project background and context:**
    * Space X advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because Space X can reuse the first stage. Therefore, if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against space X for a rocket launch. This goal of the project is to create a machine learning pipeline to predict if the first stage will land successfully.

* **Problems we need to find answers for:**
  * What factors determine if the rocket will land successfully?
  * The interaction amongst various features that determine the success rate of a successful landing.
  * What operating conditions needs to be in place to ensure a successful landing program.

## **Methodology:**

### Data Collection

The data was collected using various methods

  * Data collection was done using get request to the SpaceX API.
  * Next, we decoded the response content as a Json using .json() function call and turn it into a pandas dataframe using .json_normalize().
  * We then cleaned the data, checked for missing values and fill in missing values where necessary.
  * In addition, we performed web scraping from Wikipedia for Falcon 9 launch records with BeautifulSoup. 
  * The objective was to extract the launch records as HTML table, parse the table and convert it to a pandas dataframe for future analysis.

### Data Wrangling

  * We performed exploratory data analysis and determined the training labels.
  * We calculated the number of launches at each site, and the number and occurrence of each orbits
  * We created landing outcome label from outcome column and exported the results to csv.

### EDA with Data Visualization

  * We explored the data by visualizing the relationship between flight number and launch Site, payload and launch site, success rate of each orbit type, flight number and orbit type, the launch success yearly trend. 

### EDA with SQL

  * We loaded the SpaceX dataset into a PostgreSQL database without leaving the jupyter notebook.
  * We applied EDA with SQL to get insight from the data. We wrote queries to find out for instance:
      * The names of unique launch sites in the space mission.
      * The total payload mass carried by boosters launched by NASA (CRS)
      * The average payload mass carried by booster version F9 v1.1
      * The total number of successful and failure mission outcomes
      * The failed landing outcomes in drone ship, their booster version and launch site names.
       
### Build a Dashboard with Plotly Dash

  * We built an interactive dashboard with Plotly dash
  * We plotted pie charts showing the total launches by a certain sites
  * We plotted scatter graph showing the relationship with Outcome and Payload Mass (Kg) for the different booster version.

### Predictive Analysis (Classification)

  * We loaded the data using numpy and pandas, transformed the data, split our data into training and testing.
  * We built different machine learning models and tune different hyperparameters using GridSearchCV.
  * We used accuracy as the metric for our model, improved the model using feature engineering and algorithm tuning.
  * We found the best performing classification model.

## **Result:**

* Flight Number vs. Launch Site:
    * From the plot, we found that the larger the flight amount at a launch site, the greater the success rate at a launch site.

   ![](/images/Result%20-%20Flight%20num%20vs%20Launch%20Site.png)

* Success Rate vs. Orbit Type
    * From the plot, we can see that ES-L1, GEO, HEO, SSO, VLEO had the most success rate.

   ![](/images/EDA-with-Data-Visualization-2.png)

* Payload vs. Orbit Type
    * We can observe that with heavy payloads, the successful landing are more for PO, LEO and ISS orbits.
    
    ![](/images/Payload%20vs%20orbit%20type.png)

* Launch Success Yearly Trend
    * From the plot, we can observe that success rate since 2013 kept on increasing till 2020.
    
    ![](/../main/images/EDA-with-Data-Visualization-1.png)
    
* Markers showing launch sites with color labels
   
   ![](/images/Launch%20Success%20vs%20failure.png)

* Launch Site distance to landmarks

   ![](/images/launchsite%20distance.png)

* Pie chart showing the success percentage achieved by each launch site

   ![](/images/Success%20Percentage%20launch%20site%20pie%20chart.png)

* Pie chart showing the Launch site with the highest launch success ratio

   ![](/images/Launch%20site%20success%20ratio.png)

* Scatter plot of Payload vs Launch Outcome for all sites, with different payload selected in the range slider

   ![](/images/scatter%20plot%20-%20payload%20vs%20launch%20outcome.png)

## **Conclusion:**

We can conclude that:
  * The larger the flight amount at a launch site, the greater the success rate at a launch site.
  * Launch success rate started to increase in 2013 till 2020.
  * Orbits ES-L1, GEO, HEO, SSO, VLEO had the most success rate.
  * KSC LC-39A had the most successful launches of any sites.
  * The Decision tree classifier is the best machine learning algorithm for this task.






