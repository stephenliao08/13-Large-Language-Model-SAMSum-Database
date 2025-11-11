# ACME Dialogue Summarization (SAMSum)

**BLUF:**  
Build and compare **BART**, **BERT2BERT**, and **T5** on the **SAMSum** dataset to generate concise chat recaps.  
Target performance: **ROUGE-1 / ROUGE-L ≈ 0.4–0.5** with **sub-second inference latency**.

---

## 1. Overview

Acme’s group chats are overloaded—important updates get buried and users spend **5–10 minutes** catching up.  
This project delivers an AI summarizer trained on **SAMSum** (~16k chats) to produce short, messenger-style summaries.

Pipeline includes:

- Data loading, cleaning, tokenization  
- Model training (BART, BERT2BERT, T5)  
- Evaluation (ROUGE + qualitative spot-checks)  
- Inference utilities for fast deployment

**Goal:** ROUGE-1/ROUGE-L ≈ 0.4–0.5 + sub-second inference.

---

## 2. Dataset

**Name:** `knkarthick/samsum` (Hugging Face)  
**Size:** ~16,000 conversation–summary pairs  
**Splits:**  
- Train: ~14.7k  
- Validation: ~818  
- Test: ~819  

Style: informal, multi-turn, messenger-like conversations.

---

## 3. Installation & Environment

**Requirements**

- Python 3.9+  
- PyTorch (GPU recommended)  
- Libraries: `transformers`, `datasets`, `evaluate`, `nltk`, `matplotlib`, `seaborn`, `wordcloud`

**Install**

```bash
pip install "transformers>=4.36" datasets evaluate nltk matplotlib seaborn wo
