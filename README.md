# 🕵️ Fake Job Posting Detection using NLP

A beginner-friendly **Natural Language Processing (NLP)** project that detects whether a job posting is **REAL or FAKE** using Machine Learning.

---

## 📌 Overview

Fraudulent job postings are a growing problem on the internet — they trick job seekers into sharing personal data or paying fake fees. This project uses NLP techniques to automatically classify job postings as **real** or **fake** based on their text content.

---

## 📊 Dataset

- **Source:** [Fake Job Postings Dataset – Kaggle](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)
- **Size:** 17,880 job postings
- **Real jobs:** 17,014
- **Fake jobs:** 866
- **Features used:** title, company_profile, description, requirements, benefits

---

## 🛠️ Tech Stack

| Category | Tool |
|----------|------|
| Language | Python 3 |
| NLP | TF-IDF Vectorization |
| ML Model | Logistic Regression |
| Libraries | pandas, numpy, scikit-learn, matplotlib, seaborn, wordcloud |
| Platform | Google Colab / Jupyter Notebook |

---

## 🚀 How to Run

### ✅ Option 1 — Google Colab (Recommended for Beginners)

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Upload Notebook** → upload `fake_job_detection.ipynb`
3. Upload `fake_job_postings.csv` using the 📁 folder icon on the left sidebar
4. Click **Runtime → Run All**
5. Done! ✅

### 💻 Option 2 — VS Code / Local

```bash
# Step 1: Clone the repo
git clone https://github.com/YourUsername/fake-job-detection.git
cd fake-job-detection

# Step 2: Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn wordcloud

# Step 3: Open the notebook
jupyter notebook fake_job_detection.ipynb
```

---

## 📁 Project Structure

```
fake-job-detection/
│
├── fake_job_detection.ipynb   ← Main notebook (run this)
├── fake_job_postings.csv      ← Dataset
├── README.md                  ← You are here
```

---

## 🔍 Project Workflow

```
Load Dataset → Explore Data → Clean Text → TF-IDF → Train Model → Evaluate → Predict
```

1. **Load Data** — Read 17,880 job postings
2. **EDA** — Visualize real vs fake distribution
3. **Text Cleaning** — Combine title + description + requirements into one text
4. **WordCloud** — See common words in fake vs real jobs
5. **TF-IDF** — Convert text to numerical features (5000 features)
6. **Train** — Logistic Regression model (80/20 split)
7. **Evaluate** — Accuracy, Precision, Recall, F1, Confusion Matrix
8. **Predict** — Test with any custom job posting

---

## 📈 Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | ~97–98% |
| Precision | High |
| Recall | High |
| F1-Score | High |

---

## 🎯 Sample Prediction

```python
predict_job(
    title="Work From Home Make Money Fast",
    description="Earn $5000/week! No experience needed. Send your bank details now!",
)
# Output: 🚨 FAKE JOB — Confidence: 94.3%

predict_job(
    title="Software Engineer",
    description="Join our team at Google. Work on scalable backend systems.",
    requirements="3+ years Python. Strong DSA knowledge.",
)
# Output: ✅ REAL JOB — Confidence: 97.1%
```

---

## ⚠️ Disclaimer

This project is for **educational purposes only**. Always verify job postings through official company websites before applying.

---

## 🙋 Author

**Your Name**  
B.Tech CSE | [LinkedIn](https://linkedin.com) | [GitHub](https://github.com)

---

## 📄 License

This project is open source under the [MIT License](LICENSE).
