# 🧠 Aspect-Based Sentiment Analysis (ABSA) using RNN

This project implements an **Aspect-Based Sentiment Analysis (ABSA)** model using TensorFlow and `SimpleRNN`. Given a review, the model predicts the **sentiment** (positive, negative, neutral, or not mentioned) for multiple **aspects** such as `FOOD#QUALITY`, `SERVICE#GENERAL`, etc.

---

## 📁 Dataset Structure

Your dataset must be in `.csv` format and follow this structure:

| Review                                  | FOOD#QUALITY | SERVICE#GENERAL | ... |
|-----------------------------------------|--------------|------------------|-----|
| "The food was great but service was slow" | 1            | 2                | ... |

### 🔢 Label Encoding

| Value | Meaning        |
|-------|----------------|
| 0     | Not mentioned  |
| 1     | Positive       |
| 2     | Negative       |
| 3     | Neutral        |

> Internally, label `3` is mapped to `-1` to align with `tanh` or `softmax` based outputs depending on model type.

---

## 📦 Requirements

Install Python dependencies:

```bash
pip install -r requirements.txt
