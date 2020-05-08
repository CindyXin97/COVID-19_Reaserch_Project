# Which Feasible Measures does other countries can learn from Korea to Alleviate COVID-19? 

This project is to analyze the different urban groups responding to COVID and  the key factors impact the COVID_19 in Korea. We used clustering techniques to define the cities of it's infecting level and other related COVID-19 impacted areas. By combing the 3 time series related models and Susceptible Infected Recovered (SIR) Analysis to predict the future trend of COVID-19 and take the results of one of the factors. Meanwhile, we built the cluster-based anomaly detection model and identified the anomalous date, then we've found the relationship between policy and these anomalous date. By conducting the classification techniques, we came to our results of what are some effective meausres that other countries can learn from Korea.

# Data
3.1 Data Source

KCDC open dataset and Korean Statistical Information System
(https://www.kaggle.com/kimjihoo/coronavirusdataset, http://kosis.kr/eng/statisticsList/)

Time: Time series data of COVID-19 by region including test number, negative/positive number,
released number and deceased number along with patient info like age, sex and location.

Case: Data of COVID-19 infection cases in South Korea including location, group
infection,infection case(overseas or infected place).

PatientInfo: Epidemiological data of COVID-19 patients in South Korea including
age,sex,contact people number, confirm date, release date and decease date.

PatientRoute: Route data of COVID-19 patients in South Korea including where the patients
visited and dated.

SearchTrend: Trend data of the keywords searched in Naver(largest portal in Korea). The
keywords are cold, flu, pneumonia, coronavirus

Weather: Data of the weather including temperature, precipitation, wind speed and relative
humidity.

Sickbed: Detailed Status of sickbed by Region

Region: Statistics of public infrastructure and age & educational structures grouped by city, such as the ratio of elder people, the number of hospitals and schools, etc.

KOSIS - Korean Statistical Information Service: Demographic Population Distribution in South Korea (as of 2020)

# Method
### 1. EDA
### 2. Anomaly Detection and Policy Analysis:

In order to detect the anomaly days with infected people, we conducted cluster-based model anomaly detection and it performed the best in this situation with unlabeled data. After that, we think we are all consistent influence factors. Policy is one of the important factors that play an important role in these anomaly days so we dive deep into the policy.
### 3. Susceptible Infected Recovered (SIR) Analysis:

The SIR model of infection describes time dynamics of an infectious disease spreading through a homogenous closed population. The population is divided into three categories: Susceptible S, Infective I, or Recovered/Dead R. We simplify R for now and include dead people as recovered. 

The math behind it was like below:


### 4. Time Series Model and Regression :

MLP (Multi-layer Perceptron regressor), Prophet Model, ARIMA

### 5. Clustering 

Clustering Algorithm is used to find provinces with similar situations. We tried Kmeans, Gaussian Mixture and used silhouette score as a guideline to pick the number of clusters. 

### 6. Classification Model 

We used CART Tree, random forest to do classifications and analysed the feature importance. 

### Results 

## Contributors (Based on name letter order)
Di Xin 
Jianan Gong
Zheyuan Zhang
