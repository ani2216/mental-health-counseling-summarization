# 📘 Project Overview

Mental health counselling summarization

# Introduction
This project focuses on developing an automated system to summarize mental health counseling dialogues, helping clinicians by condensing lengthy therapy sessions into clear, actionable summaries. Leveraging sequence-to-sequence models like T5-base, T5-large, and instruction-aware LLM MentaLLaMA, along with domain-specific preprocessing (e.g., speaker tagging), we aim to capture the nuances of therapeutic conversations efficiently. Using Parameter-Efficient Fine-Tuning methods like QLoRA, the project balances clinical utility and computational feasibility. Initial results with T5-base are promising, with ongoing improvements expected from larger models and specialized techniques to better support mental health professionals in documentation and care.



1. **`preprocess.ipynb`** – Handles data loading and preprocessing tasks.
2. **`T5_Large.ipynb`** – Fine-tunes a T5-Large model on the processed data.

---

## 📁 File Descriptions

### `preprocess.ipynb`

- Loads the dataset.
- Performs data cleaning (e.g., removing nulls, filtering text).
- Tokenizes or formats the data as needed.
- Saves the processed data for use in training.

### `T5_Large.ipynb`

- Loads the preprocessed dataset.
- Initializes and configures the T5-Large model using HuggingFace Transformers.
- Sets training parameters such as learning rate, batch size, and number of epochs.
- Trains the model and evaluates it on a validation/test set.
- Optionally saves the trained model.

---

## Dataset Structure
![image](https://github.com/user-attachments/assets/214ca714-607f-4955-9d64-745ecf80c315)

## ⚙️ Requirements

Make sure you have the following libraries installed:

```bash
pip install transformers datasets scikit-learn pandas numpy torch tqdm
```

Also ensure you're using a compatible version of Python (3.7+ is recommended).

---

## 🚀 How to Run

1. **Preprocess the Data**  
   Run `preprocess.ipynb` to clean and prepare your dataset.

2. **Train the Model**  
   Run `T5_Large.ipynb` to fine-tune the T5 model using the preprocessed data.

---

## 📌 Notes

- It is recommended to run these notebooks in a GPU-enabled environment for faster training.
- Preprocessed data should be saved in a format that `T5_Large.ipynb` can read (like CSV or JSON).
- You may customize the model name, max token lengths, or training parameters within the notebook.
