# movie-sentiment-analysis-nlp

# Sentiment Analysis on IMDb Movie Reviews

## Project Overview
This project explores how different Natural Language Processing (NLP) models can classify the sentiment of IMDb movie reviews as **positive** or **negative**.  
The study compares classical machine learning algorithms, **Naive Bayes**, **Logistic Regression**, and **Support Vector Machine (SVM)**, with a modern transformer-based deep learning model, **BERT (Bidirectional Encoder Representations from Transformers)**.

The goal is to evaluate how well these models understand language sentiment, balancing **accuracy, interpretability, and computational efficiency**.

---

## Models Implemented
### Classical Machine Learning Models
- **Naive Bayes (NB)** : simple probabilistic model that performs well on sparse data.  
- **Logistic Regression (LR)** : linear model that captures sentiment polarity effectively.  
- **Support Vector Machine (SVM)** : margin-based classifier that generalizes well on TF-IDF features.

### Transformer Model
- **BERT (Fine-Tuned)** : pre-trained deep learning model fine-tuned on a smaller IMDb subset for sentiment classification.

---

## Results Summary
| **Model** | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
|:--|:--:|:--:|:--:|:--:|
| Naive Bayes | 0.825 | 0.80 | 0.8643 | 0.8309 |
| Logistic Regression | 0.835 | 0.7930 | 0.9045 | 0.8451 |
| SVM | 0.815 | 0.7803 | 0.8744 | 0.8246 |
| BERT (Fine-tuned) | 0.8275 | 0.88 | 0.76 | 0.81 |

**Key Insight:**  
Classical models, especially Logistic Regression, achieved strong and consistent performance using TF-IDF features.  
BERT demonstrated high precision and contextual understanding, even when trained on a smaller dataset. With more data and epochs, it is expected to outperform traditional models.

---

## Workflow
1. **Data Preprocessing** : text cleaning, tokenization, stopword removal, stemming, and lemmatization.  
2. **Feature Extraction** : using TF-IDF for classical models and tokenization for BERT.  
3. **Model Training** : each model trained separately using Python (v3.12), scikit-learn, and Hugging Face Transformers.  
4. **Evaluation** : accuracy, precision, recall, F1-score, and confusion matrices were computed for each model.  

---

## Dataset
- **Source:** IMDb Large Movie Review Dataset (50,000 reviews: 25k positive, 25k negative).  
- **Usage:** Full dataset used for classical models; a smaller 2,000-sample subset used for BERT fine-tuning due to hardware limits.  

---

## Technologies Used
- Python (v3.12)  
- scikit-learn  
- NLTK  
- Hugging Face Transformers  
- Pandas, NumPy, Matplotlib  

---

## Future Work
- Fine-tune BERT on the full IMDb dataset and extend training epochs.  
- Test smaller transformer models like **DistilBERT** for efficiency.  
- Try hybrid (ensemble) methods combining classical and transformer models.  


---

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/nlp-sentiment-analysis.git
   cd nlp-sentiment-analysis
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\Scripts\activate      # Windows
   ```

3. ***Install dependencies***
   ```bash
   pip install -r requirements.txt
   ```

4. ***Run the notebook***
   ```bash
   jupyter notebook
   ```# nlp-sentiment-analysis-movie
