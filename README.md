# 🎬 CINEMA.IO
**Multi-Emotion Movie Recommendation — Data & Interface Engineering**

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](#)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2C2D72?logo=pandas&logoColor=white)](https://pandas.pydata.org/)

> **Short Summary:** An end-to-end NLP movie recommendation system that reads a user's free-form emotional statement, classifies it into one of 6 core emotions using a fine-tuned DistilBERT model, and matches it against an emotion-labeled IMDb Top 1000 catalog. My contribution focused heavily on pipeline-ready data engineering (GoEmotions & IMDb datasets) and designing the web application's user interface.

---

### 📌 Project Properties
- **Author:** David Christian Golden Mahaviro
- **Context:** Group Class Assignment – NLP Final Project (BINUS University, 2026)
- **Role:** Data Preprocessing Engineer & Frontend/UI Developer
- **Tech Stack:** Python, Pandas, Streamlit
- **Links:** [View Web App](#) | [Watch Video Demo](#) <!-- Replace '#' with actual links -->

---

### 📖 Project Context
Cinema.io matches users' emotional statements with movie synopses using a fine-tuned DistilBERT classifier and TF-IDF + Cosine Similarity. While other team members focused on model architecture (SVM, BiLSTM, BERT-Base) and the core recommendation engine, I took charge of the **Data Preprocessing & Frontend Development**. 

My scope of work included:
1. Cleaning and restructuring two massive raw datasets (GoEmotions & IMDb Top 1000) to be used for the training and self-labeling stages.
2. Designing and building the interactive web application interface.

---

### ⚙️ Methodology & Problem Solving

Raw datasets from real-world sources (Reddit, IMDb) are rarely pipeline-ready. They contained messy structures, irrelevant columns, and missing values that threatened downstream model quality.

- **Emotion Table (GoEmotions):** Merged three raw Reddit comment files and filtered 27 original emotion labels down to **6 core emotions** (Joy, Love, Surprise, Anger, Fear, Sadness) using a strict priority rule for multi-label rows. Irrelevant metadata columns were dropped, producing a clean, unambiguous dataset (`goemotions_kasar_pure.csv`) ready for text-cleaning.
- **Movie Table (IMDb Top 1000):** Trimmed dozens of metadata columns down to the 3 essential features required for the recommendation engine: `title`, `genre`, and `overview`. Rows with missing synopses were removed, resulting in a lean dataset (`film_kasar.csv`) for the self-labeling stage.
- **Web Interface:** Engineered a responsive, glassmorphic UI using Streamlit to seamlessly display emotion classification results alongside interactive movie recommendation cards.

---

### 🚀 Impact & Lessons Learned

- **Pipeline Foundation:** The datasets I prepared served as the absolute starting point for the entire NLP pipeline, significantly speeding up the team's self-labeling and TF-IDF vector space construction.
- **Label Reduction Mastery:** Transforming 27 labels into 6 core classes taught me the importance of consistent priority rules in resolving multi-label conflicts and preventing ambiguous training data.
- **End-to-End Vision:** Building the UI myself reinforced how critical it is to understand backend model outputs, ensuring the frontend accurately represents the underlying data to the end user.

---

### 💻 Setup & Installation

To run the Cinema.io web interface locally:

**1. Clone the repository**
```bash
git clone [https://github.com/davidhoky/YOUR-REPO-NAME.git](https://github.com/davidhoky/YOUR-REPO-NAME.git)
cd YOUR-REPO-NAME
