# 🎬 NetData

Interactive Streamlit dashboard for exploring Netflix content with sentiment analysis, a hybrid recommender, and trend visualizations.

**Tech stack:** Streamlit · Pandas/Scikit-learn · VADER + DistilBERT (sentiment) · TF-IDF + genre/rating hybrid similarity (recommender)

## Features

- **Dataset Overview** — Filter titles by type, country, and genre; view distribution charts.
- **Sentiment Analysis** — VADER-based sentiment across the catalog, plus on-demand VADER/DistilBERT prediction for custom text.
- **Hybrid Recommender** — TF-IDF description similarity + genre overlap + rating compatibility, with adjustable weights and Precision@5 / Coverage@5 / Diversity@5 evaluation.
- **Trend Analysis** — Library growth by year, top genre trends, and top country production trends.

![Dashboard](screenshots/Dataset_Overview.png)

## Setup

```bash
git clone https://github.com/yourusername/netflix-dashboard.git
cd netflix-dashboard
python -m venv venv && source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py
```

## Structure
```
netflix-ai-dashboard/
├── data/               # netflix_titles.csv
├── src/                # sentiment_analysis.py, recommender.py, data_cleaning.py
├── app.py
└── requirements.txt
```
