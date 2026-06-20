# 📰 Fact Filter

> To develop a fake news detection system using NLP techniques that automatically classifies news articles as real or fake.

---

## 🧠 Overview

Fact Filter is an NLP-based machine learning project that detects whether a given news article is **real or fake**. It uses text preprocessing, TF-IDF vectorization, and multiple classification algorithms to achieve over **99% accuracy** on a balanced news dataset.

---

## 📁 Dataset

- Source: [Fake News Detection Datasets – Kaggle](https://www.kaggle.com/datasets/emineyetm/fake-news-detection-datasets)
- Two CSV files: `True.csv` and `Fake.csv`
- Approximately **balanced dataset** (~44,000 articles total)

---

## ⚙️ Approach

### 1. Data Preprocessing (NLP)
- Combined `title` and `text` fields into a single feature column
- Applied **tokenization**, **stopword removal**, **stemming**, and **lemmatization** using NLTK
- Visualized most frequent words using **Word Cloud**

### 2. Feature Extraction – TF-IDF
- Used `TfidfVectorizer` with **top 5000 features**
- Captures word importance relative to the entire corpus
- Converted text into numerical vectors for model input

### 3. Model Training & Comparison
Trained and evaluated multiple classifiers:

| Model | Accuracy |
|---|---|
| LinearSVC | **99.33%** |
| Random Forest | 99.71% |
| Logistic Regression | 98.70% |
| Decision Tree | 99.53% |
| Gradient Boosting | 99.60% |

75/25 train-test split with `random_state=5`

---

## 📊 Results

- **LinearSVC** achieved the best balance of speed and accuracy at **99.33%**, making it the most practical model for deployment.
- All models exceeded **98.7% accuracy**, confirming that TF-IDF combined with classical ML generalizes exceptionally well for fake news detection.

---

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** pandas, numpy, scikit-learn, NLTK, matplotlib, seaborn, WordCloud
- **Environment:** Google Colab / Jupyter Notebook

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/fact-filter.git
   cd fact-filter
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the dataset from Kaggle and place it in the project directory.

4. Open and run the notebook:
   ```bash
   jupyter notebook Fact_Filter.ipynb
   ```

---

## 📌 Project Structure

```
fact-filter/
│
├── Fact_Filter.ipynb       # Main notebook
├── README.md               # Project documentation
└── requirements.txt        # Dependencies
```

---

## 🙌 Acknowledgements

- Dataset by [Emine Yetim on Kaggle](https://www.kaggle.com/datasets/emineyetm/fake-news-detection-datasets)
- NLTK for NLP utilities
- scikit-learn for ML models
