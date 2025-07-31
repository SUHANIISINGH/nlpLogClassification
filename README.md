# Log Classification with Hybrid Classification Framework

This project implements a hybrid log classification system using a combination of rule-based, machine learning, and LLM-based approaches to handle different log complexities effectively.

---

## Classification Approaches

### 1. **Regular Expression (Regex)**
- Ideal for simple and predictable log patterns.
- Uses predefined rules for classification.

### 2. **Sentence Transformer + Logistic Regression**
- Suitable for complex patterns with sufficient labeled data.
- Converts log messages into vector embeddings and applies Logistic Regression.

### 3. **LLM (Large Language Model)**
- Useful when there isn’t enough labeled data.
- Provides contextual understanding to classify challenging patterns.

---

## Architecture Overview

The system follows a hybrid classification pipeline:
1. First, it checks if a log matches any Regex pattern.
2. If not, it uses the ML model (Sentence Transformer + Logistic Regression).
3. As a fallback or for uncertain predictions, the LLM (e.g., GPT-based) is used.

---

## Folder Structure

```markdown
classification.log/
├── models/                         # Contains trained ML models and embeddings
├── resources/                      # Contains sample logs, outputs, architecture diagrams
│   └── .ipynb_checkpoints/         # Jupyter notebook auto-saves (can be ignored)
├── training/                       # Code for training regex and ML models
│   ├── dataset/                    # Raw and preprocessed datasets for training
│   └── .ipynb_checkpoints/         # Jupyter notebook auto-saves (can be ignored)
├── .ipynb_checkpoints/            # Global Jupyter checkpoint folder (can be ignored)
├── __pycache__/                   # Python bytecode cache files (auto-generated)
```
