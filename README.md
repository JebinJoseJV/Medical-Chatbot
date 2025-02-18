# Medical Chatbot

## Overview
This medical chatbot is designed to answer medical queries by leveraging a document-based retrieval system powered by FAISS and a large language model (LLM). The system processes medical documents, stores them in a vector database, and retrieves relevant information to answer user queries.

## Features
- **Document Processing**: Extracts text from medical PDFs and stores embeddings in a FAISS vector database.
- **Question Answering**: Uses a retrieval-augmented generation (RAG) approach to provide precise answers.
- **Customizable Prompting**: Ensures responses are context-aware and avoids generating misleading information.
- **Streamlit UI**: Provides an interactive interface for user queries.

## Installation

### Prerequisites
- Python 3.8+
- Virtual environment (optional but recommended)

### Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/JebinJoseJV/Medical-Chatbot
   cd medical-chatbot
   ```
2. Create a virtual environment and activate it:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   - Create a `.env` file and add your API key:
     ```
     GROQ_API_KEY=<your_api_key>
     ```

## Usage

### Step 1: Create the Knowledge Base
Run the following script to process and store medical documents:
```sh
python create_memory.py
```

### Step 2: Query the Knowledge Base via CLI
You can test the chatbot using a command-line interface:
```sh
python connect_memory.py
```

### Step 3: Launch the Web Application
Start the Streamlit web app:
```sh
streamlit run app.py
```

## Project Structure
```
medical-chatbot/
│── data/                     # Directory containing medical PDFs
│── vectorstore/              # FAISS vector database storage
│── create_memory.py          # Script to process PDFs and store embeddings
│── connect_memory.py         # CLI-based chatbot interface
│── app.py                    # Streamlit web application
│── requirements.txt          # List of dependencies
│── README.md                 # Project documentation
```

## Technologies Used
- **LangChain**: Handles document processing and retrieval-based question answering.
- **FAISS**: Stores and retrieves document embeddings efficiently.
- **Hugging Face Transformers**: Provides sentence embeddings for document storage and retrieval.
- **Groq API**: Uses an advanced LLM for answering queries.
- **Streamlit**: Creates an interactive web interface.

## Future Enhancements
- Support for more document formats (e.g., DOCX, TXT)
- Integration with additional LLMs for improved accuracy
- Cloud-based deployment (AWS, GCP, or Azure)

## License
This project is open-source and available under the [MIT License](LICENSE).



