# Deep Machine Learning for Natural Language Processing  

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red?logo=pytorch)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-yellow?logo=huggingface)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikit-learn)

This is a 3-part Natural Language Processing (NLP) project, focusing on **Twitter Dataset Sentiment Analysis**.  

The main goal was to build a binary classification model (Positive/Negative) for a Twitter dataset, evolving from classical statistical methods to State-of-the-Art Large Language Models.

## Project Structure

The repository is organized into three progressive stages:

* **`[01_Statistical_Baseline]`**: The baseline approach using TF-IDF vectorization and Logistic Regression.
* **`[02_Deep_Learning_Word2Vec]`**: Custom Deep Neural Networks (DNN) trained on Word2Vec embeddings.
* **`[03_Transformers_FineTuning]`**: Transfer learning using BERT and DistilBERT models.

### Performance Comparison

A comparative analysis of the models developed across the three projects.  

To ensure a consistent and fair evaluation across all three architectural approaches, the models were assessed using a unified set of metrics: **Accuracy**, **Precision**, **Recall**, and **F1-Score**. Basic accuracy figures are displayed below, more detailed performance analysis is in
each part's report.

| Approach | Model Architecture | Feature Extraction | Accuracy (Test) | Key Takeaway |
| :--- | :--- | :--- | :--- | :--- |
| **Project 1** | Logistic Regression | TF-IDF | **~77%** | Strong baseline, highly interpretable, fast training. |
| **Project 2** | Feed-Forward NN (PyTorch) | Word2Vec (Gensim) | **~81%** | Captures semantic relationships but requires careful tuning. |
| **Project 3** | **BERT / DistilBERT** | Transformer Embeddings | **~90%** | **SOTA performance**; understands context, sarcasm, and complex syntax. |

*> Note: Detailed experiments, learning curves, and confusion matrices can be found in the report PDF of each sub-project.*

### Installation & Usage

Each sub-directory contains its own notebooks and datasets. To replicate the results:

1.  Clone the repository:
    ```bash
    git clone https://github.com/Fanisbar/ML_sentiment_analysis.git
    ```
2.  Navigate to the desired project folder (e.g., for BERT):
    ```bash
    cd 03_Transformers_FineTuning
    ```
3.  Install dependencies (ensure you have PyTorch and Transformers installed):
    ```bash
    pip install torch torchvision transformers scikit-learn pandas nltk gensim
    ```
4.  Run the Jupyter Notebooks located in the `notebooks/` directory.

*Developed as coursework for YS19:Artificial Intelligence II(Deep Machine Learning for Natural Language Processing), course of DIT, UoA. The assignment for each project
can be found in the report directory*.
<br>

## Author

* **Theofanis Barmparosos - Θεοφάνης Μπαρμπαρόσος**
* **ID**: sdi2200107
* **Institution**: Department of Informatics and Telecommunications(DIT), UoA  
