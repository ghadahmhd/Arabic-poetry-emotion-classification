# Arabic Poetry Emotion Classification Using NLP and Machine Learning Techniques

## Overview
This project applies Natural Language Processing (NLP) and Machine Learning techniques to classify Arabic poetry into three emotional categories:

- Joy
- Love
- Sadness

The system processes Arabic poetic text, extracts linguistic features using TF-IDF, and predicts the dominant emotion expressed in a poem.

---

## Dataset
The original dataset contained approximately 9,455 Arabic poems labeled with emotional categories.

After preprocessing and cleaning:
- 9,449 valid poems remained

To reduce class imbalance, the dataset was balanced to:
- 1,900 Joy poems
- 1,900 Love poems
- 1,900 Sad poems

Final dataset size:
- 5,700 poems

---

## Preprocessing
Arabic text preprocessing included:

- Fixing Arabic text encoding
- Removing diacritics (Tashkeel)
- Arabic letter normalization
- Removing punctuation and numbers
- Removing extra whitespace
- Cleaning noisy text

Example normalization:
- أ / إ / آ → ا
- ى → ي
- ة → ه

---

## Feature Engineering
Text was transformed using:

**TF-IDF (Term Frequency–Inverse Document Frequency)**

Configuration:
- Maximum features: 7000
- N-grams: 1 to 3 (unigram, bigram, trigram)

This helped capture contextual poetic phrases.

---

## Models Used
The following models were evaluated:

1. Naive Bayes  
2. Logistic Regression  
3. Optimized Logistic Regression (final model)

Final model:
- Logistic Regression on balanced data

---

## Results
Final model performance:

- Accuracy: **60.7%**
- Macro F1-score: **0.60**

Class-wise F1-score:
- Joy: **0.66**
- Love: **0.59**
- Sadness: **0.56**

The confusion matrix showed overlap between emotional classes, especially between Love and Sadness, reflecting the blended emotional nature of Arabic poetry.

---

## Live Prediction
The model supports prediction on new Arabic poems.

Example:

Input:
"يا من سكنت القلب حبًا وملأت الروح نورًا"

Prediction:
Love / Joy (depending on phrasing)

---

## Files
- `arabic_poetry_emotion_classification.py` → project code
- `arabic_poem_emotion_model.pkl` → trained model
- `tfidf_vectorizer.pkl` → saved TF-IDF vectorizer

---

## Technologies
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---


