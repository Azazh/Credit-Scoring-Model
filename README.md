
# **Credit Scoring Model for Buy-Now-Pay-Later Service**  

This project focuses on building a **Credit Scoring Model** to assess the creditworthiness of potential borrowers for a **Buy-Now-Pay-Later (BNPL)** service. The model utilizes **transaction data** from an eCommerce platform to classify customers as **high-risk** or **low-risk**, based on their likelihood of defaulting on payments.  

The project follows a structured approach that includes **Exploratory Data Analysis (EDA), Feature Engineering, Model Development, Model Evaluation, and Deployment as an API.**  


## **Table of Contents**  

1. [Project Overview](#project-overview)  
2. [Data Description](#data-description)  
3. [Tasks and Steps](#tasks-and-steps)  
   - [Task 1: Exploratory Data Analysis (EDA)](#task-1-exploratory-data-analysis-eda)  
   - [Task 2: Default Estimator and WoE Binning](#task-2-default-estimator-and-woe-binning)  
   - [Task 3: Feature Engineering](#task-3-feature-engineering)  
   - [Task 4: Model Development and Evaluation](#task-4-model-development-and-evaluation)  
   - [Task 5: Model Deployment via API](#task-5-model-deployment-via-api)  
4. [Installation Instructions](#installation-instructions)  
5. [Usage](#usage)  
6. [Contributing](#contributing)  
7. [License](#license)  



## **Project Overview**  

### **Objective**  

Bati Bank is partnering with an eCommerce company to offer a **Buy-Now-Pay-Later (BNPL) service**. The goal is to develop a **Credit Scoring Model** that assesses customer risk levels, predicts the likelihood of **loan default**, and provides insights into **optimal loan amounts and durations**.  

### **Methodology**  

The project involves the following key steps:  
✅ Performing **Exploratory Data Analysis (EDA)** to identify trends, outliers, and missing values.  
✅ Engineering **meaningful features** to enhance predictive performance.  
✅ Training and evaluating **multiple machine learning models** for credit risk classification.  
✅ **Optimizing hyperparameters** to improve model performance.  
✅ Deploying the trained model using a **REST API** for real-time predictions.  


## **Data Description**  

The dataset consists of **customer transactions**, including details about their purchases, accounts, and historical behaviors. Key features include:  

- **TransactionId**: Unique identifier for each transaction  
- **BatchId**: Processing batch number  
- **AccountId**: Customer’s account identifier  
- **CustomerId**: Unique identifier for each customer  
- **CurrencyCode**: Currency type for the transaction  
- **CountryCode**: Country where the transaction occurred  
- **ProviderId**: Provider of the purchased item  
- **ProductCategory**: Category of the purchased item  
- **ChannelId**: Customer’s usage channel (e.g., Web, Android, iOS)  
- **Amount**: Value of the transaction  
- **TransactionStartTime**: Timestamp of when the transaction occurred  
- **FraudResult**: Binary label indicating whether the transaction was fraudulent (1 = Fraudulent, 0 = Non-Fraudulent)  

The dataset is processed to handle **missing values, categorical encoding, and scaling** before feeding it into the machine learning models.  


## **Tasks and Steps**  

### **Task 1: Exploratory Data Analysis (EDA)**  

📌 **Data Overview & Cleaning**:  
- Checking dataset shape, missing values, and duplicates  
- Handling missing values via imputation techniques  

📌 **Statistical Analysis**:  
- Summary statistics (mean, median, standard deviation)  
- Identifying outliers using boxplots  

📌 **Data Visualization**:  
- Distribution plots for numerical variables  
- Fraud detection analysis through correlation matrices  
- Feature importance analysis  

📌 **Data Preprocessing**:  
- Encoding categorical features  
- Standardizing numerical features using Min-Max Scaling  



### **Task 2: Default Estimator and WoE Binning**  

📌 **Default Estimator (Proxy Labeling)**:  
- Classifying users as **high-risk or low-risk** based on transaction patterns  

📌 **Weight of Evidence (WoE) & Information Value (IV)**:  
- **WoE Transformation**: Converting categorical variables into numerical representations  
- **IV Calculation**: Identifying the most significant predictors for credit risk  



### **Task 3: Feature Engineering**  

📌 **Aggregate Features**:  
- Total transaction amount  
- Average transaction amount per user  
- Number of transactions per user  

📌 **Time-Based Features**:  
- Hour of the day transactions occur  
- Day of the week transactions occur  

📌 **Behavioral Features**:  
- Frequency of high-value transactions  
- Ratio of fraud to non-fraud transactions  



### **Task 4: Model Development and Evaluation**  

📌 **Train-Test Split**:  
- Splitting data into **training and testing sets**  

📌 **Model Selection**:  
- Comparing different machine learning models:  
  - ✅ Logistic Regression  
  - ✅ Decision Trees  
  - ✅ Random Forest  
  - ✅ Gradient Boosting Machines (GBM)  

📌 **Hyperparameter Tuning**:  
- Using **Grid Search** and **Random Search** for optimization  

📌 **Model Evaluation Metrics**:  
- **Accuracy**: Measures correct classifications  
- **Precision**: Identifies the proportion of correctly predicted positive cases  
- **Recall (Sensitivity)**: Measures how well the model detects actual positive cases  
- **F1 Score**: Balances precision and recall  
- **ROC-AUC**: Assesses the model’s ability to distinguish between classes  



### **Task 5: Model Deployment via API**  

📌 **REST API Development**:  
- Using **FastAPI / Flask** to create a web-based API  

📌 **Model Integration**:  
- Loading the trained model into the API backend  

📌 **API Endpoints**:  
- **POST /predict**: Accepts customer transaction details and returns a risk classification  

📌 **Deployment Options**:  
- Cloud hosting using **AWS, GCP, or Heroku**  



## **Installation Instructions**  

To set up the project locally, follow these steps:  

1️⃣ **Clone the repository**:  
   ```bash
   git clone https://github.com/Azazh/Credit-Scoring-Model.git
   cd credit-scoring-model
   ```  

2️⃣ **Install dependencies**:  
   ```bash
   pip install -r requirements.txt
   ```  

3️⃣ **Run the Jupyter Notebook for EDA & Model Training**:  
   ```bash
   jupyter notebook
   ```  

4️⃣ **Start the API Server**:  
   ```bash
   python api.py
   ```  



## **Usage**  

📌 **Running Exploratory Data Analysis (EDA)**  
- Open `EDA.ipynb` and execute cells for visualization and preprocessing  

📌 **Training Machine Learning Models**  
- Run `model_training.ipynb` to train and evaluate models  

📌 **Deploying the Model via API**  
- Start the API server with `python api.py`  
- Use **Postman** or **cURL** to test the API endpoints  

Example API call:  
```bash
curl -X POST "http://localhost:5000/predict" -H "Content-Type: application/json" -d '{"Amount": 1000, "ProductCategory": "Electronics"}'
```



## **Contributing**  

Contributions are welcome! If you find issues or want to improve the model, feel free to submit a **pull request**.  



## **License**  

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.  

