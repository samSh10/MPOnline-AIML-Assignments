# 🧠 Deep Learning RAG Assistant

An end-to-end **Retrieval-Augmented Generation (RAG)** application that enables intelligent question answering over the book **Deep Learning with Python**. The project combines semantic search with Google's Gemini LLM to provide accurate, context-aware responses from the indexed document.

---

## ✨ Features

- 📄 PDF document ingestion
- ✂️ Intelligent text chunking
- 🧠 Semantic embeddings using Sentence Transformers
- 🔍 FAISS vector database for similarity search
- 🤖 Google Gemini for answer generation
- 💬 Interactive Streamlit chat interface
- ⚡ Fast semantic retrieval with Retrieval-Augmented Generation (RAG)

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|------------|
| Language | Python |
| Framework | LangChain |
| LLM | Google Gemini 3.1 Flash Lite |
| Embeddings | Sentence Transformers (all-MiniLM-L6-v2) |
| Vector Store | FAISS |
| Frontend | Streamlit |
| PDF Loader | PyPDFLoader |

---

## 📂 Project Structure

```text
Deep-Learning-RAG-Assistant/
│
├── app/
│   ├── chains/
│   ├── embeddings/
│   ├── indexing/
│   ├── llm/
│   ├── loaders/
│   ├── prompts/
│   ├── retriever/
│   ├── splitter/
│   ├── vectorstore/
│   └── config.py
│
├── data/
│   ├── pdfs/
│   └── vectorstore/
│
├── scripts/
│
├── streamlit_app.py
├── requirements.txt
├── README.md
├── .env.example
└── .gitignore
```

---

## ⚙️ Architecture

```
                 PDF Document
                       │
                       ▼
               PDF Loader
                       │
                       ▼
              Text Chunking
                       │
                       ▼
          Sentence Embeddings
                       │
                       ▼
             FAISS Vector Store
                       │
                User Question
                       │
                       ▼
              Similarity Search
                       │
                       ▼
          Retrieved Context Chunks
                       │
                       ▼
              Prompt Template
                       │
                       ▼
             Google Gemini LLM
                       │
                       ▼
                  Final Answer
```

---

## 🚀 Installation

Clone the repository

```bash
git clone https://github.com/samSh10/deep-learning-rag-assistant.git

cd deep-learning-rag-assistant
```

Create a virtual environment

```bash
python -m venv .venv
```

Activate it

### Windows

```bash
.venv\Scripts\activate
```

### Linux / macOS

```bash
source .venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root.

```env
GOOGLE_API_KEY=your_google_api_key
```

---

## 📚 Build the Vector Database

Place your PDF inside

```
data/pdfs/
```

Then run

```bash
python -m scripts.test_indexer
```

This will:

- Load the PDF
- Split it into chunks
- Generate embeddings
- Build the FAISS vector index

---

## ▶️ Run the Application

Launch the Streamlit interface

```bash
streamlit run streamlit_app.py
```

Then open the local URL shown in the terminal.

---

## 💬 Example Questions

- What is backpropagation?
- Explain gradient descent.
- What is overfitting?
- How do convolutional neural networks work?
- What are recurrent neural networks?

---

## 🔮 Future Improvements

- 📑 Multiple PDF support
- 📄 Source page citations
- 💾 Chat memory
- 📤 Upload PDFs from the UI
- 🔀 Hybrid Search (BM25 + FAISS)
- 🎯 Reranking
- 🌐 Deployment on Streamlit Cloud

---

## 👨‍💻 Author

**Sambhav Shrivastava**

GitHub: https://github.com/samSh10

---

## ⭐ If you found this project useful

Give the repository a ⭐ on GitHub!
