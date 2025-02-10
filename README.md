# RAG-CHATBOT-APP

A Retrieval-Augmented Generation (RAG) chatbot application built with Flask, which leverages LM-Studio's REST API for embeddings and model operations. 
The user interface is implemented in HTML/CSS located in the `templates/` directory and assets in the `static/` directory. This project can be easily deployed via Docker and is available on Dockerhub.

### Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Docker Deployment](#docker-deployment)
- [Folder Structure](#folder-structure)
- [License](#license)

### Features

- **Flask REST API:** Serves as the backend for processing user requests.
- **HTML/CSS Frontend:** A clean interface built with HTML/CSS.
- **LM-Studio Integration:** Uses LM-Studio's REST API for embeddings and model inference.
- **Docker Containerization:** Deploy the application in a containerized environment.
- **Testing:** Unit tests are provided under the `tests/` directory.

## Installation & Setup

### Prerequisites

- **Python 3.9+:** [Install Python](https://www.python.org/downloads/)
- **LM-Studio:** [LM-Studio](https://lmstudio.ai/) Ensure LM-Studio is running as a REST API.
- **Git:** For version control.
- **Docker:** (Optional) For containerized deployment.

## 1. Clone the Repository

```
git clone https://github.com/MichaelMA85/chatbot-RAGapp.git
cd chatbot-RAGapp
```
## 2. Set Up Virtual Environment & Install Dependencies

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
### Install the required dependencies:
```
pip install -r requirements.txt
```
## Usage
### Running RAG-ChatBot Application Locally
**Start the Flask server by running:**

```
python app.py
```
Open your browser and navigate to http://127.0.0.1:5000 to interact with the chatbot.

## Links

The RAG-Chatbot is constructed using the deepseek-r1-distill-qwen-7b.

```
https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-7B
```
The Embedding-Model is constructed using the jina-embeddings

```
https://huggingface.co/jinaai/jina-embeddings-v2-base-en
```