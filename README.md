# 🧠 Advanced RAG Pipeline with LangChain, Zilliz, and OpenAI

This project demonstrates a Retrieval-Augmented Generation (RAG) system that extracts and indexes content from PDFs (including both text and tables), stores the embeddings in a Zilliz vector database, and performs intelligent question answering using OpenAI's GPT models.

## 📁 Project Structure

```
Assignment_2/
│
├── uploaded_files/        # Folder containing input PDF documents
├── Assignment_2.ipynb     # Jupyter Notebook with full RAG pipeline implementation
└── .env                   # Environment variables for API keys
```

## ⚙️ Features

- ✅ PDF parsing with `pdfplumber` (text + tables)
- ✅ Text chunking using `RecursiveCharacterTextSplitter`
- ✅ Embedding with `OpenAIEmbeddings`
- ✅ Vector storage with `Zilliz` (Milvus)
- ✅ Question answering via `LangChain` + `ChatOpenAI`
- ✅ Export to DOCX using `python-docx`

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/YourUsername/Assignment_2.git
cd Assignment_2
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

> ✅ Ensure `pymilvus`, `pdfplumber`, `langchain`, `openai`, and `python-docx` are included in `requirements.txt`.

### 3. Set Environment Variables

Create a `.env` file with the following variables:

```env
ZILLIZ_HOST=your_zilliz_host
ZILLIZ_API_KEY=your_zilliz_api_key
OPENAI_API_KEY=your_openai_key
```

### 4. Run the Notebook

Launch the notebook:

```bash
jupyter notebook Assignment_2.ipynb
```

The notebook will:
- Load PDF files from `uploaded_files/`
- Extract text and tables
- Generate embeddings and upload to Zilliz
- Run a QA loop using LangChain and OpenAI

## 🛠️ Tech Stack

- **LangChain** – Orchestration of RAG components
- **Zilliz/Milvus** – Vector database for semantic search
- **OpenAI GPT** – LLM for intelligent responses
- **pdfplumber** – PDF parsing for both text and tables
- **python-docx** – For final document generation

## 📌 Future Improvements

- Add support for image-based tables using OCR
- Implement metadata filtering in vector search
- Enable multi-modal chunk ranking with reranking (e.g., MMR, BM25)

## 👤 Author

Mohsen Zeinali – [GitHub](https://github.com/Nahidzeinali-web)


---

### 📦 `requirements.txt`
```
langchain
openai
pymilvus
pdfplumber
python-dotenv
python-docx

```
