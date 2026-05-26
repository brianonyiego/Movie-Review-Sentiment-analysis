# 🎬 Movie Review Sentiment Analysis

Deep Learning-based Sentiment Analysis project for IMDb-style movie reviews using multiple word embedding techniques and neural network architectures.

## 📌 Project Overview

This project focuses on binary sentiment classification of movie reviews using Natural Language Processing (NLP) and Deep Learning techniques.

The study compares the performance of:

- **Word Embeddings**
  - GloVe
  - fastText

- **Deep Learning Architectures**
  - BiLSTM
  - CNN-GRU

The objective is to determine which embedding and neural network combination performs best for movie review sentiment prediction.

---

## 📖 Background

Sentiment Analysis (Opinion Mining) is a Natural Language Processing task used to classify textual opinions as positive or negative.

This project applies sentiment analysis to IMDb-style movie reviews to explore:

- Customer opinion mining
- Text preprocessing
- Deep learning for NLP
- Comparative model evaluation
- Big data considerations in text analytics

---

# 🗂 Dataset

The dataset contains:

- Movie review text
- Binary sentiment labels
  - Positive
  - Negative

### Dataset Statistics

| Metric | Value |
|---|---|
| Total Reviews | 14,885 |
| Positive Reviews | 7,441 |
| Negative Reviews | 7,444 |
| Average Raw Review Length | 232.95 words |
| Average Processed Review Length | 120.87 words |

The dataset was balanced to reduce bias caused by class imbalance.

---

# ⚙️ Data Preprocessing

The preprocessing pipeline included:

- Lowercasing
- Punctuation removal
- Stopword removal
- Tokenization
- Whitespace normalization
- Non-alphabetic token filtering

### Important NLP Consideration

Negation words such as:

- `not`
- `never`
- `no`

were preserved because they carry strong sentiment meaning.

---

# 📊 Exploratory Data Analysis

The project included:

- Sentiment distribution analysis
- Review length analysis
- Word frequency visualization
- ROC curve analysis
- Confusion matrix evaluation

---

# 🧠 Deep Learning Models

Four model combinations were implemented:

| Embedding | Architecture |
|---|---|
| GloVe | BiLSTM |
| GloVe | CNN-GRU |
| fastText | BiLSTM |
| fastText | CNN-GRU |

---

# 🏗 Model Architectures

## 1️⃣ BiLSTM

Bidirectional Long Short-Term Memory networks capture:

- Forward context
- Backward context
- Sequential dependencies
- Long-range sentiment relationships

Best suited for sentiment understanding.

---

## 2️⃣ CNN-GRU

Hybrid architecture combining:

- CNN for local feature extraction
- GRU for sequential learning

Used to evaluate hybrid deep learning performance for text classification.

---

# 📈 Model Performance

| Model | Accuracy | AUROC |
|---|---|---|
| GloVe + BiLSTM | 0.7586 | 0.8260 |
| GloVe + CNN-GRU | 0.5078 | 0.5063 |
| fastText + BiLSTM | **0.7627** | **0.8375** |
| fastText + CNN-GRU | 0.4926 | 0.4969 |

---

# 🏆 Best Performing Model

## ✅ fastText + BiLSTM

### Performance

- Accuracy: **76.27%**
- AUROC: **0.8375**

### Why it performed best

- fastText handles:
  - rare words
  - misspellings
  - subword information

- BiLSTM captures:
  - contextual dependencies
  - bidirectional sequence information

This combination produced the strongest sentiment discrimination capability.

---

# 📉 Error Analysis

### BiLSTM Models

- Balanced predictions
- Better sentiment separation
- Lower false positive and false negative rates

### CNN-GRU Models

Observed issues:

- Prediction bias
- Underfitting
- Near-random classification
- Poor AUROC (~0.5)

Possible causes:

- Hyperparameter tuning issues
- Insufficient model capacity
- Training instability

---

# 💼 Business Applications

This project demonstrates how sentiment analysis can support:

- Streaming platforms
- Recommendation systems
- Brand monitoring
- Customer feedback analysis
- Audience engagement tracking
- Content strategy optimization

---

# ⚠️ Limitations

- Binary sentiment only
- Limited dataset size
- No sarcasm detection
- No transformer models (e.g., BERT)
- CNN-GRU models require further tuning

---

# 🛡 Governance & Ethics

Key considerations include:

- Bias monitoring
- Privacy protection
- Responsible AI deployment
- Human oversight
- Transparency in automated sentiment scoring

---

# 🛠 Technologies Used

## Programming Language

- Python

## Libraries & Frameworks

- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- NLTK

## NLP Embeddings

- GloVe
- fastText

---

# 📂 Project Structure

```bash
Movie-Review-Sentiment-Analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── preprocessing.ipynb
│   ├── eda.ipynb
│   └── model_training.ipynb
│
├── models/
│   ├── glove_bilstm/
│   ├── glove_cnn_gru/
│   ├── fasttext_bilstm/
│   └── fasttext_cnn_gru/
│
├── results/
│   ├── confusion_matrices/
│   ├── roc_curves/
│   └── plots/
│
├── requirements.txt
├── README.md
└── report.pdf
```

---

# 🚀 How to Run the Project

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/movie-review-sentiment-analysis.git
cd movie-review-sentiment-analysis
```

---

## 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3️⃣ Run Preprocessing

```bash
python preprocessing.py
```

---

## 4️⃣ Train Models

```bash
python train.py
```

---

## 5️⃣ Evaluate Models

```bash
python evaluate.py
```

---

# 📚 References

- Maas et al. (2011) — IMDb Sentiment Dataset
- Pennington et al. (2014) — GloVe Embeddings
- Bojanowski et al. (2017) — fastText
- Hochreiter & Schmidhuber (1997) — LSTM
- Liu (2012) — Sentiment Analysis and Opinion Mining

---

# 👨‍🎓 Academic Information

| Field | Value |
|---|---|
| Assignment Title | Movie Review Sentiment Analysis |
| Module Code | MANG3098 |
| Student ID | 33414882 |

---

# ⭐ Key Takeaway

The project demonstrates that combining **fastText embeddings** with a **BiLSTM architecture** provides strong sentiment classification performance for movie reviews by effectively capturing contextual and subword-level semantic information.
