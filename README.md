# Phase_3_Project

# Telco Customer Churn

Customer churn, also known as customer depletion, occurs when customers stopped using a company's product or service during a certain time frame. A telephone companies is interested in identifying segments of these customers because the price of acquisition for a new customer is greater than retaining an existing one.Therefore, they would like a churn prediction model to proactively engage the customers a risk of churning with special offers to prevent them from leaving.

#### Data Dictionary (columns)

* customerID: customer ID
* gender: whether the customer is a male or a female
* SeniorCitizen: whether the customer is a senior citizen or not (1, 0)
* Partner: whether the customer has a partner or not (Yes, No)
* Dependents: whether the customer has dependents or not (Yes, No)
* tenure: number of months the customer has stayed with the company
* PhoneService: whether the customer has a phone service or not (Yes, No)
* MultipleLines: whether the customer has multiple lines or not (Yes, No, No phone service)
* InternetService: customer’s internet service provider (DSL, Fiber optic, No)
* OnlineSecurity: whether the customer has online security or not (Yes, No, No internet service)
* OnlineBackup: whether the customer has online backup or not (Yes, No, No internet service)
* DeviceProtection: whether the customer has device protection or not (Yes, No, No internet service)
* TechSupport: whether the customer has tech support or not (Yes, No, No internet service)
* StreamingTV: whether the customer has streaming TV or not (Yes, No, No internet service)
* StreamingMovies: whether the customer has streaming movies or not (Yes, No, No internet service)
* Contract: the contract term of the customer (Month-to-month, One year, Two year)
* PaperlessBilling: whether the customer has paperless billing or not (Yes, No)
* PaymentMethod: the customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
* MonthlyCharges: the amount charged to the customer monthly
* TotalCharges: the total amount charged to the customer
* Churn: whether the customer churned or not (Yes or No)

## Exploratory Data Analysis

#### Churn within the given population

![customerID](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/customerID.png)

27% of the customers have churned.

### Categorical Data thats significant 

#### Phone Service

![churn by PhoneService](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/churn%20by%20PhoneService.png)
![Percentage of churn by PhoneService](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/Percentage%20of%20churn%20by%20PhoneService.png)

The customers subscribed to the phone service represents 90% of the dataset. No correlation between the two.

#### Online Security

![churn by OnlineSecurity](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/churn%20by%20OnlineSecurity.png)
![Percentage of churn by OnlineSecurity](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/Percentage%20of%20churn%20by%20OnlineSecurity.png)

Customers without online security have a churn rate of 42% compared with 15% for those that have the given security service.

#### Tech Support

![churn by TechSupport](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/churn%20by%20TechSupport.png)
![Percentage of churn by TechSupport](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/Percentage%20of%20churn%20by%20TechSupport.png)

Customers without tech support 49% of the total customers while the ones with support represent 29% of the total customers. The Churn rate is 41% for those without support, then those with support have a 15% churn rate, which is significantly lower. 

#### Contract

![churn by Contract](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/churn%20by%20Contract.png)
![Percentage of churn by Contract](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/Percentage%20of%20churn%20by%20Contract.png)

Contract is a major factor when talking about churn rate. When we look at the month-to-month the churn rate is staggering. But, as the contract gets longer the churn rate gets smaller.

### 4.2 Numerical Data

#### Tenure

![Customers distribution by tenure](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/Customers%20distribution%20by%20tenure.png)
![churn by tenure](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/churn%20by%20tenure.png)
![Percentage of churn by tenure](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/Percentage%20of%20churn%20by%20tenure.png)

Tenure shows that long contracts are important for lasting sucess. 

#### Monthly Charges

![Customers distribution by MonthlyCharges](https://github.com/mriffaud/Telco-Customer-Churn/blob/master/images/Customers%20distribution%20by%20MonthlyCharges.png)


## Conclusion

After narrowing down my opinions after completing an array of models I choose the Ramdon Forest. It showed the greatest improvment, and most importantly the largest improvment in recall score. I know that I do not have my confusion matrix shown, but the false negatives were slashed in half from my baseline model to my final model. This is important because I focused on customers who were predicted to not churn but actually do churn. The increase in recall score from my confusion matix jumped from .51 - .66 or in other words my false negatives decreased from 617 to 310 (an improvment). Reducing the false negatives focuses on making those falsly labled customers valued, keeping the current customers content. Another point to mnake is that keeping customers is less expensive than finding new ones.   








































