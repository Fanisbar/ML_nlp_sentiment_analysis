# Project 2: Neural Networks & Word Embeddings

In this stage, we move beyond simple frequency counts (TF-IDF) to capture the **semantic meaning** of words using Deep Learning.

## Methodology

### 1. Word Embeddings (Word2Vec)
Instead of treating words as independent symbols, we trained a **Word2Vec** model (using `Gensim`) on the dataset.
* Maps words to dense vectors in a continuous vector space.
* Words with similar meanings (e.g., "good" and "great") are positioned close to each other.

### 2. Deep Neural Network (DNN)
We implemented a custom Feed-Forward Neural Network using **PyTorch**.
* **Input:** Aggregated Word2Vec embeddings (Mean/Sum pooling).
* **Hidden Layers:** Fully connected layers with **ReLU** activation.
* **Regularization:** Applied **Dropout** to prevent overfitting on the small dataset.
* **Optimization:** Adam Optimizer with Cross-Entropy Loss.

## File Description
* `notebooks/sdi2200107.ipynb`: The PyTorch training pipeline, including evaluation.
* `notebooks/tutorials/`: Contains reference notebooks for PyTorch basics and Word Embeddings.
* `report/final_report.pdf`: Analysis of the learning curves and hyperparameter tuning.

## Results
* **Accuracy:** Very minimal improvement to aprox. 79% on the validation set.
* **Observations:** The model generalizes slightly better than Logistic Regression but requires careful tuning of the
learning rate and hidden layer dimensions. Also, due to the complex depth of the model, large datasets are required to
achieve better results and take full advantage of the architecture.
