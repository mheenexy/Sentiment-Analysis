## Flipkart Product Review Sentiment Analysis

This project aims to classify customer reviews from Flipkart into sentiment categories. The analysis involves text preprocessing, exploratory data analysis (EDA), and machine learning using classification algorithms.

## Overview

The dataset contains over 200,000 product reviews. By leveraging Natural Language Processing (NLP) techniques, we clean the text data and convert it into numerical features using TF-IDF vectorization to train predictive models.

## Dataset

* **Source:** [Kaggle - Flipkart Product Customer Reviews Dataset](https://www.kaggle.com/datasets/niraliivaghani/flipkart-product-customer-reviews-dataset)
* **Initial Size:** 205,052 rows.
* **Cleaned Size:** 171,572 rows (after removing nulls and duplicates).
* **Key Columns:** - `Summary`: Short review title.
* `Review`: Detailed customer feedback.
* `Sentiment`: Target label (Positive, Negative, Neutral).



## Tech Stack

* **Language:** Python
* **Libraries:**
* Data Handling: `pandas`, `numpy`
* NLP: `nltk`, `re` (Regular Expressions)
* Visualization: `matplotlib`, `seaborn`, `wordcloud`
* Machine Learning: `scikit-learn`



## Workflow

### 1. Data Cleaning

* Handled missing values in the `Review` and `Summary` columns.
* Removed duplicate entries to ensure model integrity.

### 2. Text Preprocessing

Standard NLP pipeline applied to the review text:

* Lowercasing.
* Removing special characters and numbers.
* Tokenization.
* Removing Stopwords (e.g., "the", "is", "at").
* **Lemmatization:** Reducing words to their root form (e.g., "running" $\rightarrow$ "run").

### 3. Exploratory Data Analysis (EDA)

* Visualized the distribution of sentiments (Positive reviews are the most frequent).
* Generated **Word Clouds** to identify the most common words in positive and negative reviews.

### 4. Feature Engineering

* Used **TF-IDF Vectorizer** (Term Frequency-Inverse Document Frequency) to convert text into a matrix of numerical features, highlighting the importance of specific words across the corpus.

### 5. Modeling

Two classification models were trained and compared:

* **Logistic Regression**
* **Random Forest Classifier**

## Results

The models were evaluated based on their accuracy on the test dataset:

| Model | Accuracy |
| --- | --- |
| **Logistic Regression** | **96.44%** |
| Random Forest | 95.01% |

**Conclusion:** Logistic Regression outperformed the Random Forest model for this specific text classification task.
