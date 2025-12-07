## Cross-Domain Sentiment Analysis: Electronics → Skincare Reviews

**Overview**

This project investigates how sentiment analysis models perform when trained in one domain and tested in another. Specifically, it evaluates three approaches:

Logistic Regression

BiLSTM (Bidirectional Long Short-Term Memory)

DistilBERT

The main research question is: How does model performance change when moving from Amazon Electronics reviews to Sephora Skincare reviews?

**Datasets**

1. Amazon Electronics Reviews

  Used as the source (training) domain.
  Reviews contain product ratings, text, and metadata.

2. Sephora Skincare Reviews

  Used as the target (cross-domain) dataset.
  Contains reviews of skincare products including ratings and free-text feedback.

Both datasets were preprocessed for cleaning, tokenization, and numerical encoding suitable for each model.

**Methodology**

Data Preprocessing: Cleaning, tokenization, padding, and vectorization (TF-IDF for Logistic Regression, sequences for BiLSTM, and tokenizer inputs for DistilBERT).

Model Training:

Logistic Regression trained on TF-IDF vectors.
BiLSTM trained on padded word sequences.
DistilBERT fine-tuned for sequence classification.

**Evaluation Metrics:**

Accuracy, 
Precision, 
Recall, 
F1-score.

Cross-domain F1 drop to assess robustness under domain shift.

Cross-Domain Testing: Each model trained on Amazon Electronics was tested on Sephora Skincare reviews to simulate real-world domain transfer.

**Key Findings**

DistilBERT: Highest in-domain performance but largest drop in cross-domain F1, showing sensitivity to domain-specific language.

BiLSTM: Moderate in-domain performance, more resilient to domain shift.

Logistic Regression: Lower absolute performance but stable across domains.

**Conclusion** 

Transformer models excel in familiar contexts, but simpler architectures generalize more consistently across domains. Domain adaptation techniques could improve transformer performance for cross-domain sentiment analysis.

**Installation**

Clone the repository: git clone https://github.com/Atikuzzaman101/Sentiment_Analysis_Data_Science_Project.git 

Install dependencies: pip install -r requirements.txt

Download cleaned datasets from Kaggle and place them in the data/ folder.

