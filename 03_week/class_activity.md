# Where are we?

## Previosly in this class
- Ingest/Collect
- Store
- Process/Analyze
- Consume/Visualize
- Answers and Insights

## Later on in this class
- Exploratory data analysis
- Dashboards and Reporting 
- Forecasting

# Dataset

## Synthetic data
- is synthetic random?
- examples

## Different ways of creating synthetic data
- anonymization (https://kohokoho.herokuapp.com/)
- scratch
- mix

## Real world patterns
- growth
- market saturation
- trend
- seasonality
- advertisement
- pareto
- churn
- normalized data
- nepali context
- relationships between data (name and gender as an example)

## Class Activity
- what do you think the demography will look like (gender breakdown, age breakdown, address?, income? etc.)
- do you think depending on what you sell (maybe we should start our platform with select few items for simplicity purposes?), do you think a segment of demography will be interested?
- think in terms of visualization as well
- in terms of transaction, what might the different types of payment modality?
- lets explore similar questions.

## eHamroPasalmandu.com
Categories
- Mobile phone
- Laptop
- ca

# Tables
- users table
- transactions table
- items table


### Users
| columns        |                                     |                                                                               |
| -------------- | ----------------------------------- | ----------------------------------------------------------------------------- |
| user\_id       |                                     | primary key of users                                                          |
| name           |                                     | nepali names                                                                  |
| address        |                                     | kathmandu addresses                                                           |
| email          |                                     | firstname@lastname.fakedata.com                                               |
| dob            |                                     | 16-24, 24-30, 30-36, 36-42, 42+                                               |
| gender         | male, female, other, prefer not to say | approx 60% M, 40% F                                                           |
| channel        | facebook, friends,                  | 60% Word of Mouth, 10 Facebook post/ads, 10% others, 10% google search, 10% organic |
| first\_contact | app, web                            | random                                                                        |
| created on     |                                     | date                                                                          |

### Items
| columns   |                              |                     |
| --------- | ---------------------------- | ------------------- |
| item\_id  |                              | primary key of item |
| name      |                              |                     |
| category  | mobile phone, laptop, camera |                     |
| price     |                              |                     |
| inventory |                              |                     |
| url       |                              |                     |
