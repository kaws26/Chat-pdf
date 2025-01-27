# Conversational RAG with PDF Uploads and Chat History

## Overview
This project demonstrates a Conversational Retrieval-Augmented Generation (RAG) application built using Streamlit and LangChain. It enables users to upload PDF files, extract their content, and interact with the extracted information through a conversational interface. The application also supports maintaining chat history for contextualized question answering.

## Features
- **PDF Uploads**: Upload one or more PDF documents.
- **Text Splitting**: Use `RecursiveCharacterTextSplitter` to split document content for efficient processing.
- **Embeddings and Vector Store**: Generate embeddings using HuggingFace's `all-MiniLM-L6-v2` model and store them in a Chroma vector store.
- **Contextualized Question Answering**: Answer user queries based on document content and chat history.
- **Chat History Management**: Preserve conversation context for personalized interactions.

## Tech Stack
- **Streamlit**: Frontend framework for building the web application.
- **LangChain**: Framework for managing LLM-powered chains and tools.
- **HuggingFace**: Embeddings using `all-MiniLM-L6-v2`.
- **Chroma**: Vector database for efficient document retrieval.
- **ChatGroq**: LLM for conversational responses.
- **Python**: Core programming language for backend and logic.

## Prerequisites
Ensure you have the following installed:
- Python 3.8+
- `pip` (Python package manager)
- A HuggingFace token (set as `HF_TOKEN` in the `.env` file)
- A Groq API key (set as `GROQ_API_KEY` in the `.env` file)

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo-name/conversational-rag.git
   cd conversational-rag
   ```

2. **Set Up Environment Variables**:
   Create a `.env` file in the project root and add the following:
   ```env
   HF_TOKEN=your_huggingface_token
   GROQ_API_KEY=your_groq_api_key
   ```

3. **Install Dependencies**:
   Use the `requirements.txt` file to install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**:
   Start the Streamlit app:
   ```bash
   streamlit run app.py
   ```

## Usage
1. Open the application in your browser (usually at `http://localhost:8501`).
2. Upload one or more PDF files using the file uploader.
3. Ask questions based on the content of the uploaded documents.
4. View responses and chat history in the interface.

## File Structure
```plaintext
.
├── app.py                 # Main application file
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (not tracked in Git)
├── chroma_store/          # Directory to persist Chroma vector store
├── temp.pdf               # Temporary storage for uploaded PDFs
└── README.md              # Project documentation
```

## Key Components
- **`PyPDFLoader`**: Parses and loads PDF content.
- **`RecursiveCharacterTextSplitter`**: Splits document text into manageable chunks.
- **`HuggingFaceEmbeddings`**: Creates vector embeddings for text chunks.
- **`Chroma`**: Stores and retrieves embeddings for efficient question answering.
- **`ChatMessageHistory`**: Manages chat context for personalized interactions.

## Environment Variables
| Variable         | Description                                  |
|------------------|----------------------------------------------|
| `HF_TOKEN`       | Your HuggingFace API token                  |
| `GROQ_API_KEY`   | Your Groq API key for the conversational LLM|

## Dependencies
All required packages are listed in `requirements.txt`. Install them using:
```bash
pip install -r requirements.txt
```

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any improvements.

## Contact
For any questions or issues, please contact [kawaljeetsingh0026@gmail.com](mailto:kawaljeetsingh0026@gmail.com).

