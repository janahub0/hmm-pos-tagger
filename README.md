# Part-of-Speech Tagging with Hidden Markov Models

This project implements a **Part-of-Speech (POS) tagger** using a **Hidden Markov Model (HMM)** and compares it against a simple baseline model, the **Most Frequent Class (MFC) tagger**.

The model is trained and evaluated on a preprocessed version of the **Brown corpus** using the **universal POS tagset**.

---

## Project Overview

Part-of-speech tagging assigns grammatical categories (e.g., NOUN, VERB, ADJ) to words based on their context.  
In this project, I built:

- A **Most Frequent Class (MFC)** tagger as a baseline
- A **Hidden Markov Model (HMM)** POS tagger using maximum likelihood estimates

The HMM models both:
- **Emission probabilities** (word | tag)
- **Transition probabilities** (tag | previous tag)

---

## Dataset

- Source: Brown corpus (universal tagset)
- Total sentences: 57,340
- Training split: 80%
- Testing split: 20%
- Number of tags: 12

---

## Models Implemented

### 1. Most Frequent Class (MFC) Tagger
- Assigns each word the tag it most frequently appeared with in training
- Used as a baseline for comparison

**Accuracy:**
- Training: ~95.7%
- Testing: ~93.0%

---

### 2. Hidden Markov Model (HMM) Tagger
- One hidden state per POS tag
- Discrete emission distributions
- Fully connected tag transition graph
- Start and end state probabilities estimated from data

**Accuracy:**
- Training: >97%
- Testing: >95.5%

---

## Implementation Details

The following components were implemented from scratch:

- Pair counts for word–tag emissions
- Unigram and bigram tag counts
- Sentence start and end tag probabilities
- Construction of the HMM using Pomegranate
- Viterbi decoding for sequence prediction
- Accuracy evaluation on training and test sets

---

## Files in This Repository

- `HMM Tagger.ipynb` – Jupyter Notebook with full implementation and outputs
- `HMM Tagger.html` – HTML export of the executed notebook
- `helpers.py` – Dataset utilities (provided)
- `tests.py` – Test assertions (provided)
- `README.md` – Project documentation

---

## Technologies Used

- Python
- Pomegranate
- NumPy
- Jupyter Notebook
