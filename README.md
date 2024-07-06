# PDF Question Answering with RAG

This project implements a Retrieval Augmented Generation (RAG) system to answer questions based on the content of a PDF document.

## Features
- Uploads PDF or plain text files
- Answers questions about the content of the uploaded file
- Provides source information for the answers

## Getting Started

### Prerequisites
- Python 3.7+
- GPU (recommended for faster response times)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Phatban/PDF-QA-With-RAG.git
2. Install the required dependencies:
   ```bash
   cd PDF-QA-With-RAG
   pip install -r requirements.txt
### Usage
1. Run the Chainlit app:
   ```bash
   chainlit run app.py --host 0.0.0.0 --port 8000
2. Open the app in your browser by visiting the URL provided in the console.
3. Upload a PDF or text file, then ask questions about its content.

## Architecture
The system is composed of the following components:

1. **File Processing**: Handles the loading and splitting of the input file into smaller documents.
2. **Vector Database**: Creates and manages the Chroma vector database for efficient retrieval of relevant documents.
3. **Language Model**: Loads and configures the Vicuna language model for generating answers.
4. **RAG System**: Integrates the vector database and language model to provide the final question-answering functionality.
5. **Chainlit App**: Provides the web-based user interface for interacting with the system.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
