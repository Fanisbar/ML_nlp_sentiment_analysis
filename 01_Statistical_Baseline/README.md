# Project 1: Statistical Sentiment Analysis

This project establishes a **baseline** for the sentiment analysis task using classical Machine Learning techniques. The focus here is on text preprocessing and statistical feature extraction without the use of deep neural networks.

## Methodology

### 1. Preprocessing
Before feeding data into the model, extensive cleaning was performed:
* Removal of URLs, user mentions (@user), and hashtags.
* Tokenization and lowercasing.
* **Stemming/Lemmatization** to reduce vocabulary size.
* Stop-word removal.

### 2. Feature Extraction (TF-IDF)
**Term Frequency-Inverse Document Frequency (TF-IDF)** was employed to convert text into numerical vectors. This highlights words that are unique to specific documents (tweets) while filtering out common noise.

### 3. Classification Model
* **Algorithm:** Logistic Regression.
* **Why?** It provides a probabilistic output and enables the inspection of feature importance (coefficients) to understand which words drive positive or negative sentiment.

## File Description
* `notebooks/sdi2200107.ipynb`: The main code for preprocessing, training, and evaluation.
* `report/final_report.pdf`: Detailed academic report including ROC curves and confusion matrices.
* `data/`: Contains the raw Twitter datasets.

## Results
* **Accuracy:** Achieved approx. 77% on the validation set.
* **Observations:** The model struggles with context (e.g., "not bad" might be classified as negative due to the word "bad").
