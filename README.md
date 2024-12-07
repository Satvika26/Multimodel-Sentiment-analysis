# Multimodel-Sentiment-analysis

Overview
This project performs sentiment analysis on Amazon reviews using two approaches:
1. VADER Sentiment Analysis: A lexicon and rule-based sentiment analysis tool, part of the `nltk` library.
2. Roberta Sentiment Analysis: A transformer-based model fine-tuned for sentiment analysis.

The goal is to compare these models and analyze customer sentiments based on their review scores.

Steps and Features

1. Data Preprocessing:
   - Reviews data is loaded from a CSV file (`Reviews.csv`).
   - Limited to the first 500 reviews for efficiency.
   - Displays the distribution of review scores (1–5 stars).

2. Sentiment Analysis:
   - VADER Sentiment Analysis:
     - Analyzes review text to calculate positive, negative, neutral, and compound sentiment scores.
     - Results are visualized to show sentiment trends for different star ratings.
   - Roberta Sentiment Analysis:
     - Uses the `cardiffnlp/twitter-roberta-base-sentiment` model to compute softmax probabilities for negative, neutral, and positive sentiments.

3. Combining Results:
   - Sentiment scores from both models are merged into a unified DataFrame.
   - Sentiment trends and relationships are visualized using bar plots and pair plots.

4. Insights from Reviews:
   - Identifies the most positive/negative reviews for specific star ratings using both models.
   
Visualizations
- Distribution of Review Scores: Bar plot of the number of reviews for each star rating.
- Sentiment Scores by Stars:
  - Compound scores by review stars using VADER.
  - Positive, neutral, and negative scores using VADER and Roberta.
- Pairplot: Displays correlations between VADER and Roberta sentiment scores.

 Requirements
The project uses the following libraries:
- Pandas: For data manipulation.
- Numpy: For numerical operations.
- Matplotlib & Seaborn: For visualizations.
- NLTK: For VADER sentiment analysis.
- Hugging Face Transformers: For Roberta sentiment analysis.
- TQDM: For progress visualization during analysis.


Sample Insights
- VADER and Roberta models are compared for accuracy and alignment.
- Example findings:
  - "Most positive review (1-star)" and "most negative review (5-stars)" identified to understand anomalies.

Future Enhancements
- Expand analysis to the full dataset.
- Incorporate topic modeling for deeper insights.
- Improve efficiency with batch processing for transformer-based models.

