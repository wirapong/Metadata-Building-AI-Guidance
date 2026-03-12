# Metadata-Building-AI-Guidance

AI-powered document metadata extraction and semantic question-answering system for research documents.

This project provides an interactive **Streamlit-based platform** that allows users to upload research documents, automatically generate structured metadata, and perform semantic search and question answering over the document content using OpenAI embeddings and large language models.

The system is designed to support **AI-driven metadata construction, digital knowledge organization, and research document analysis**, which can be applied in digital libraries, knowledge graphs, and scholarly information systems.

---

# Features

* Upload multiple document formats
* Automatic metadata extraction
* Semantic document embeddings
* Context-aware question answering
* Metadata export to CSV
* Interactive Streamlit interface

Supported file formats:

* PDF
* DOCX
* TXT
* CSV
* JSON
* Markdown
* HTML
* Python files

---

# System Architecture

The system follows a **Retrieval-Augmented Generation (RAG)** pipeline:

```
Document Upload
      │
      ▼
Text Extraction
      │
      ▼
Text Chunking
      │
      ▼
Embedding Generation
      │
      ▼
Vector Similarity Retrieval
      │
      ▼
Context Construction
      │
      ▼
LLM-based Question Answering
```

Metadata extraction is performed separately using a prompt-based LLM workflow.

---

# Project Structure

```
Metadata-Building-AI-Guidance/
│
├── app.py
├── utils.py
├── requirements.txt
└── README.md
```

### `app.py`

Main Streamlit application that manages:

* document upload
* metadata generation
* semantic search
* user interface

See the application implementation here:


---

### `utils.py`

Core backend utilities for:

* text extraction from documents
* text chunking
* embedding generation
* similarity retrieval
* metadata extraction
* question answering

Functions include:

```
extract_text()
chunk_text()
build_embeddings()
retrieve_context()
generate_metadata()
answer_query()
```

Source code:


---

### `requirements.txt`

Dependencies required to run the application.

Includes libraries such as:

* Streamlit
* OpenAI
* pandas
* numpy
* scikit-learn
* networkx
* pypdf
* python-docx
* tiktoken

See the dependency file here:


---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/metadata-building-ai-guidance.git
cd metadata-building-ai-guidance
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# OpenAI API Setup

Create a **Streamlit secrets file**:

```
.streamlit/secrets.toml
```

Add your API key:

```toml
OPENAI_API_KEY="your-openai-api-key"
```

---

# Running the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

Then open the browser:

```
http://localhost:8501
```

---

# Usage

### Step 1 — Upload Documents

Upload one or more documents through the interface.

The system will:

* extract text
* split into chunks
* generate embeddings
* index the documents

---

### Step 2 — Metadata Generation

After indexing, the system automatically extracts metadata including:

* Title
* Authors
* Keywords
* Summary
* Named entities

Metadata can be downloaded as:

```
metadata.csv
```

---

### Step 3 — Ask Questions

Users can ask questions about uploaded documents.

Example queries:

```
What is the main contribution of this paper?
Summarize the methodology.
What datasets were used?
Who are the authors?
```

The system retrieves relevant context using embeddings and generates answers using an LLM.

---

# Example Metadata Output

```json
{
  "title": "Ontology-Based Semantic Retrieval for Museum News Systems",
  "authors": ["Author A", "Author B"],
  "keywords": ["ontology", "semantic retrieval", "museum information systems"],
  "summary": "This paper proposes a semantic retrieval framework...",
  "entities": ["museum ontology", "SPARQL", "knowledge graph"]
}
```

---

# Potential Applications

* Digital libraries
* Research knowledge graphs
* Academic metadata extraction
* Research paper summarization
* Semantic document search
* Institutional repositories
* Cultural heritage knowledge systems

---

# Future Improvements

Planned extensions include:

* GraphRAG integration
* knowledge graph construction
* citation extraction
* PDF layout understanding
* multi-document summarization
* ontology-based metadata alignment
* vector database integration (FAISS / Chroma / Weaviate)

---

# Research Context

This system can support research in:

* Knowledge Organization Systems (KOS)
* Knowledge Graphs
* Semantic Metadata
* AI-driven Digital Libraries
* Retrieval-Augmented Generation (RAG)

---

# License

MIT License

---

# Citation

If you use this system in research, please cite:

```
Chansanam, W. (2026).
Metadata-Building-AI-Guidance: AI-driven metadata extraction and semantic search system.
GitHub Repository.
```

---

If you want, I can also **upgrade this README to a top-tier research software style**, including:

* badges (Python / Streamlit / OpenAI)
* architecture diagram
* GraphRAG roadmap
* citation section for papers
* DOI-ready README for Zenodo.
