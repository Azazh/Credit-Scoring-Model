Here's your updated README file with **Task 4 - Modelling** and **Task 5 - Model Serving API Call** included.  

---

# Credit Scoring Model for Buy-Now-Pay-Later Service  

This project is focused on building a **Credit Scoring Model** to assess the creditworthiness of potential borrowers for a **buy-now-pay-later (BNPL)** service. The model uses transaction data provided by an eCommerce platform to classify customers as **high-risk** or **low-risk** based on their likelihood of defaulting on payments. The solution involves **exploratory data analysis (EDA)**, **feature engineering**, **model development**, and **risk prediction**.  

## Table of Contents  

1. [Project Overview](#project-overview)  
2. [Data Description](#data-description)  
3. [Tasks and Steps](#tasks-and-steps)  
   - [Task 1: Exploratory Data Analysis (EDA)](#task-1-exploratory-data-analysis-eda)  
   - [Task 2: Default Estimator and WoE Binning](#task-2-default-estimator-and-woe-binning)  
   - [Task 3: Feature Engineering](#task-3-feature-engineering)  
   - [Task 4: Modelling](#task-4-modelling)  
   - [Task 5: Model Serving API Call](#task-5-model-serving-api-call)  
4. [Installation Instructions](#installation-instructions)  
5. [Usage](#usage)  
6. [Contributing](#contributing)  
7. [License](#license)  

## Project Overview  

Bati Bank is partnering with a successful eCommerce company to offer a **buy-now-pay-later (BNPL)** service. As part of the partnership, the bank needs to build a **credit scoring model** to assess the risk associated with potential borrowers. The goal is to categorize users into **high-risk** and **low-risk** groups and predict the optimal **loan amount** and **duration**.  

The credit scoring model leverages **transaction data, customer profiles**, and various features to predict the **likelihood of default** and to assign **credit scores** to new customers.  

## Data Description  

The dataset includes:  

- **TransactionId**: Unique transaction identifier  
- **BatchId**: Unique batch number for processing  
- **AccountId**: Customer’s account identifier  
- **SubscriptionId**: Unique subscription identifier  
- **CustomerId**: Unique customer identifier  
- **CurrencyCode**: Country currency  
- **CountryCode**: Geographical country code  
- **ProviderId**: Source provider of the item bought  
- **ProductId**: Item being bought  
- **ProductCategory**: Category of the purchased product  
- **ChannelId**: Customer’s usage channel (e.g., web, Android, IOS)  
- **Amount**: Value of the transaction  
- **TransactionStartTime**: Timestamp of when the transaction occurred  
- **PricingStrategy**: Category of Xente's pricing structure for merchants  
- **FraudResult**: Indicates if the transaction is fraudulent (1 = Yes, 0 = No)  
- **TransactionYear**: Year when the transaction occurred  

## Tasks and Steps  

### Task 1: Exploratory Data Analysis (EDA)  

1. **Overview of the Data**  
2. **Summary Statistics**  
3. **Distribution of Numerical Features**  
4. **Encode Categorical Variables**  
5. **Handle Missing Values**  
6. **Normalize/Standardize Numerical Features**  
7. **Feature Engineering (e.g., WoE and IV calculations)**  

### Task 2: Default Estimator and WoE Binning  

1. **Construct a Default Estimator (Proxy)**
2. **Perform Weight of Evidence (WoE) Binning**  

### Task 3: Feature Engineering  

1. **Create Aggregate Features (e.g., Total Transaction Amount, Count, Std Dev)**  
2. **Extract Time-Based Features (e.g., Hour, Day, Month)**  

### Task 4: Modelling  

1. **Split the Data**  
   - Splitting the dataset into **training** and **testing** sets for model evaluation.  

2. **Choose Models**  
   - Select at least two of the following models:  
     - **Logistic Regression**  
     - **Decision Trees**  
     - **Random Forest**  
     - **Gradient Boosting Machines (GBM)**  

3. **Train the Models**  
   - Train the selected models on the **training dataset**.  

4. **Hyperparameter Tuning**  
   - Improve model performance using techniques like:  
     - **Grid Search**  
     - **Random Search**  

5. **Model Evaluation**  
   - Evaluate models using the following performance metrics:  
     - **Accuracy**: Measures overall correctness.  
     - **Precision**: Measures how many predicted positives were actually positive.  
     - **Recall (Sensitivity)**: Measures how many actual positives were predicted correctly.  
     - **F1 Score**: A balance between precision and recall.  
     - **ROC-AUC**: Measures model ability to distinguish between classes.  

### Task 5: Model Serving API Call  

1. **Create a REST API**  
   - Develop an API to serve the trained machine-learning model for real-time predictions.  

2. **Choose a Framework**  
   - Select a suitable framework for building REST APIs (e.g., **Flask, FastAPI, Django REST Framework**).  

3. **Load the Model**  
   - Load the trained model from **Task 4**.  

4. **Define API Endpoints**  
   - Create API endpoints that accept **input data** and return **predictions**.  

5. **Handle API Requests**  
   - Implement logic to:  
     - Receive input data.  
     - Preprocess it.  
     - Make predictions using the model.  

6. **Return Predictions**  
   - Format and return the predicted results as an API response.  

7. **Deploy the API**  
   - Deploy the API on a **web server or cloud platform** for real-time usage.  

---

## Installation Instructions  

To run this project locally:  

1. Clone the repository:  

   ```bash
   git clone https://github.com/Azazh/Credit-Scoring-Model.git
   cd credit-scoring-model
   ```

2. Install dependencies:  

   ```bash
   pip install -r requirements.txt
   ```

3. Ensure required libraries are installed (e.g., **Pandas, Scikit-learn, Flask/FastAPI**).  

---

## Usage  

After setup, you can start working with the dataset and the models by running:  

```bash
jupyter notebook
```

To start the API server (Flask example):  

```bash
python app.py
```

---

## Contributing  

Contributions are welcome! Feel free to submit a **pull request** or open an **issue** for improvements.  

---

## License  

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.  

---
