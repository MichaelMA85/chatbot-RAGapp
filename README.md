# RAG-CHATBOT-APP

A Retrieval-Augmented Generation (RAG) chatbot application built with Flask, leveraging LM-Studio's REST API for embeddings and model operations.  
The user interface is implemented in HTML/CSS, with assets in the `templates/` and `static/` directories. Easily deployable via Docker.

---

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Folder Structure](#folder-structure)
- [License](#license)

---

## Features

- **Flask REST API**: Backend for processing user requests.
- **HTML/CSS Frontend**: Clean and responsive interface.
- **LM-Studio Integration**: REST API for embeddings and model inference.
- **Docker Support**: Containerized deployment.
- **Testing**: Unit tests in the `tests/` directory.

---

## Prerequisites

- **Python 3.9+**: [Download Python](https://www.python.org/downloads/)
- **LM-Studio**: [Download LM-Studio](https://lmstudio.ai/) (required for local model hosting).
- **Git**: For cloning the repository.
- **Docker** (optional): For containerized deployment.

---

## Installation

### 1. Clone the Repository

```
git clone https://github.com/MichaelMA85/chatbot-RAGapp.git
cd chatbot-RAGapp
```
## 2. Set Up Virtual Environment

### Create a virtual environment (recommended):

```
python -m venv venv
```

### Activate the virtual environment:
***On Linux/macOS:***
```
source venv/bin/activate
```
***On Windows:***
```
venv/bin/activate
```
## 3. Install Dependencies
```
pip install -r requirements.txt
```

## 4. Set Up LM-Studio

1. **Install LM-Studio**:
   - Download and install LM-Studio from [LM-Studio](https://lmstudio.ai/).

2. **Load Models in LM-Studio**:
   - Open LM-Studio and load your models:
     - **My Chat Model**: [`deepseek-r1-distill-qwen-7b`](https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-7B)
     - **My Embedding Model**: [`jina-embeddings-v2-base-en`](https://huggingface.co/jinaai/jina-embeddings-v2-base-en)

3. **Enable REST API in LM-Studio**:
   - Go to **Developer Settings** in LM-Studio.
   - Enable the **REST API** and note the API URL (default: `http://localhost:1234`).

4. **Update `config.py`**:
   - Open the `config.py` file and ensure the following settings match your LM-Studio configuration:
     ```python
     LM_STUDIO_API_URL = "http://localhost:1234/v1/chat/completions"
     LM_STUDIO_EMBEDDING_API_URL = "http://localhost:1234/v1/embeddings"
     # Name must match LM-Studio's model
     EMBEDDING_MODEL_NAME = "jina-embeddings"
     CHAT_MODEL_NAME = "deepseek-r1-distill-qwen-7b"
     ```
 

---

## Usage

### Running RAG-ChatBot Application Locally

1. **Start the Flask Server**:
   - Run the following command in your terminal:
     ```
     "python app.py"
     ```

2. **Access the Application**:
   - Open your browser and navigate to [http://127.0.0.1:5000](http://127.0.0.1:5000) to interact with the chatbot.

---

## Folder Structure

chatbot-RAGapp/
├── html/               # chat.html for the frontend
├── static/             # Static assets (CSS, JS, etc.)
├── tests/              # Unit tests
├── app.py              # Flask application entry point
├── utils.py            # Utilities
├── config.py           # Configuration settings
├── requirements.txt    # Python dependencies
├── Dockerfile          # Docker configuration
└── README.md           # Project documentation


## Links

The RAG-Chatbot is constructed using the deepseek-r1-distill-qwen-7b.

```
https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-7B
```
The Embedding-Model is constructed using the jina-embeddings

```
https://huggingface.co/jinaai/jina-embeddings-v2-base-en
```
