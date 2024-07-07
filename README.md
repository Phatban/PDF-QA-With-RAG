# RAG for Document Question Answering

This repository contains the implementation of a Retrieval Augmented Generation (RAG) system for Question Answering on documents. The system allows users to upload a PDF or text file, ask questions about the content, and receive relevant answers extracted from the document.

## Project Structure

The project is organized into two Jupyter Notebook files:

1. `RAG_Without_UI.ipynb`: Implements the core RAG functionality without a user interface.
2. `RAG_With_ChatUI.ipynb`: Integrates the RAG system with a chat-based user interface using the Chainlit library.

## RAG System Overview

The RAG system follows these main steps:

1. Document Processing:
   - The input document (PDF or text) is loaded and split into smaller chunks using a text splitter.
   - Each chunk is considered as a separate document in the database.

2. Vectorization:
   - The text documents are converted into vector representations using an embedding model.
   - This allows for efficient similarity search and retrieval.

3. Vector Database:
   - The vectorized documents are stored in a vector database (Chroma) for fast retrieval.
   - The database is used to find the most relevant documents based on the user's question.

4. Large Language Model (LLM):
   - The Vicuna model is used as the LLM for generating answers.
   - The model is loaded and configured to run efficiently on the available hardware.

5. Question Answering:
   - The user inputs a question related to the document.
   - The system retrieves the most relevant documents from the vector database.
   - The retrieved documents, along with the question, are passed to the LLM.
   - The LLM generates an answer based on the provided context.

## Usage

### RAG Without UI

1. Open the `RAG_Without_UI.ipynb` notebook in Jupyter.
2. Install the required dependencies as mentioned in the notebook.
3. Run the notebook cells in sequential order.
4. When prompted, provide the path to your PDF or text file.
5. Enter a question related to the document.
6. The system will generate an answer based on the relevant content from the document.

### RAG With Chat UI

1. Open the `RAG_With_ChatUI.ipynb` notebook in Jupyter.
2. Install the required dependencies, including the Chainlit library.
3. Run the notebook cells in sequential order.
4. The notebook will provide a URL for accessing the chat interface.
5. Open the URL in a web browser.
6. Upload a PDF or text file using the chat interface.
7. Ask questions related to the uploaded document.
8. The system will generate answers and display them in the chat interface.

## Dependencies

The project requires the following main dependencies:

- Python 3.x
- PyTorch
- Transformers
- LangChain
- Chroma
- Chainlit (for the chat UI)

Please refer to the notebooks for the complete list of dependencies and installation instructions.

## Acknowledgements

This project was developed as part of the AI Vietnam (AIO2024) course. It utilizes various open-source libraries and models, including Vicuna, LangChain, and Chainlit. We extend our gratitude to the developers and contributors of these projects.
