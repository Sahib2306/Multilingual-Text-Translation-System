# 🌍 Multilingual Text Translation System

A deep learning–based **multilingual text translation system** that translates text between **English, Hindi, Punjabi, Telugu, and Japanese** using an **LSTM encoder–decoder model**.  
The trained model is deployed as a **web application using FastAPI** with an easy-to-use browser interface.

---

## ✨ Features

- 🌐 Supports **5 languages**:
  - English
  - Hindi
  - Punjabi
  - Telugu
  - Japanese
- 🔁 **Any-to-any translation** using language tags
- 🧠 Deep Learning model (LSTM Encoder–Decoder)
- 🚀 Backend powered by **FastAPI**
- 🖥️ Web-based UI using **HTML + Jinja2**
- 🔤 Proper **Unicode font rendering** for all scripts
- 📊 Custom dataset with **10,000 rows**

---

## 🧱 Project Architecture
multilingual_translator/
│
├── data/
│ └── translation_dataset.csv
│
├── model/
│ ├── translation_model.h5
│ └── tokenizer.pkl
│
├── app/
│ ├── init.py
│ ├── main.py
│ ├── translate.py
│ └── templates/
│ └── index.html
│
├── train.py
├── requirements.txt
└── README.md


---

## 🧠 Model Overview

- Model Type: **LSTM Encoder–Decoder**
- Tokenization: **Character-level**
- Training Data: **Custom multilingual parallel dataset**
- Input Format:

<source_lang> <target_lang> <text>

- Output: Translated text in target language

---

## ⚙️ Installation & Setup

### 1️⃣ Create Virtual Environment (Python 3.10 recommended)

```bash
python3.10 -m venv .venv
source .venv/bin/activate

2️⃣ Install Dependencies

pip install -r requirements.txt
pip install python-multipart

🏋️ Model Training

python train.py

After training, the following files will be created:

model/
├── translation_model.h5
└── tokenizer.pkl

🚀 Run the Application
uvicorn app.main:app --reload

Open in browser:

http://127.0.0.1:8000
