# Day 21 – Natural Language Processing (NLP)

[Google Colab Notebook Link](https://colab.research.google.com/drive/1QIHU6at93UUKFl1hpmV0GH0TZXNwgnzk)

## Overview

I learned about **Natural Language Processing (NLP)**, a branch of Artificial Intelligence that helps computers understand, analyze, and process human language.

I explored different NLP techniques such as text cleaning, tokenization, stopword removal, stemming, lemmatization, Bag of Words, and TF-IDF. I also worked on an Amazon Reviews Sentiment Analysis project using Logistic Regression to classify reviews as positive or negative.

## Topics Covered

### 1. Introduction to NLP

NLP stands for **Natural Language Processing**. It is a part of Artificial Intelligence that enables computers to understand, analyze, and process human language.

**Real-life applications of NLP:**
- Google Translate
- Chatbots and customer support systems
- Voice assistants like Alexa and Siri
- Spam email detection
- Sentiment analysis of customer reviews

### 2. NLP Pipeline

An NLP pipeline consists of several steps used to process text data.

1. Text Input
2. Text Cleaning
3. Tokenization
4. Stopword Removal
5. Stemming or Lemmatization
6. Feature Extraction
7. Model Building
8. Prediction

### 3. Installing and Importing Libraries

I used NLTK and Regular Expressions for performing NLP tasks.

```python
# pip install nltk

import nltk
import re
```

- **NLTK:** Natural Language Toolkit used for NLP operations.
- **re:** Used for pattern matching and text cleaning.

I also downloaded the required NLTK resources.

```python
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```

### 4. Text Cleaning

Text cleaning is the process of removing unwanted characters, numbers, and symbols from text data.

I used Regular Expressions to remove special characters and numbers.

```python
text = "NLP is very interesting and useful for $$$$@@33354 beginners!"

clean_text = re.sub('[^a-zA-Z]', ' ', text)

print(clean_text)
```

This keeps alphabetic characters and replaces other characters with spaces.

### 5. Tokenization

Tokenization is the process of breaking text into smaller units called tokens, usually words.

```python
from nltk.tokenize import word_tokenize

tokens = word_tokenize(clean_text)

print(tokens)
```

**Example:**

Input: `"NLP is very interesting"`

Output: `['NLP', 'is', 'very', 'interesting']`

### 6. Stopword Removal

Stopwords are common words that usually carry less important information for a particular text analysis task.

Examples: is, am, are, the, a, an, for, and.

```python
from nltk.corpus import stopwords

stop_words = set(stopwords.words('english'))

filtered_tokens = []

for word in tokens:
    if word.lower() not in stop_words:
        filtered_tokens.append(word)

print(filtered_tokens)
```

Stopword removal helps reduce unnecessary words in text.

### 7. Stemming

Stemming is the process of reducing words to their root form. The resulting word may not always be a meaningful dictionary word.

```python
from nltk.stem import PorterStemmer

stemmer = PorterStemmer()

stemmed_words = []

for word in filtered_tokens:
    stemmed_words.append(stemmer.stem(word.lower()))

print(stemmed_words)
```

**Examples:**
- playing → play
- studies → studi
- interesting → interest

### 8. Lemmatization

Lemmatization reduces words to their meaningful dictionary root form.

```python
from nltk.stem import WordNetLemmatizer

lemmatizer = WordNetLemmatizer()

lemmatized_words = []

for word in filtered_tokens:
    lemmatized_words.append(lemmatizer.lemmatize(word.lower()))

print(lemmatized_words)
```

**Examples:**
- studies → study
- better → better (with default noun-based lemmatization, context matters)

Lemmatization generally produces meaningful words, unlike some stemming results.

### 9. Bag of Words (BoW)

Bag of Words is a text feature extraction technique that converts text into numerical form by counting word occurrences.

```python
from sklearn.feature_extraction.text import CountVectorizer

corpus = ["nlp is fun", "nlp is powerful"]

vectorizer = CountVectorizer()

bow = vectorizer.fit_transform(corpus)

print(vectorizer.get_feature_names_out())
print(bow.toarray())
```

It creates a vocabulary and represents each sentence using word counts.

### 10. TF-IDF (Term Frequency–Inverse Document Frequency)

TF-IDF is a feature extraction technique that assigns importance to words based on their frequency in a document and across the collection of documents.

It gives relatively higher importance to words that are frequent in a particular document but less common across the entire collection.

```python
from sklearn.feature_extraction.text import TfidfVectorizer

vectorizer = TfidfVectorizer()

tfidf = vectorizer.fit_transform(corpus)

print(vectorizer.get_feature_names_out())
print(tfidf.toarray())
```

### 11. Introduction to Amazon Reviews Dataset

I used an Amazon Reviews dataset containing customer reviews and ratings.

```python
import numpy as np
import pandas as pd

df = pd.read_csv("/content/Amazon_Reviews.csv", engine='python')
```

I explored the dataset using:

```python
df.head()
df.tail()
df.info()
```

The dataset contained 21,214 rows and 9 columns.

For sentiment analysis, I selected only the Review Text and Rating columns.

```python
df = df[['Review Text', 'Rating']]
```

### 12. Text Preprocessing on Amazon Reviews

I created a function to clean the customer reviews by converting text to lowercase and removing URLs, special characters, and extra spaces.

```python
import re

def clean_text(text):
    text = str(text).lower()
    text = re.sub(r"http\S+", "", text)
    text = re.sub(r"[^a-zA-Z]", " ", text)
    text = re.sub(r"\s+", " ", text).strip()
    return text

df['clean_text'] = df['Review Text'].apply(clean_text)
```

I then removed stopwords and applied lemmatization to prepare the text for feature extraction.

```python
from nltk.corpus import stopwords

stop_words = set(stopwords.words('english'))

def remove_stopwords(text):
    return " ".join([
        word for word in text.split()
        if word not in stop_words
    ])

df['clean_text'] = df['clean_text'].apply(remove_stopwords)
```

```python
from nltk.stem import WordNetLemmatizer

lemmatizer = WordNetLemmatizer()

def lemmatize(text):
    return " ".join([
        lemmatizer.lemmatize(word)
        for word in text.split()
    ])

df['clean_text'] = df['clean_text'].apply(lemmatize)
```

### 13. Feature Extraction Using TF-IDF

After cleaning the reviews, I converted text into numerical features using TF-IDF.

```python
from sklearn.feature_extraction.text import TfidfVectorizer

vectorizer = TfidfVectorizer(max_features=5000)

X = vectorizer.fit_transform(df['clean_text'])
```

Here, `max_features=5000` limits the vocabulary to a maximum of 5,000 features.

### 14. Creating Sentiment Labels

I converted customer ratings into binary sentiment labels.

- Rating 4 or above → Positive (1)
- Rating below 4 → Negative (0)

```python
def sentiment_label(rating_str):
    if not rating_str:
        return 0

    try:
        rating = int(rating_str.split()[1])
        return 1 if rating >= 4 else 0
    except:
        return 0

y = df['Rating'].apply(sentiment_label)
```

### 15. Model Training Using Logistic Regression

I used the Logistic Regression algorithm to classify customer reviews into positive and negative categories.

First, I divided the dataset into training and testing sets.

```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2
)
```

Then, I created and trained the model.

```python
model = LogisticRegression()

model.fit(X_train, y_train)
```

### 16. Model Evaluation

I evaluated the model using Accuracy Score.

```python
from sklearn.metrics import accuracy_score

y_pred = model.predict(X_test)

print("Accuracy:", accuracy_score(y_test, y_pred))
```

The notebook showed an accuracy of approximately **92.10%**.

### 17. Visualizing Rating Distribution

I used a bar graph to visualize the distribution of customer ratings.

```python
import matplotlib.pyplot as plt

df['Rating'].value_counts().plot(kind='bar')

plt.show()
```

### 18. Predicting Sentiment of New Reviews

I created a function to predict whether a new customer review is positive or negative.

```python
def predict_review(review_text):
    clean = clean_text(review_text)
    no_stopwords = remove_stopwords(clean)
    lemmatized = lemmatize(no_stopwords)

    review_vectorized = vectorizer.transform([lemmatized])

    prediction = model.predict(review_vectorized)

    if prediction[0] == 1:
        return "Positive review"
    else:
        return "Negative review"
```

**Example:**

```python
print(predict_review(
    "This product is amazing and works perfectly"
))

print(predict_review(
    "Worst experience, waste of money"
))
```

The function predicts the sentiment of a new review using the trained Logistic Regression model.

## Key Learnings

1. Understood the meaning and applications of NLP.
2. Learned the different stages of an NLP pipeline.
3. Practiced text cleaning using Regular Expressions.
4. Understood tokenization and stopword removal.
5. Learned the difference between stemming and lemmatization.
6. Understood Bag of Words and TF-IDF techniques.
7. Worked with an Amazon Reviews dataset.
8. Learned how to preprocess customer review text.
9. Converted text into numerical features using TF-IDF.
10. Trained a Logistic Regression model for sentiment classification.
11. Evaluated model performance using accuracy score.
12. Created a function to predict sentiment for new reviews.

## Practice Questions

1. What is Natural Language Processing (NLP)?
2. Give five real-life applications of NLP.
3. What are the main steps of an NLP pipeline?
4. What is the use of the NLTK library?
5. What is text cleaning?
6. What is tokenization?
7. What are stopwords?
8. Explain stemming and lemmatization.
9. What is Bag of Words?
10. What is TF-IDF and why is it used?
11. What is sentiment analysis?
12. How was the Amazon Reviews dataset used in this practical?
13. How were positive and negative sentiment labels created?
14. Why was Logistic Regression used?
15. What is accuracy score?
