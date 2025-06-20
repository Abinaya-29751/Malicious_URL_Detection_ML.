# Malicious URL Detection System using Machine Learning

## Introduction

The Internet has become an essential part of daily life, but with its convenience comes risks—specifically the spread of malicious URLs designed to perform phishing, malware delivery, identity theft, and fraud. Traditional URL detection methods like blacklists and manual checks are ineffective against evolving threats. This project uses Machine Learning to develop a system that automatically detects malicious URLs by analyzing their lexical and structural properties.

---

##  Problem Statement

The goal is to build an accurate and efficient ML model that:

1. Extracts meaningful features from URLs.
2. Classifies URLs into **Benign** or **Malicious**.
3. Provides real-time prediction capability.
4. Minimizes false positives and maximizes detection accuracy.

---

##  Dataset

- **Source:** Kaggle ([Malicious and Benign URLs](https://www.kaggle.com/datasets/mishra5001/malicious-and-benign-urls))
- **File Used:** `urldata.csv`
- **Labels:** 
  - `benign` (0)
  - `malicious` (1)

---

## Features Extracted

| Feature Name          | Description                                         |
|----------------------|-----------------------------------------------------|
| URL Length           | Total characters in the URL.                        |
| Number of Digits     | Total digits present in the URL.                    |
| Number of Special Characters | Total non-alphanumeric symbols.          |
| IP Address Presence  | 1 if URL contains an IP address, else 0.            |
| Number of Subdomains | Total dots ('.') in the URL indicating subdomains.  |
| HTTPS Presence       | 1 if URL uses HTTPS, else 0.                        |
| '@' Symbol Presence  | 1 if URL contains '@', else 0.                      |
| Number of Query Parameters | Count of '?' and '&' symbols.                |

---

##  Technologies Used

- **Python Libraries:** 
  - Pandas, Numpy, scikit-learn, XGBoost, imbalanced-learn (SMOTE), Matplotlib, Seaborn
- **Algorithms:**
  - Random Forest Classifier
  - XGBoost Classifier
- **Imbalanced Data Handling:**
  - SMOTE (Synthetic Minority Over-sampling Technique)

---

##  Model Training & Evaluation

- **Train/Test Split:** 80% / 20%
- **Evaluation Metrics:**
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - Confusion Matrix (Visualized using Seaborn Heatmaps)

---

##  Model Performance

| Model              | Accuracy |
|-------------------|----------|
| Random Forest      | ~ (as per execution) |
| XGBoost Classifier | ~ (as per execution) |

Confusion matrices for both models are displayed to visualize prediction performance.

---

##  How to Run Locally

### 1. Clone the Repository:

```bash
git clone https://github.com/yourusername/Malicious_URL_Detection_ML.git
cd Malicious_URL_Detection_ML

Install Required Libraries:

pip install -r requirements.txt

Run the Python Script:

python malicious_url_detection.py
