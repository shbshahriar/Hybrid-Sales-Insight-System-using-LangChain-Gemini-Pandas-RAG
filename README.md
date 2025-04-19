
# 🔮 Hybrid Sales Insight System using LangChain + Gemini + Pandas + RAG

This project is a smart hybrid system for **sales data analysis** that combines:
- 🤖 **LLM-based code execution** (via Gemini + Pandas agent) for structured queries
- 📚 **Retrieval-Augmented Generation (RAG)** (via Chroma + Gemini) for unstructured insights

📊 Designed for extracting **actionable business intelligence** from historical sales datasets — dynamically, flexibly, and intelligently.

---

## 🚀 Features

- 📁 Google Drive integration for easy file access on Colab.
- ⚡ Fast LLM reasoning with **Google Gemini 2.0 Flash Lite**.
- 🧮 **Pandas agent** for Python-powered numeric and tabular analysis.
- 🔍 **RAG pipeline** using vector search + Gemini for rich text generation.
- 🔄 **Automatic query routing** based on keyword analysis.
- 📚 Vector-based document retrieval with **ChromaDB** and **Google Embeddings**.

---

## 🛠️ Setup

1. **Mount Google Drive**

```python
from google.colab import drive
drive.mount('/content/drive')
```

2. **Install Dependencies**

```bash
!pip install -r '/path/to/your/requirements.txt'
!pip install langchain-experimental
```

3. **Set Your API Key**

```python
import os
os.environ['GOOGLE_API_KEY'] = "your-google-api-key-here"
```

---

## ⚙️ How It Works

Your query is routed to the right engine based on its intent:

| Query Type      | Routed To           | Example                                      |
|-----------------|---------------------|----------------------------------------------|
| Structured      | Pandas Agent        | `"What is the average sales per branch?"`    |
| Unstructured    | RAG Chain (Gemini)  | `"Describe the sales pattern in the data"`   |

Keyword-based routing logic powers this intelligent flow.

---

## 📂 Project Structure

```
├── Dataset.csv                     # Your sales transaction dataset
├── requirements.txt                # All Python dependencies
├── your_script.ipynb/.py           # Full hybrid logic and model setup
├── chroma_db/                      # Vector DB for document embeddings
```

---

## 🔍 Example Queries

```python
# Structured (Pandas agent)
hybrid_answer("What is the average sales amount per branch?")

# Unstructured (RAG)
hybrid_answer("Describe the sales pattern")

# Time-based insights (RAG)
hybrid_answer("Describe year base sales for all outlet")
```

---

## 🧠 Tech Stack

- 🧠 **LangChain Core + Experimental**
- 🔗 **ChromaDB** (vector database)
- 🤖 **Gemini 2.0 Flash Lite**
- 🐼 **Pandas** (tabular data analysis)
- 🔎 **GoogleGenerativeAIEmbeddings**
- ☁️ **Google Colab + Drive**

---

## ✨ Author

**Md. Shihab Shahriar**  
MScSE Student | AI Enthusiast  
📧 mshahriar2510015@mscse.uiu.ac.bd

---

## 🧭 Roadmap / To-Do

- 🧠 Replace keyword-based routing with LLM-based classifier
- 📈 Integrate dynamic charting (Matplotlib/Plotly)
- 🔐 Deploy via REST API or Streamlit app
- ⚙️ Add CLI support for offline usage

---

## 📜 License

Open-source under the [MIT License](LICENSE).

