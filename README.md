# Credit Scoring Model for Buy-Now-Pay-Later Service

This project is focused on building a Credit Scoring Model to assess the creditworthiness of potential borrowers for a buy-now-pay-later service. The model uses transaction data provided by an eCommerce platform to classify customers as high or low risk based on their likelihood of defaulting on payments. The solution involves exploratory data analysis (EDA), feature engineering, model development, and risk prediction.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Description](#data-description)
3. [Tasks and Steps](#tasks-and-steps)
   - [Task 1: Exploratory Data Analysis (EDA)](#task-1-exploratory-data-analysis-eda)
   - [Task 2: Default Estimator and WoE Binning](#task-2-default-estimator-and-woe-binning)
   - [Task 3: Feature Engineering](#task-3-feature-engineering)
4. [Model Development](#model-development)
5. [Installation Instructions](#installation-instructions)
6. [Usage](#usage)
7. [Contributing](#contributing)
8. [License](#license)

## Project Overview

Bati Bank is partnering with a successful eCommerce company to offer a buy-now-pay-later service. As part of the partnership, the bank needs to build a credit scoring model to assess the risk associated with potential borrowers. The goal is to categorize users into high-risk and low-risk groups and predict the optimal loan amount and duration.

The credit scoring model leverages transaction data, customer profiles, and various features to predict the likelihood of default and to assign credit scores to new customers.

## Data Description

The data for this project includes the following features:

- **TransactionId**: Unique transaction identifier
- **BatchId**: Unique batch number for processing
- **AccountId**: Customer’s account identifier
- **SubscriptionId**: Unique subscription identifier
- **CustomerId**: Unique identifier attached to the customer
- **CurrencyCode**: Country currency
- **CountryCode**: Geographical country code
- **ProviderId**: Source provider of the item bought
- **ProductId**: Item being bought
- **ProductCategory**: Category of the purchased product
- **ChannelId**: Customer’s usage channel (e.g., web, Android, IOS)
- **Amount**: Value of the transaction
- **Value**: Absolute value of the transaction
- **TransactionStartTime**: Timestamp of when the transaction occurred
- **PricingStrategy**: Category of Xente's pricing structure for merchants
- **FraudResult**: Indicates if the transaction is fraudulent (1 = Yes, 0 = No)
- **TransactionYear**: Year when the transaction occurred

## Tasks and Steps

### Task 1: Exploratory Data Analysis (EDA)

1. **Overview of the Data**:
   - Understand the structure of the dataset by examining the number of rows, columns, and data types.

2. **Summary Statistics**:
   - Calculate and visualize the central tendency, dispersion, and shape of the dataset’s distribution.

3. **Distribution of Numerical Features**:
   - Visualize the distribution of numerical features to identify patterns, skewness, and outliers.

4. **Encode Categorical Variables**:
   - Convert categorical variables into numerical format using techniques such as One-Hot Encoding and Label Encoding.

5. **Handle Missing Values**:
   - Impute or remove missing values from the dataset using methods such as mean, median, or mode imputation, or removal of missing rows/columns.

6. **Normalize/Standardize Numerical Features**:
   - Normalize or standardize numerical features to bring them onto a similar scale using techniques such as Min-Max scaling or Z-score standardization.

7. **Feature Engineering**:
   - Utilize tools such as [xverse](https://pypi.org/project/xverse/) and [woe](https://pypi.org/project/woe/) for weight of evidence (WoE) and information value (IV) calculations.

### Task 2: Default Estimator and WoE Binning

1. **Construct a Default Estimator (Proxy)**:
   - Visualize transactions to classify users as high-risk (bad) or low-risk (good) based on the RFMS space.

2. **Perform Weight of Evidence (WoE) Binning**:
   - Apply WoE binning to the features and compute the information value (IV) to assess feature significance.

### Task 3: Feature Engineering

1. **Create Aggregate Features**:
   - Aggregate transaction-related features such as:
     - Total Transaction Amount
     - Average Transaction Amount
     - Transaction Count
     - Standard Deviation of Transaction Amounts

2. **Extract Time-Based Features**:
   - Extract features related to transaction timing such as:
     - Transaction Hour
     - Transaction Day
     - Transaction Month

## Model Development

1. **Develop a Model to Assign Risk Probability**:
   - Train a machine learning model to predict the risk probability (likelihood of default) for a new customer based on their transaction data.

2. **Develop a Model to Assign Credit Score**:
   - Use the risk probability to assign a credit score to a customer, which quantifies their creditworthiness.

3. **Predict Optimal Loan Amount and Duration**:
   - Develop a model to predict the optimal loan amount and duration based on the customer's risk profile.

## Installation Instructions

To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Azazh/Credit-Scoring-Model.git
   cd credit-scoring-model
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure that you have the necessary libraries installed for data processing and machine learning, such as Pandas, Scikit-learn, Matplotlib, and Xverse.

## Usage

Once the setup is complete, you can start working with the dataset and the models by following the instructions in the Jupyter notebooks provided in the project.

```bash
jupyter notebook
```

Run the cells in the notebook to perform the exploratory data analysis, feature engineering, and model training.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
