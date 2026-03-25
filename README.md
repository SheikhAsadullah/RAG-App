# 🧠 RAG Application with LangChain

An end-to-end **Retrieval-Augmented Generation (RAG)** application built using **LangChain**, enabling intelligent question answering over custom datasets using semantic search and large language models.

This project demonstrates how to build a scalable and modular RAG pipeline — from document ingestion to contextual response generation.

---

## 🚀 Key Features

- 🔍 Semantic search over custom documents  
- 🧠 End-to-end RAG pipeline implementation  
- 📦 Vector database powered by ChromaDB  
- 🔗 Modular architecture using LangChain  
- ⚡ Fast and efficient embedding-based retrieval  
- 🧪 Simple CLI-based querying system  

---

## 🏗️ System Architecture

The application follows a standard RAG workflow:

### 1. Document Ingestion
- Loads raw documents from the `data/` directory

### 2. Text Processing
- Splits documents into manageable chunks
- Converts text into embeddings using LLM-based models

### 3. Vector Storage
- Stores embeddings in a local **ChromaDB** vector database

### 4. Query Pipeline
- Accepts user queries
- Retrieves relevant chunks using similarity search
- Passes context + query to an LLM for final response generation

---

## 📂 Project Structure

| File / Folder            | Description                                  |
|-------------------------|----------------------------------------------|
| `data/`                 | Input documents for indexing                 |
| `chroma/`               | Auto-generated vector database (ignored)     |
| `create_database.py`    | Script to build vector store                 |
| `query_data.py`         | Script to query indexed data                 |
| `requirements.txt`      | Project dependencies                         |
| `README.md`             | Project documentation                        |
| `LICENSE`               | License details                              |
| `.gitignore`            | Ignored files configuration                  |

## ⚙️ Setup & Installation

### 1️⃣ Clone the Repository

```bash
git clone <your-repo-url>
cd RAG-Application-with-LangChain
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

Activate environment:

```bash
# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Configuration

Create a `.env` file in the root directory:

```env
OPENAI_API_KEY=your_api_key_here
```

⚠️ Important:

* Never commit `.env` files
* Already included in `.gitignore`

---

## 🧱 Build Vector Database

Before querying, index your documents:

```bash
python create_database.py
```

This step:

* Loads documents from `data/`
* Splits text into chunks
* Generates embeddings
* Stores them in ChromaDB

---

## ❓ Query the System

Run the query script:

```bash
python query_data.py
```

### Example:

```
> What is this document about?
```

💡 The system:

* Retrieves relevant document chunks
* Sends context to the LLM
* Generates an accurate, contextual answer

---

## 🧪 Best Practices

* Re-run `create_database.py` when documents change
* Keep `chroma/` directory out of version control
* Use clean and structured input data for better results

---

## 🚀 Future Improvements

* 🌐 Web UI (Streamlit / FastAPI)
* 📄 Support for PDFs, URLs, APIs
* ☁️ Integration with cloud vector DBs (Pinecone, Weaviate)
* 🔐 Authentication & multi-user support
* ⚡ Caching for faster retrieval
* 🐳 Docker-based deployment

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Sheikh Asadullah**
GitHub: [https://github.com/SheikhAsadullah](https://github.com/SheikhAsadullah)

---

## ⭐ Acknowledgements

* LangChain
* ChromaDB
* OpenAI
* Open-source AI community

---

## 💡 About This Project

This project is designed to demonstrate practical implementation of:

* Retrieval-Augmented Generation (RAG)
* Vector databases
* LLM-powered applications

Ideal for:

* AI/ML portfolios
* Interviews
* Learning real-world GenAI systems

