# 📰 Fake News Detection Using NLP

This project focuses on detecting fake news articles using Natural Language Processing (NLP) techniques and machine learning. It leverages a Support Vector Classifier (SVC) trained on TF-IDF features to classify news as **real** or **fake** with over 99% accuracy.

---

## 📁 Files in the Repository

- `fake_news_detection_using_NLP.ipynb` - Main Jupyter notebook with code for preprocessing, vectorization, and classification.
- `summary_of_project.pdf` - Summary of methodology and key results.

---


### 🔗 Download Datasets

[![Download Fake.csv](https://img.shields.io/badge/Download-Fake.csv-brightgreen?style=for-the-badge)](https://drive.google.com/file/d/1mQ4VDZz3d1zNhVx8IXGn0SMnQ9CYRKG9/view?usp=sharing)

[![Download True.csv](https://img.shields.io/badge/Download-True.csv-brightgreen?style=for-the-badge)](https://drive.google.com/file/d/1C7BMGva3V5KXVyxv7u3HbTPH_9r8RcYX/view?usp=sharing)

> ⚠️ Please download both files and place them in the root directory of the project before running the notebook.



## 🧠 Project Workflow

### 🔹 1. Data Collection
- Two datasets: `Fake.csv` (23,481 samples) and `True.csv` (21,417 samples).
- Each has `title`, `text`, `subject`, and `date` columns.

### 🔹 2. Text Preprocessing
- Combined `title` and `text` into a single content field.
- Converted text to lowercase.
- Removed digits, punctuation, and stopwords.
- Tokenized and lemmatized using NLTK.

### 🔹 3. Feature Engineering
- Transformed text data using **TF-IDF Vectorizer**.
- Limited vocabulary to the top 5000 most frequent terms.
- Split into 80% training and 20% testing sets.

### 🔹 4. Model Training
- Trained a **Support Vector Classifier (SVC)** with a linear kernel on the training data.
- Achieved strong performance on the test data.

---

## 📊 Model Performance

| Metric      | Score    |
|-------------|----------|
| Accuracy    | 99.44%   |
| Precision   | 99.56%   |
| Recall      | 99.39%   |
| F1-Score    | 99.47%   |

- Confusion Matrix:
  - **True Positives (Fake predicted correctly):** 4704
  - **True Negatives (True predicted correctly):** 4226
  - **False Positives (True → Fake):** 21
  - **False Negatives (Fake → True):** 29

---

## 📌 Key Insights

- The model performs with near-perfect accuracy, demonstrating the power of TF-IDF features and SVC in NLP classification tasks.
- Very few misclassifications show strong generalization across the dataset.
- Next steps could involve:
  - Feature importance analysis
  - Testing on external datasets
  - Deploying the model using Flask/Streamlit

---

## 🚀 How to Run This Project

1. Clone the repository:
   ```bash
   git clone [https://github.com/vishnuvsh321/fake-news-detection-using-NLP]
