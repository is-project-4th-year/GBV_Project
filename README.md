
---

# **SpeakSafe – GBV Detection System with Explainable AI System**

**Final Year Project (2025)**

Author: **sharly.misati@strathmore.edu**

---

## **Overview**

**SpeakSafe** is an explainable machine learning system designed to detect **Gender-Based Violence (GBV)** in online text. It analyzes tweets, user-submitted text, and scraped content to identify harmful patterns across **five GBV categories**:

1. **Sexual Violence**
2. **Physical Violence**
3. **Emotional / Psychological Abuse**
4. **Economic Violence**
5. **Harmful Traditional Practices**

The system combines:

* **TweetNLP Transformer Model (HuggingFace)**
* **Multinomial Naïve Bayes (TF-IDF features)**
* **Soft-Voting Hybrid Ensemble**
* **LIME Explainability** for token-level highlights

SpeakSafe also recommends **Kenyan and UN GBV resources**, including hotlines, support centers, and emergency contacts.

---

## **Key Features**

### **Hybrid Ensemble Model**

* TweetNLP embedding-based classifier
* Naïve Bayes statistical classifier
* Probability-level soft voting

### **Explainability**

* LIME highlight visualization
* Shows keywords that influenced the prediction
* Per-category contribution breakdown

### **Data Inputs**

* Manual text input
* Tweet URL scraping using Twitter API
* Automatic preprocessing & cleaning

### **Secure Authentication**

* Firebase Authentication (Email/Password)

### **Support Resource Panel**

Automatically recommends **Kenyan hotlines**, **GBV centers**, and **UN resources** based on detected category.

---

## **Project Structure**

```
GBV_PROJECT/
├── app.py
├── preprocess.py
├── lime_functions.py
├── shap_utils.py
├── config.yaml
├── requirements.txt
├── README.md
├── assets/images/
│   ├── login.png
│   ├── dashboard.png
│   └── explanations.png
├── models/
│   ├── naive_bayes_model.joblib
│   ├── tfidf_vectorizer.joblib
│   └── tweetnlp/
├── GBV_Model.ipynb
├── GBV_RNN.ipynb
├── GBV_Deep_Neural_Networks.ipynb
└── .streamlit/
    └── secrets.toml
```

---

## **Model Performance (Summary)**

| Metric    | Score |
| --------- | ----- |
| Accuracy  | ~0.87 |
| Precision | ~0.84 |
| Recall    | ~0.86 |
| F1-Score  | ~0.85 |


### **Category-Level Highlights**

* Emotional abuse: highest recall
* Economic violence: hardest to detect due to subtle wording
* Sexual & physical violence: strongest overall precision

---

## **Running the App**

### **1️ Install dependencies**

```
pip install -r requirements.txt
```

### **2️ Set Firebase credentials**

Place the Firebase admin JSON inside the project and configure `.streamlit/secrets.toml`.

### **3️ Start the app**

```
streamlit run app.py
```

---

## **Support Resources**

### **🇰🇪 Kenya**

* **Emergency Police:** 999 / 112
* **National GBV Hotline:** 1195
* **Childline Kenya:** 116
* **GVRC – Nairobi Women’s Hospital**
* **HAK Toll-Free:** 0800-720-186

### **Global**

* **UN Women GBV Helpdesk**
* **UNFPA Safe Spaces Network**
* **UNHCR GBV Protection Services**

---

## **Technologies Used**

* **Python 3.9**
* **TweetNLP Transformer Model**
* **Scikit-Learn (Naïve Bayes, TF-IDF)**
* **LIME Explainability**
* **Streamlit**
* **Firebase Admin SDK**
* **Twitter API v2**

---

## **Future Enhancements**

* Add **Swahili language model**
* Mobile app (Android/iOS)
* Real-time Chrome extension
* Larger GBV dataset for improved minority class performance

---

## **License**

This project is licensed under the MIT License. Refer the **LICENSE** file for details.

---
