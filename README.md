# 🧠 RAG-Based Question Answering System (FAISS + Groq)

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline that enables users to query custom documents and receive accurate, context-aware answers.

It combines **semantic search (FAISS)** with **fast LLM inference (Groq)** to build an efficient and scalable document question-answering system.

---

## 🚀 Features

* 📄 Supports **PDF and text document ingestion**
* 🔍 **Semantic search** using FAISS vector database
* 🧠 Embeddings via `all-MiniLM-L6-v2`
* ⚡ Fast LLM responses using Groq (`llama-3.1-8b-instant`)
* 📊 Returns **sources + similarity scores**
* 🧩 Modular and extensible architecture
* 🗂️ Persistent vector storage

---

## 🏗️ Project Structure

```
RAG-PROJECT/
│── src/
│   ├── data_loader.py
│   ├── embedding.py
│   ├── vectorstore.py
│   ├── search.py
│
│── Data/
│   ├── pdf/
│   ├── text_files/
│
│── faiss_store/        # Vector DB (ignored in git)
│── notebook/           # Experiment notebooks
│
│── app.py              # Main execution script
│── main.py
│── requirements.txt
│── .env                # API keys (not committed)
│── README.md
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```
git clone https://github.com/YOUR_USERNAME/rag-groq-project.git
cd rag-groq-project
```

---

### 2️⃣ Create virtual environment

```
python -m venv .venv
source .venv/bin/activate   # Linux/Mac
.venv\Scripts\activate      # Windows
```

---

### 3️⃣ Install dependencies

```
pip install -r requirements.txt
```

---

### 4️⃣ Setup environment variables

Create a `.env` file in the root directory:

```
GROQ_API_KEY=your_api_key_here
```

---

## ▶️ Running the Project

```
python app.py
```

Example query:

```
What is CNN?
```

---

## 🔄 How It Works

1. Documents (PDF/Text) are loaded and split into chunks
2. Chunks are converted into embeddings
3. Embeddings are stored in FAISS vector database
4. User query is converted into embedding
5. Top relevant chunks are retrieved
6. Context is passed to Groq LLM
7. Final answer is generated

---

## 🧠 Tech Stack

* Python
* LangChain
* FAISS
* Sentence Transformers
* Groq API

---

## 📌 Use Cases

* 📚 Study material Q&A
* 🏢 Internal knowledge base assistant
* 📄 Document search systems
* 🤖 AI-powered chat over custom data

---

## ⚠️ Notes

* `.env`, `.venv`, and `faiss_store/` are excluded from Git
* Make sure to use **latest Groq models** (e.g., `llama-3.1-8b-instant`)
* First run may take time to build vector database

---

## ✨ Future Improvements

* Streamlit / Web UI
* Chat interface with memory
* Multi-document summarization
* API deployment

---

## 👨‍💻 Author

Harsh Bhatt

---

## ⭐ If you found this useful

Give it a star ⭐ on GitHub!
