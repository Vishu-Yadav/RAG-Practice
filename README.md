# RAG Practice

A comprehensive learning project for Retrieval Augmented Generation (RAG) using LangChain, ChromaDB, and various LLM providers.

## About This Project

This project explores RAG implementations at various levels of complexity, progressing from basic RAG setups to advanced multi-document retrieval systems with persistent vector storage.

## Project Structure

```
├── 01_RAG/                          # Tutorial notebooks
│   ├── 01_rag.ipynb                # Basic RAG implementation
│   ├── 02_rag_with_pdf.ipynb       # RAG with PDF document processing
│   ├── 03_rag_local_persist.ipynb  # RAG with persistent local storage
│   └── 04_rag_multi_docs.ipynb     # RAG with multiple documents
├── Vector/                          # Vector database storage
│   ├── chroma.sqlite3              # ChromaDB persistent database
│   └── [embedding collections]     # Document embeddings
├── DOCS/                           # Documentation folder
├── main.py                         # Main application entry point
├── pyproject.toml                  # Project dependencies and configuration
└── README.md                       # This file
```

## Features

- **Basic RAG**: Introduction to retrieval augmented generation
- **PDF Processing**: Learn how to extract and process PDF documents
- **Persistent Storage**: Store vector embeddings locally using ChromaDB
- **Multi-Document Retrieval**: Handle queries across multiple documents
- **LLM Integration**: Support for Google Generative AI and OpenAI models

## Dependencies

The project uses the following key libraries:

- **LangChain** (>=1.2.6) - LLM framework and RAG utilities
- **LangChain Community** (>=0.4.1) - Community integrations
- **LangChain Google GenAI** (>=4.2.0) - Google Generative AI integration
- **LangChain OpenAI** (>=1.1.7) - OpenAI API integration
- **ChromaDB** (>=1.4.1) - Vector database for storing embeddings
- **PyPDF** (>=6.6.0) - PDF processing
- **python-dotenv** (>=0.9.9) - Environment variable management

## Getting Started

### Prerequisites

- Python 3.10 or higher

### Installation

1. Clone or download this project
2. Install dependencies:
   ```bash
   pip install -e .
   ```

3. Set up environment variables:
   - Create a `.env` file in the project root
   - Add your API keys:
     ```
     GOOGLE_API_KEY=your_google_api_key
     OPENAI_API_KEY=your_openai_api_key
     ```

### Running the Project

To run the main application:

```bash
python main.py
```

To explore the tutorials, open the Jupyter notebooks in the `01_RAG/` directory:

```bash
jupyter notebook 01_RAG/
```

## Tutorials Overview

1. **01_rag.ipynb** - Start here! Learn the fundamentals of RAG systems
2. **02_rag_with_pdf.ipynb** - Process PDF documents and use them as knowledge sources
3. **03_rag_local_persist.ipynb** - Persist embeddings locally for faster retrieval
4. **04_rag_multi_docs.ipynb** - Scale up to handle multiple documents efficiently

## Vector Database

The project uses **ChromaDB** for vector storage:
- Local persistent storage in `Vector/` directory
- Automatic indexing and retrieval of document embeddings
- Efficient similarity search for RAG queries

## Use Cases

- Document Q&A systems
- Knowledge base search
- Multi-document information retrieval
- LLM augmentation with custom knowledge

## License

This is a learning project for RAG practice.

## Notes

- Ensure your API keys are properly configured before running any notebooks that use external LLMs
- The vector database will be created automatically in the `Vector/` directory
- Each notebook is self-contained and can be run independently
