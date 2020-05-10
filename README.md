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

![Anomaly_Detection_results](https://github.com/CindyXin97/COVID-19_Research_Project/blob/master/Image/Anomaly_Detection_results.png)
### 3. Susceptible Infected Recovered (SIR) Analysis:

The SIR model of infection describes time dynamics of an infectious disease spreading through a homogenous closed population. The population is divided into three categories: Susceptible S, Infective I, or Recovered/Dead R. We simplify R for now and include dead people as recovered. 

The math behind it was like below:

![SIR_ Model_Math](https://github.com/CindyXin97/COVID-19_Research_Project/blob/master/Image/SIR_%20Model_Math.png)

![SIR_Result](https://github.com/CindyXin97/COVID-19_Research_Project/blob/master/Image/SIR_Result.png)

### 4. Time Series Model and Regression :

MLP (Multi-layer Perceptron regressor), Prophet Model, ARIMA

![ARIMA](https://github.com/CindyXin97/COVID-19_Research_Project/blob/master/Image/ARIMA.png)

### 5. Clustering 

Clustering Algorithm is used to find provinces with similar situations. We tried Kmeans, Gaussian Mixture and used silhouette score as a guideline to pick the number of clusters. 

### 6. Classification Model 

We used CART Tree, random forest to do classifications and analysed the feature importance. 

### Results 

Based on clustering methods, we divided cities in Korea into 3 infective levels. And we conducted  three time-series model related MLP, Prophet, ARIMA to predict the number of existing COVID-19 infected patients for each day, we found that this pandemic will end on May 17th, 2020 as ARIMA performs the best. By taking 'elementary_school_count', 'kindergarten_count', 'university_count',  'academy_ratio', 'elderly_population_ratio',  'vehicle', 'nursing_home_count', 'elderly_alone_ratio' and 'search trend' as features, we conducted classification model with decision tree and random forest. Finally, we identified nursing home counts, academy ration, vehicle number and search trend really influence the performance of control in Korea. In conclusion, starting emergency diagnosis for the elderly,  closing the schools, limiting people’s outdoor activities and raising people’s awareness are feasible measures  in Korea which other countries can learn from.  


## Contributors (Based on name letter order)
Di Xin (dx489@nyu.edu)
Jianan Gong (jg6193@nyu.edu)
Zheyuan Zhang (zz2498@nyu.edu)
