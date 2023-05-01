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

* **Project background and context**
⋅⋅⋅Space X advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because Space X can reuse the first stage. Therefore, if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against space X for a rocket launch. This goal of the project is to create a machine learning pipeline to predict if the first stage will land successfully.

* **Problems we need to find answers for**
⋅⋅⋅* What factors determine if the rocket will land successfully?
⋅⋅⋅* The interaction amongst various features that determine the success rate of a successful landing.
⋅⋅⋅*What operating conditions needs to be in place to ensure a successful landing program.

## **Methodology:**

### * **Data Collection

The data was collected using various methods

⋅⋅⋅* Data collection was done using get request to the SpaceX API.
⋅⋅⋅* Next, we decoded the response content as a Json using .json() function call and turn it into a pandas dataframe using .json_normalize().
⋅⋅⋅* We then cleaned the data, checked for missing values and fill in missing values where necessary.
⋅⋅⋅* In addition, we performed web scraping from Wikipedia for Falcon 9 launch records with BeautifulSoup. 
⋅⋅⋅* The objective was to extract the launch records as HTML table, parse the table and convert it to a pandas dataframe for future analysis.




