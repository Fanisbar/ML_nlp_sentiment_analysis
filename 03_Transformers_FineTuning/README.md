# Project 3: Fine-Tuning BERT & DistilBERT

The final stage of the project leverages **Transfer Learning** using Transformer-based architectures. We fine-tuned pre-trained Large Language Models (LLMs) from HuggingFace.

## Methodology

### 1. Models Used
* **BERT (Bidirectional Encoder Representations from Transformers):** Analyzes the context of a word in both directions (left-to-right and right-to-left).
* **DistilBERT:** A smaller, faster, cheaper, and lighter version of BERT, retaining 97% of its performance.

### 2. Fine-Tuning Process
* **Tokenization:** Used the specific `BertTokenizer` to handle sub-words.
* **Training:** Unfroze the classifier layers and fine-tuned the model weights on our specific sentiment dataset using the `Trainer` API (or custom PyTorch loop).
* **Evaluation:** Monitored Training Loss vs. Validation Loss to stop early and avoid overfitting.

## File Description
* `notebooks/sdi2200107_bert.ipynb`: Fine-tuning pipeline for the standard BERT model.
* `notebooks/sdi2200107_distill_bert.ipynb`: Fine-tuning pipeline for DistilBERT.
* `report/experiments_bert.txt` & `report/experiments_distill_bert.txt`: Logs from experimental runs.

## Results
* **Accuracy:** Great improvement to aprox. 85% on the validation set.
* **Key Finding:** BERT successfully captures nuances like sarcasm and double negatives that completely baffled the TF-IDF and Word2Vec models.
