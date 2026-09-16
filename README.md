# 📩 Spam Message Detection Pipeline

Detecting whether a message is **Spam** or **Not Spam** by combining distance-based, margin-based, and probability-based machine learning models.

---

## 🛠️ Built With

- **Python**
- **Pandas / NumPy** – data handling
- **Matplotlib / Seaborn** – visualization
- **Scikit-learn** – KNN, SVM, Naive Bayes, evaluation metrics
- **Jupyter Notebook** – development environment

---

## 🧭 What's Inside This Project

This project explores a communication-security style problem: given a set of numeric signals extracted from a message (length, keyword scores, sender behavior, timing, etc.), predict whether it's spam.

Three different modeling philosophies are compared side by side:

- **K-Nearest Neighbors** – classifies based on similarity to nearby messages
- **Support Vector Machine** – finds the cleanest possible boundary between classes
- **Naive Bayes** – reasons purely in terms of probability, including a hand-worked demonstration of Bayes' Theorem

---

## 🔄 Pipeline Summary

1. Explore the dataset and visualize feature distributions and correlations
2. Convert the raw timestamp into usable numeric signals (month, weekend flag)
3. Clean up unnecessary columns and handle missing values
4. Split into train/test sets and scale features (fit only on training data)
5. Train and tune KNN, experimenting with K values and distance metrics
6. Train SVM with Linear and RBF kernels, and examine support vectors
7. Train Naive Bayes and manually verify its probability calculation using Bayes' Theorem
8. Compare all models on Accuracy, Precision, Recall, and F1 Score
9. Recommend the best model for deployment

---

## 📊 Dataset

Each row represents one message, described using signals such as:

- Text-derived stats: message length, word count, special characters, digits, URLs
- Keyword scores indicating spam-like or legitimate-like wording
- Sender behavior: activity score, account age, recent message volume
- Time-based signals: hour of day, day of week
- **Label:** `spam_label` (0 = Not Spam, 1 = Spam)

---

## 📈 Outcome

All three models are evaluated on an identical held-out test set. Final model selection is based on the highest overall F1 Score, since it balances catching real spam against not wrongly flagging genuine messages.

---

## 📂 Where to Find Things

| File | Path |
|---|---|
| Notebook | [`Notebook/Spam_Detection_Pipeline.ipynb`](./Notebook/Spam_Detection_Pipeline.ipynb) |
| Dataset | [`Dataset/Message_Intelligence_Dataset.csv`](./Dataset/Message_Intelligence_Dataset.csv) |
| Theory / Concepts | [`Theory_PDF/Theory.pdf`](./Theory_PDF/Theory.pdf) |

```
Spam-Detection-Pipeline/
│
├── Dataset/
│   └── Message_Intelligence_Dataset.csv
│
├── Notebook/
│   └── Spam_Detection_Pipeline.ipynb
│
├── Docs/
│   └── Theory.pdf
│
└── README.md
```

---

## ▶️ Running It Locally

```bash
git clone <repo-url>
cd Spam-Detection-Pipeline
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook Notebook/Spam_Detection_Pipeline.ipynb
```

---

## 🙋 AD MEET

Built as part of an AI/ML & Data Science coursework project.
