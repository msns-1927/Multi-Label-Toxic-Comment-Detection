# Multi-Label-Toxic-Comment-Classification-using-TF-IDF-and-Logistic-Regression
“Built a multi-label toxic comment classification system using TF-IDF features and a One-Vs-Rest Logistic Regression model, evaluated with F1-score and ROC-AUC to handle class imbalance.”

**📌 Project Overview :**

Online platforms often struggle to moderate toxic and abusive user-generated content at scale. This project addresses that challenge by building a multi-label toxic comment classification system using classical Natural Language Processing (NLP) and machine learning techniques.

The model is designed to identify multiple types of toxicity within a single comment, including toxic, severe toxic, obscene, threat, insult, and identity hate. The project emphasizes a clean end-to-end machine learning workflow with a strong focus on feature engineering, interpretability, and proper evaluation for imbalanced data.

---------
**🧠 Problem Statement :**

Toxic comments can negatively impact online communities and user experience. Since a single comment can belong to multiple toxicity categories, this problem is framed as a multi-label text classification task rather than a simple binary classification problem.

Key challenges addressed:

- Multi-label classification
- Highly imbalanced target classes
- Converting unstructured text into meaningful numerical features
- Using appropriate evaluation metrics beyond accuracy

---------

**📂 Dataset Description :**

The dataset consists of user comments along with binary labels indicating different types of toxicity:
- toxic
- severe_toxic
- obscene
- threat
- insult
- identity_hate

Each comment may belong to zero, one, or multiple labels, making the task multi-label in nature.

---------

**🔧 Methodology :**

**1️⃣ Data Preprocessing :**
- Loaded and inspected the dataset
- Handled missing values in text fields
- Separated input features (comment_text) and target labels

**2️⃣ Feature Engineering :**
- Extracted linguistic features such as:
  - Comment length
  - Capital letter ratio
  - Average word length
  - Punctuation counts

- Converted raw text into numerical features using TF-IDF vectorization
   - Used unigrams and bigrams
   - Removed common English stop words

**3️⃣ Model Development :**
- Implemented a One-Vs-Rest Logistic Regression classifier to handle multi-label prediction
- Each toxicity label is modeled using a separate binary classifier
- This approach provides a strong, interpretable baseline for text classification tasks

---------

**📊 Model Evaluation :**

Due to the imbalanced nature of toxic comment data, accuracy alone is not a reliable metric. The model is evaluated using:
- Precision, Recall, and F1-score (per label)
- Micro F1-score for overall performance
- Macro F1-score to treat all labels equally
- ROC-AUC (micro-average) using predicted probabilities

These metrics provide a more realistic understanding of model performance across all toxicity categories.

---------

**✅ Results & Observations :**
- The model successfully learns patterns associated with different toxic behaviors
- Frequent toxicity categories (e.g., toxic, insult) perform better than rare ones (e.g., threat)
- TF-IDF with Logistic Regression provides a strong and interpretable baseline
- Proper metric selection significantly improves evaluation reliability

---------

**⚠️ Limitations :**
- The model relies on surface-level text features and may struggle with:
  - Sarcasm
  - Context-dependent toxicity
  - Implicit or subtle hate speech
- No deep learning or contextual embeddings are used in this implementation

---------

**🔮 Future Improvements :**
- Perform detailed error analysis on misclassified samples
- Tune decision thresholds for better recall/precision trade-offs
- Explore advanced NLP techniques such as word embeddings or transformer-based models
- Deploy the model as a REST API or web application for real-time moderation

---------

**🧰 Tools & Technologies Used :**
- Python
- Pandas, NumPy
- Scikit-learn
- TF-IDF Vectorizer
- Logistic Regression (One-Vs-Rest)
- Jupyter Notebook

---------

**🎯 Key Takeaway :**

This project demonstrates a complete and correct classical NLP machine learning pipeline for multi-label toxic comment classification, focusing on clarity, correctness, and industry-standard evaluation practices rather than unnecessary model complexity.
