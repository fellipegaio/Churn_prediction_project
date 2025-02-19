# Customer Churn Prediction

## 📌 Project Overview  

This project focuses on predicting **customer churn** for a telecommunications provider. The goal is to **identify customers at risk of leaving** so the company can offer them promotional incentives and improve retention.  

The dataset includes information on **customer contracts, personal details, internet and phone services, and payment methods**. Using **machine learning models**, we aim to uncover patterns in customer behaviour and provide actionable insights.  

---

## 🏢 Business Context  

The telecom company provides **landline telephony and internet services**, offering both DSL and fiber optic connections. Additional services include:  

- **Internet security** (*DeviceProtection*, *OnlineSecurity*)  
- **Technical support** (*TechSupport*)  
- **Cloud storage** (*OnlineBackup*)  
- **Entertainment** (*StreamingTV*, *StreamingMovies*)  

Customers can choose between **monthly, 1-year, or 2-year contracts** with different payment methods. The challenge is to analyze **which factors contribute to customer churn** and build a reliable predictive model.  

---

## 📊 Dataset  

The dataset consists of **four CSV files**, each containing different aspects of customer data:  

- `contract.csv` – Contract details (start & end dates, payment type, etc.)  
- `personal.csv` – Customer demographics  
- `internet.csv` – Internet service details  
- `phone.csv` – Telephony service details  

All files are linked by a unique **`customerID`**, and the churn status is determined by **contract end dates**.  

---

## 🚀 Approach  

### **1️⃣ Data Preparation**  
✔ Merged all datasets into a **single DataFrame**  
✔ Standardized column names & adjusted data types  
✔ Converted categorical variables into numerical features  
✔ Handled missing values using **IterativeImputer**  

### **2️⃣ Exploratory Data Analysis (EDA)**  
✔ Identified key churn indicators  
✔ Created new features (e.g., **contract duration**)  
✔ Visualized **correlations & customer trends**  

### **3️⃣ Model Training & Evaluation**  
✔ Split data into **training (75%) and testing (25%)** sets  
✔ Trained **Random Forest, CatBoost, and LightGBM** models  
✔ Tuned hyperparameters using **GridSearchCV**  
✔ Evaluated models using **AUC-ROC & Accuracy**  

---

## 🏆 Model Results  

| Model           | AUC-ROC | Accuracy |
|----------------|---------|----------|
| **Random Forest** | 0.86 | 0.80 |
| **CatBoost** | 0.86 | 0.74 |
| **LightGBM** | 0.86 | 0.80 |

💡 **Why LightGBM?**  
- **Same AUC-ROC as other models**, but more computationally efficient  
- **Handles large datasets well** and is faster than Random Forest  
- **Balances performance & scalability**, making it the best choice  

---

## 🔑 Key Insights  

- **Who is most likely to churn?**  
  ✅ **Senior citizens (83.7%)**  
  ✅ **Customers with month-to-month contracts (55%)**  
  ✅ **Users without additional services (51-71%)**  

- **Contract length matters** – shorter contracts (≤ 10 months) have a higher churn rate  
- **Additional services reduce churn** – customers with **OnlineSecurity, TechSupport, or StreamingTV** are more likely to stay  

---

## 🛠 Tech Stack  

- **Programming**: Python (`pandas`, `numpy`, `scikit-learn`)  
- **Machine Learning**: `RandomForestClassifier`, `GradientBoostingClassifier`, `CatBoostClassifier`, `LightGBM`  
- **Feature Engineering**: `IterativeImputer`, `GridSearchCV`  
- **Visualization**: `matplotlib`, `seaborn`  

---

## 🤝 Contributions & Feedback  

If you have suggestions or improvements, feel free to reach out!  

📩 Contact: ofellipegaio@gmail.com | LinkedIn: https://www.linkedin.com/in/fellipegaio  
