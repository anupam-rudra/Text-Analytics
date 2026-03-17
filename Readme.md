# 🍽️ Amazon Fine Food Reviews - Sentiment Analysis

## 📌 Project Overview
This project performs **end-to-end text analysis and sentiment classification** on the Amazon Fine Food Reviews dataset.  
The goal is to transform raw customer reviews into meaningful insights using **Natural Language Processing (NLP)** and **Machine Learning models**.

The pipeline includes:
- Text preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering using TF-IDF
- Training multiple ML models
- Model evaluation and comparison
- Binary classification (positive vs negative)
- Confidence score estimation

---

## 📂 Dataset Description

The dataset contains customer reviews of food products from Amazon.

### 🔑 Key Columns Used:

| Column Name | Description |
|------------|------------|
| `Text`     | The actual customer review text |
| `Score`    | Rating given by the user (1 to 5) |

### 🎯 Target Creation (Sentiment)

We convert numerical ratings into sentiment categories:

- **1–2 → Negative**
- **3 → Neutral**
- **4–5 → Positive**

This allows us to frame the problem as a **classification task**.

---

## 🧹 Data Preprocessing

Raw text data is noisy and needs cleaning before modeling.

### Steps performed:
- Convert text to lowercase
- Remove special characters and punctuation
- Remove numbers
- Remove stopwords (common words like *the, is, and*)


---

## 📊 Exploratory Data Analysis (EDA)

We analyze sentiment distribution to understand class balance.

- Visualized using **count plots**
- Helps detect class imbalance issues

---

## ☁️ Word Cloud Visualization

A word cloud is generated using cleaned text to identify:

- Most frequent words
- General themes in reviews

---

## 🔧 Feature Engineering (TF-IDF)

Text data is converted into numerical form using:

### 👉 TF-IDF (Term Frequency - Inverse Document Frequency)

- Assigns importance to words based on frequency
- Reduces impact of very common words
- Creates a sparse numerical matrix

---

## ✂️ Train-Test Split

The dataset is split into:
- **80% Training Data**
- **20% Testing Data**

Stratified sampling is used to preserve class distribution.

---

## 🤖 Model Building

We train multiple machine learning models:

### 1. Logistic Regression
- Baseline linear model
- Works well for text classification

### 2. Naive Bayes
- Probabilistic model
- Very efficient for NLP tasks

### 3. Support Vector Machine (SVM)
- Effective in high-dimensional spaces
- Performs well with TF-IDF features

---

## 📈 Model Evaluation

Each model is evaluated using:

- **Accuracy Score**
- **Classification Report**
  - Precision
  - Recall
  - F1-score

A comparison table is created to identify the best model.

---

## 🏆 Best Model Selection

Based on performance, **Logistic Regression** is selected as the best model and evaluated in detail.

---

## 🔄 Binary Classification (Advanced Step)

To simplify the problem:
- Neutral reviews are removed
- Task becomes:
  - **Positive vs Negative**

This often improves performance and interpretability.

---

## 🔮 Prediction Function

A reusable function is created to:

- Accept new review text
- Clean it
- Transform using TF-IDF
- Predict sentiment

### Example usage:
```python
predict_sentiment("This product is great!", model, vectorizer)

## 📉 Confusion Matrix

A confusion matrix is used to visualize:

- True Positives  
- True Negatives  
- False Positives  
- False Negatives  

This helps in understanding how well the model is performing beyond accuracy.

---

## ❌ Error Analysis

We extract incorrectly classified reviews to:

- Understand model weaknesses  
- Identify ambiguous or misleading text  

---

## 📊 Confidence Score

The model provides probability estimates for predictions.

- Confidence score = highest predicted probability  
- Helps measure how certain the model is  

### Example:

- Prediction: Positive  
- Confidence: 0.92 → Highly confident  

---

## 🚀 Key Insights

- TF-IDF is highly effective for text classification  
- Logistic Regression performs strongly on this dataset  
- Removing neutral reviews improves binary classification performance  
- Error analysis reveals limitations in handling sarcasm and context  

---

