# Aspect-Based Sentiment Analysis using BERT

## Overview
This repository implements Aspect-Based Sentiment Analysis (ABSA) using BERT-based models. It consists of two main components:

1. **Aspect Term Extraction (ATE)**: Identifies aspect terms in a given text.
2. **Aspect Sentiment Analysis (ASA)**: Determines the sentiment polarity (Positive, Neutral, or Negative) associated with an aspect term.

---

## 1. Aspect Term Extraction (ATE)
### Model: `aspect_term_extraction_BERTs.py`
- Uses **DistilBERT** for Named Entity Recognition (NER) to extract aspect terms.
- Trained with `Trainer` from Hugging Face.
- Saves the model and tokenizer for inference.
- Uses `pipeline` for testing aspect extraction on a sample sentence.

---

## 2. Aspect Sentiment Analysis (ASA)
### Model: `aspect_sentiment_analysis_BERTs.py`
- Uses **DistilBERT** for sequence classification (sentiment analysis).
- Predicts sentiment polarity (`Positive`, `Neutral`, `Negative`).
- Uses `Trainer` from Hugging Face for fine-tuning.
- Combines extracted aspect terms with original sentences for sentiment classification.
