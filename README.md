# AIPyChat
This project is a Streamlit application that allows users to upload PDF documents and ask questions about the content. The app leverages OpenAI’s GPT-3.5-turbo model to generate responses based on the content of the uploaded PDFs.

---

## Features

- **PDF Upload**: Users can upload PDF documents through the sidebar.
- **Text Extraction**: The text from the uploaded PDFs is extracted.
- **Text Chunking**: The extracted text is split into manageable chunks for processing.
- **Embedding Generation**: The text chunks are converted into embeddings using OpenAI's embeddings.
- **Vector Store Creation**: A FAISS vector store is created from the embeddings for efficient similarity search.
- **Question Answering**: Users can input questions, which are answered based on the content of the uploaded PDFs using OpenAI's GPT-3.5-turbo model.



## Demo


https://github.com/user-attachments/assets/73ba5d73-9739-496f-a9ba-20e5e3b329a1








## Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/vineetsansare/AIPyChat.git   
   ```

2. Create a virtual environment and activate it:
   ```sh
   python3 -m venv env
   source env/bin/activate
   ```

3. Install the required packages:
   ```sh
   pip install -r requirements.txt
   ```

4. Set up your OpenAI API key:
   - Replace `OPENAI_API_KEY` in the code with your actual OpenAI API key.

## Usage

1. Run the Streamlit app:
   ```sh
   streamlit run app.py
   ```

2. Upload a PDF file through the sidebar.

3. Ask questions related to the content of the uploaded PDF in the provided text input field.

## Code Overview

The main components of the code are:

- **PDF Upload**: Uses Streamlit's `file_uploader` to upload PDF files.
- **Text Extraction**: Utilizes `PyPDF2.PdfReader` to extract text from the uploaded PDF.
- **Text Chunking**: Employs `RecursiveCharacterTextSplitter` to split the extracted text into chunks.
- **Embedding Generation**: Uses `OpenAIEmbeddings` to generate embeddings from the text chunks.
- **Vector Store Creation**: Creates a FAISS vector store from the embeddings for efficient similarity search.
- **Question Answering**: Uses `ChatOpenAI` and `load_qa_chain` to answer user questions based on the relevant text chunks.

## Dependencies

- streamlit
- PyPDF2
- langchain
- langchain_community
- faiss-cpu (or faiss-gpu for GPU support)
