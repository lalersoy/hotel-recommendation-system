# Hotel Recommendation System

This project builds a **hotel recommendation system** using **sentiment analysis** and **TF-IDF-based text processing**. It utilizes hotel reviews from TripAdvisor to analyze customer sentiments and recommend the best hotels based on user preferences.

---

## Project Structure
```
/hotel-recommendation-system
│── /code                 # Contains the Jupyter Notebook
│   ├── recommendation-tool.ipynb  # Main notebook with sentiment analysis & recommendations
│── README.md             # Project documentation
```

---

## Setup Instructions

Before running the notebook, ensure you have the dataset in the correct location.

1. **Download the dataset** from **[Carnegie Mellon University (CMU)](https://www.cs.cmu.edu/~jiweil/html/hotel-review.html)**.
2. **Place the files (`reviews.csv` and `offerings.csv`) in a folder.**  
3. **Update the file path** in the code:
   ```python
   reviews = pd.read_csv("/path/to/data/reviews.csv")
   offerings = pd.read_csv("/path/to/data/offerings.csv")
   ```
4. **FastText Language Detection Model:**
   - The script automatically downloads **`lid.176.bin`**, which is used for language detection.
   - If you face issues, manually download it from **[this link](https://dl.fbaipublicfiles.com/fasttext/supervised-models/lid.176.bin)** and place it in the same directory as your notebook.

## Preprocessing
- **Preprocessing Steps:**
  - Tokenization, Lemmatization, and Stopword Removal
  - Language Filtering using `fastText`
  - Sentiment Scoring with `VADER`
  - Feature Extraction using **TF-IDF**

---

## Sentiment Analysis
- **VADER Sentiment Analysis** assigns a sentiment score to each review.
- We analyze the **correlation between sentiment scores and user ratings**.
- Word clouds visualize **positive and negative sentiment keywords**.

---

## Recommendation System
- **User Query:** The system recommends hotels based on **textual similarity**.
- **TF-IDF Vectorization:** Converts user input and reviews into numerical vectors.
- **Cosine Similarity:** Finds the most relevant reviews and hotel names.

---

## Requirements
- Python 3.8+
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `nltk` (for sentiment analysis)
- `scikit-learn` (for TF-IDF & similarity calculations)
- `fastText` (for language detection)
- `wordcloud` (for visualization)

To install all dependencies:
```bash
!pip install pandas numpy matplotlib seaborn nltk scikit-learn fasttext wordcloud
```

---

### Author 
Deniz Lal Ersoy
**[GitHub Repo](https://github.com/lalersoy/hotel-recommendation-system)**  

---

