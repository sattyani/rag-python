# RAG Python Project

A Retrieval-Augmented Generation (RAG) system built with Python that combines document retrieval with large language models to provide accurate, context-aware responses.

## 🚀 Features

- **Document Retrieval**: Search and retrieve relevant documents from your knowledge base
- **AI-Powered Chat**: Interact with an intelligent assistant that uses retrieved documents to provide accurate answers
- **Multiple Vector Database Support**: Integration with popular vector databases like Pinecone and Vectorize
- **Flexible Interface**: Both CLI and web-based interfaces available
- **Extensible Architecture**: Easy to add new document sources and AI models

## 📋 Prerequisites

- Python 3.13 or higher
- OpenAI API key (for language model access)
- Vector database credentials (Pinecone, Vectorize, or similar)

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sattyani/rag-python.git
   cd rag-python
   ```

2. **Install dependencies**
   ```bash
   # Using pip
   pip install -r requirements.txt
   
   # Or using uv (recommended)
   uv sync
   ```

3. **Set up environment variables**
   Create a `.env` file in the project root:
   ```env
   OPENAI_API_KEY=your-openai-api-key-here
   
   # For Pinecone (optional)
   PINECONE_API_KEY=your-pinecone-api-key
   PINECONE_ENVIRONMENT=your-pinecone-environment
   PINECONE_INDEX_NAME=your-index-name
   
   # For Vectorize (optional)
   VECTORIZE_API_KEY=your-vectorize-api-key
   VECTORIZE_ENDPOINT=your-vectorize-endpoint
   ```

## 🚀 Quick Start

### Basic Usage

```bash
python main.py
```

### Ask Questions

Once running, you can ask questions like:
- "What is machine learning?"
- "Explain the concept of neural networks"
- "How does RAG work?"

## 📁 Project Structure

```
rag-python/
├── main.py              # Main application entry point
├── pyproject.toml       # Project configuration and dependencies
├── README.md           # This file
├── .env                # Environment variables (create this)
├── .gitignore          # Git ignore rules
└── .python-version     # Python version specification
```

## 🔧 Configuration

### Vector Database Setup

The system supports multiple vector database providers:

1. **Pinecone**: Cloud-based vector database
2. **Vectorize**: Vector search service
3. **Local**: In-memory vector storage (for development)

Choose your preferred provider and set up the corresponding environment variables.

### Document Ingestion

To add documents to your knowledge base:

1. Prepare your documents (PDF, TXT, MD formats supported)
2. Run the ingestion script:
   ```bash
   python ingest_documents.py --source /path/to/documents
   ```

## 💡 Usage Examples

### CLI Interface

```bash
# Basic chat
python main.py

# With specific document source
python main.py --source documents/

# Debug mode
python main.py --debug
```

### Python API

```python
from rag_chat import RAGChat

# Initialize the RAG system
rag = RAGChat()

# Ask a question
response = rag.query("What is the capital of France?")
print(response)
```

## 🎯 Use Cases

- **Customer Support**: Build intelligent chatbots that can answer questions based on your documentation
- **Research Assistant**: Query large document collections and get precise answers
- **Knowledge Management**: Create searchable knowledge bases from your internal documents
- **Educational Tools**: Build AI tutors that can answer questions from textbooks and course materials

## 🔍 How It Works

1. **Document Processing**: Documents are split into chunks and converted to embeddings
2. **Vector Storage**: Embeddings are stored in a vector database for fast similarity search
3. **Query Processing**: User questions are converted to embeddings and matched against stored documents
4. **Context Retrieval**: Most relevant document chunks are retrieved
5. **AI Generation**: Language model generates answers using retrieved context

## 🛡️ Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `OPENAI_API_KEY` | Yes | OpenAI API key for language model access |
| `PINECONE_API_KEY` | Optional | Pinecone API key (if using Pinecone) |
| `PINECONE_ENVIRONMENT` | Optional | Pinecone environment |
| `PINECONE_INDEX_NAME` | Optional | Pinecone index name |
| `VECTORIZE_API_KEY` | Optional | Vectorize API key (if using Vectorize) |
| `VECTORIZE_ENDPOINT` | Optional | Vectorize endpoint URL |

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenAI](https://openai.com/) for providing the language model APIs
- [Pinecone](https://www.pinecone.io/) for vector database services
- [Vectorize](https://vectorize.io/) for vector search capabilities

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/sattyani/rag-python/issues) page
2. Create a new issue with detailed information about your problem
3. Join our community discussions

---

**Built with ❤️ for the AI Engineering Bootcamp**
