## Project Overview

Customer churn: the rate at which customers discontinue their relationship with a business, is a critical metric that directly impacts long-term profitability and sustainability. In today's competitive market landscape, retaining existing customers is often more cost-effective and beneficial than acquiring new ones. High churn rates can signal underlying issues in customer satisfaction, service quality, pricing models, or product value, and failing to address them can significantly affect a company’s bottom line.

This project aims to tackle the challenge of customer attrition by leveraging data-driven approaches to build a predictive model capable of identifying customers who are at risk of churning. By analyzing historical customer data spanning demographics, transactional behavior, website interactions, service usage, and feedback—the model can detect patterns and early warning signs that correlate with churn behavior.

The goal is not only to achieve high predictive accuracy but also to uncover actionable insights that help businesses understand why customers churn. These insights can then inform targeted retention strategies, such as personalized communication, loyalty programs, service improvements, or promotional offers, all designed to reduce churn and improve customer lifetime value (CLV).

Ultimately, this project underscores the strategic importance of predictive analytics in customer relationship management (CRM) and demonstrates how organizations can harness machine learning to become more proactive, responsive, and customer-centric in their operations.

## Problem Statement

Acquiring new customers is significantly more costly than retaining existing ones. Therefore, identifying early signs of churn can help in formulating timely and personalized retention strategies. The goal is to leverage customer behavior data to predict churn accurately.

Customer churn not only leads to revenue loss but also affects brand reputation and long-term growth. By analyzing patterns in demographics, purchasing habits, website engagement, service usage, and customer feedback, businesses can uncover the factors that contribute most to churn. This knowledge enables the development of targeted interventions—such as loyalty programs, improved service offerings, or customized communications—to reduce churn rates and enhance customer satisfaction.

Ultimately, this project aims to empower decision-makers with predictive insights, allowing them to shift from reactive problem-solving to proactive customer management.

## Tools and Methodology

### Tools Used:

* Python
* Jupyter Notebook
* Pandas, NumPy (Data manipulation)
* Matplotlib, Seaborn (Visualization)
* Scikit-learn (Machine Learning)
* TQDM (Progress tracking)

### Methodology:

* Data Loading and Exploration
* Exploratory Data Analysis (EDA)
* Feature Engineering (from nested structures)
* Encoding and Scaling
* Model Building (Logistic Regression, Decision Tree)
* Model Evaluation (Validation & Test Set)
* Confusion Matrix Visualization

## Data Source

The data was provided in an Excel file named Dataset.xlsx, which includes both flat and nested structures related to customer demographics, subscriptions, interactions, purchases, and more.

## 🧾 Brief Breakdown of the Dataset

| **Column**               | **Description**                                                         |
| ------------------------ | ----------------------------------------------------------------------- |
| `CustomerID`             | Unique identifier for each customer                                     |
| `Gender`                 | Gender of the customer (Male/Female)                                    |
| `Age`                    | Customer age                                                            |
| `Segment`                | Segment category the customer falls into                                |
| `Timestamp`              | Time of record or transaction                                           |
| `ChurnLabel`             | Target variable indicating churn (1 = churned, 0 = retained)            |
| `PurchaseHistory`        | Nested column with purchase frequency, total value, and product details |
| `SubscriptionDetails`    | Nested data on subscription plan, start/end date                        |
| `WebsiteUsage`           | Nested metrics on page views and time spent                             |
| `EngagementMetrics`      | Login frequency and usage metrics                                       |
| `Feedback`               | Contains rating and comments from the customer                          |
| `MarketingCommunication` | Email interaction data (sent, opened, clicked)                          |
| `ServiceInteractions`    | Types of interactions with customer service                             |
| `PaymentHistory`         | Payment methods, late payments, and related info                        |
| `ClickstreamData`        | Click behavior captured from the website                                |

## Process Taken to Analyze the Data

The data analysis process began with data exploration, where the dataset was carefully examined for any inconsistencies, such as missing values and duplicate records. Descriptive statistics were generated to summarize the central tendencies, dispersion, and distribution of the numerical features, which provided an initial understanding of the dataset’s structure and the nature of its variables.

Following exploration, a thorough exploratory data analysis (EDA) was conducted. Visualizations were employed to identify trends and relationships within the data. Key plots included the distribution of the target variable ChurnLabel, as well as count plots for categorical features such as Gender and Segment. A line chart was generated to observe the monthly churn trend over time, while a correlation heatmap helped uncover the strength and direction of relationships between numerical features. Additionally, a bar plot was used to analyze the relationship between customer feedback ratings and churn, offering insights into the role of satisfaction in customer retention.

Next, feature engineering was performed, particularly focusing on columns with nested data. These nested structures were parsed using Python’s literal\_eval function, which allowed string representations of lists or dictionaries to be converted into actual Python objects. From these, meaningful features were extracted, such as purchase frequency, total purchase value, subscription duration, website activity levels, and engagement frequency. Count-based features were also created to represent the variety and frequency of service interactions and payment methods, enhancing the dataset’s predictive power.

After feature extraction, encoding and scaling techniques were applied. Categorical variables like Gender and SubscriptionPlan were encoded into numerical format to make them suitable for machine learning algorithms. Numerical features were then standardized using StandardScaler to ensure that all variables contributed equally to the model, especially important for algorithms sensitive to feature scaling.

Finally, the cleaned and processed data was used for model building and evaluation. Two classification models were developed: Logistic Regression and Decision Tree Classifier. These models were trained on the training subset of the data and evaluated using standard classification metrics, including accuracy, precision, recall, and F1 score. To visualize model performance, confusion matrices were generated for each model, illustrating the models' ability to correctly distinguish between churned and retained customers.

Throughout this process, both statistical rigor and domain context were considered to ensure that the models and insights derived were both accurate and actionable. Visual examples of the plots and confusion matrices can be inserted to support the analysis and illustrate findings.
