---
layout: page
title: CLARITY - Unmasking Political Question Evasions
description: Engineered a complete NLP pipeline and fine-tuned Large Language Models to classify evasive political responses.
img: /assets/img/CLARITY.jpg
importance: 1
category: Course Project
---

**TL;DR:** Engineered an accelerated NLP pipeline and fine-tuned Large Language Models (including Llama 3.1) to classify direct, partial, and evasive political responses, outperforming state-of-the-art baselines on the SemEval CLARITY dataset.

![SemEval CLARITY](/assets/img/CLARITY.jpg)

### Technologies & Methodology
* **Software & Frameworks:** Python, PyTorch, Hugging Face Transformers, spaCy, NLTK, ELFEN, scikit-learn, Tinker.
* **Machine Learning Models:** Llama-3.1-8B-Instruct, Llama-3.1-70B-Instruct, RoBERTa-base, Neural Networks, Support Vector Machines (SVM).
* **Dataset & Tools:** SemEval CLARITY dataset, Optuna (hyperparameter optimization).

### Key Contributions & Results
* Developed an accelerated NLP preprocessing and feature extraction pipeline utilizing parallelization, spaCy for negation detection, and ELFEN for hedge detection.
* Fine-tuned a Llama-3.1-8B-Instruct decoder model via the Tinker platform, achieving a 0.71 Weighted F1 score that significantly outperformed existing dataset baselines.
* Evaluated encoder-only (RoBERTa) and classical baseline architectures (SVM, Random Forest, Neural Networks) to benchmark semantic alignment and contextual performance against raw linguistic features.
* Addressed severe class imbalances (Clear Reply vs. Ambivalent vs. Clear Non-Reply) by optimizing macro-averaged metrics through Optuna hyperparameter tuning.

