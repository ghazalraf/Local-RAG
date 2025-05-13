# Local-RAG

This project lets you run a local Retrieval-Augmented Generation (RAG) application using Langchain and Ollama. 

Alternatively, if you have Docker installed, you can create a simple local RAG/GenAI chat by following these instructions: https://github.com/open-webui/open-webui (You can still use Ollama for running local, open-source LLMS).

For better LLM results, use Open AI API. Reference Alejandro-AO's repo that was the inspiration for this project: https://github.com/alejandro-ao/ask-multiple-pdfs 

## Setup Instructions
### 1. ✅ Install Ollama 

  Download and install Ollama from the official website:

  🔗 https://www.ollama.com/download

  Make sure it's installed and running in the background (the server usually starts automatically).

### 2. 🐍 Ensure you have Python 3.10+  

  Make sure you're using Python 3.10 or higher in your development environment (VS Code, Cursor, etc.).

  You can check with:
  ``` python3 --version```

### 3. 📨 Create and Activate a Virtual Environment 

  Open terminal in your IDE and run:
  ```
  python3 -m venv .venv
  source .venv/bin/activate  # On Windows, use `.venv\Scripts\activate`
  ````

### 4. 📦 Add Requirements:

  Create a requirements.txt file in your project folder. Copy the contents from requirements.txt within this repo and save.

### 5. 📩 Install all dependencies:

  Run the following command to install all the required packages:
  ```pip install -r requirements.txt```

### 6. 🧠 Pull the required Ollama Models:

  Still inside your IDE terminal (with the virtual environment activated), run:
  ```ollama pull mistral && ollama pull nomic-embed-text```

  Let the installation complete before moving to next step. 
  Instead of Mistral, if you want to download/test other models, find their respective pull command from [the ollama.](https://www.ollama.com/search).

### 7. 📑 Add the main code files:

  Create two files in your project folder
  * `main.py`
  * `htmlTemplates.py`

  Then paste the contents from your respective source files into each of them.

### 8. ▶️ Run the Streamlit App:

  Once everything is installed and all models are downloaded, launch the RAG app with:
  ```streamlit run main.py```
  This will open a browser tab with your local AI-powered retrieval chatbot.

### 🛠 Troubleshooting:

* Ollama not found? Make sure it's installed and running: ollama list
* Models missing? Re-run ollama pull mistral && ollama pull nomic-embed-text
* Python issues? Check you're using Python 3.10+ and your virtual environment is active.

### 🔭 Learn more about Langchain RAG modules: 
https://python.langchain.com/docs/tutorials/rag/#components 

