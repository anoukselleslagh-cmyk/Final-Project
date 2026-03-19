# 🛒 Amazon Product Recommendation System

**TBS Barcelona – Group 7 | January 2026**

A recommendation engine built for the Amazon marketplace, implementing three strategies to predict products users will enjoy.

## 🎯 Objective

Build a recommendation system that, given a user's purchase and rating history, suggests 5 new products they will enjoy. The engine supports:

- **Popularity-Based** — Best sellers for new/unknown users (Cold Start solution)
- **User-Based Collaborative Filtering** — Finds users with similar shopping patterns
- **Item-Based Collaborative Filtering** — Finds products with similar rating profiles

All approaches use a **Hybrid Effective Rating**:

```
EffectiveRating = Rating + 0.1 × Sentiment
```

Similarity is measured with **Cosine Similarity**:

```
sim(X, Y) = (X · Y) / (||X|| × ||Y||)
```

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- The dataset file `Group7.xlsx` in the project root

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/TBS-Amazon-Recommender.git
cd TBS-Amazon-Recommender

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

The app will open at `http://localhost:8501`.

## 📊 Features

| Feature | Description |
|---------|-------------|
| User-Based CF | Enter a User ID to get personalized recommendations |
| Product-Based CF | Select a product to find similar items |
| Data Insights | Interactive EDA: sparsity, distributions, sentiment breakdown |
| Model Evaluation | Train/test split with RMSE, MAE, Precision@5, Coverage |

## 🛠 Tech Stack

- **Python** — Core language
- **Pandas** — Data manipulation and cleaning
- **Scikit-Learn** — Cosine similarity and train/test splitting
- **Streamlit** — Interactive web application
- **Plotly** — Data visualizations
- **Hu & Liu Lexicon** — Sentiment analysis (~2,000 positive, ~4,800 negative words)

## 📁 Project Structure

```
├── app.py                 # Main Streamlit application
├── Group7.xlsx            # Amazon ratings dataset
├── positive-words.txt     # Hu & Liu positive sentiment lexicon
├── negative-words.txt     # Hu & Liu negative sentiment lexicon
├── requirements.txt       # Python dependencies
└── README.md              # This file
```

## 👥 Team

Group 7 — TBS Barcelona, Master's Program

## 📝 License

Academic project — TBS Education, Barcelona Campus.
