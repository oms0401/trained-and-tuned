# Trained and tuned Project repository 🚀

This README provides step-by-step instructions to run two Python scripts, `llm.py` and `rag.py`, which leverage the Groq API for building intelligent chatbots.

## Prerequisites 🛠️

Before you begin, ensure you have the following installed:

* **Python 3.8 or higher:** You can download it from [python.org](https://www.python.org/downloads/).
* **pip:** Python package installer, usually included with Python installations.

Additionally, this project uses a `requirements.txt` file to manage dependencies. It's highly recommended to create a virtual environment to isolate the project dependencies.

### 1. Create a Virtual Environment (Recommended) 📦

1.  Open your terminal or command prompt.
2.  Navigate to the directory where you have saved the project files.
3.  Create a virtual environment using `venv` (or `conda` if you prefer):

    ```bash
    # Using venv
    python -m venv venv
    source venv/bin/activate  # On macOS and Linux
    venv\Scripts\activate  # On Windows

    # Using conda (if you have Anaconda installed)
    conda create -n groq_chat python=3.9  # Or your preferred Python version
    conda activate groq_chat
    ```

### 2. Install Dependencies ⚙️

1.  Make sure your virtual environment is activated.
2.  Navigate to the directory containing the `requirements.txt` file.
3.  Install all the necessary libraries using pip:

    ```bash
    pip install -r requirements.txt
    ```

    This command will install the following packages (and their dependencies):

    * `streamlit`
    * `langchain`
    * `langchain-groq`
    * `python-dotenv`
    * `transformers`
    * `pypdf`
    * `torch`
    * `nest-asyncio`

### 3. Obtain a Groq API Key 🔑

1.  Go to the [Groq Cloud website](https://console.groq.com/) and sign up for an account.
2.  Once logged in, navigate to the API Keys section (usually under your profile or settings).
3.  Create a new API key. **Keep this key secure and do not share it.**

### 4. Create an Environment File (`.env`) 📂

1.  In the same directory where you have saved the `llm.py` and `rag.py` scripts, create a new file named `.env`.
2.  Open the `.env` file and add your Groq API key as follows:

    ```
    GROQ_API_KEY="YOUR_GROQ_API_KEY"
    ```

    Replace `"YOUR_GROQ_API_KEY"` with the actual API key you obtained from the Groq Cloud website.

### 5. Prepare the PDF Document (for `rag.py`) 📄

1.  For the `rag.py` script, you need a PDF document to perform Retrieval-Augmented Generation (RAG).
2.  Save the PDF document named `OpenAI AI Agents.pdf` in the same directory as your Python scripts.

## Running the Scripts with Streamlit 🏃

You can run each script individually using Streamlit commands in your terminal. **Ensure your virtual environment is still activated.**

### Running `llm.py` (Simple Chatbot) 💬

1.  Open your terminal or command prompt.
2.  Navigate to the directory where you saved `llm.py`.
3.  Run the following command:

    ```bash
    streamlit run llm.py
    ```

4.  Streamlit will automatically open a new tab in your web browser displaying the "Ask Chatbot!" application.
5.  You can now type your prompts in the chat input and interact with the Groq-powered language model.

### Running `rag.py` (RAG-Based Chatbot) 📚

1.  Open your terminal or command prompt (you can use the same one or open a new one).
2.  Navigate to the directory where you saved `rag.py` and the `OpenAI AI Agents.pdf` file.
3.  Run the following command:

    ```bash
    streamlit run rag.py
    ```

4.  Streamlit will automatically open a new tab in your web browser displaying the "Ask RAG-Chatbot!" application.
5.  You can now type your prompts related to the content of the `OpenAI AI Agents.pdf` document. The chatbot will retrieve relevant information from the PDF and use it to generate its responses.

## Interacting with the Chatbots 🗣️

Once the Streamlit applications are running in your browser:

* **Type your question or prompt** in the text input field at the bottom of the page.
* **Press Enter** or click the send button.
* The chatbot's response will appear in the chat window along with your message history.

Enjoy interacting with your Groq-powered chatbots!

## AI Engineering Roadmap 🗺️

Here's a roadmap to guide you on your journey to becoming an AI Engineer:

**Resources for the AI engineering guide**

**Stage 1) - Python Fundamentals 🐍**

* **Python Basics**
    * Playlist link - [Python Tutorial](https://youtube.com/playlist?list=PLkQC5wF3Zy4Ug2MCKV_jeyX8_Fyb4O2Ot&feature=shared)
    * Objective - To learn what Python does and also try to know why the following works it will build the intuition regarding the language and problem-solving in general. Mastering the concepts of OOPS, functions, and decorators are a must.
* **Advance Python - Type Hinting**
    * link - [PEP 484 -- Type Hints](https://peps.python.org/pep-0484/)
    * Objective - To learn Python modern practices and getting the intuition for the production-ready code that will be used in various stages of the SWE development.
* **Glossary**
    * Learn the dataclass and callable as well. A simple ChatGPT prompt would be enough to get you prepared in this topic.
* **Asynchronous Programming Fundamentals**
    * [Async support in FastAPI](https://fastapi.tiangolo.com/async/)
    * Objective - Learn the pillars of the async and await functions which are the backbone for request handling.

**Stage 2) - Learning Machine Learning Essentials for the AI Engineering 🤖**

* **Machine Learning Basics**
    * Link - [Machine Learning Tutorial](https://youtube.com/playlist?list=PLxlkzujLkmQ87mDkOp2aw5Z-PB1gBqnI-&feature=shared )
    * Lectures to be skipped from the playlist - from 24 to 33
* **Introduction to NLP**
    * Link - [Introduction to NLP](https://youtu.be/ENLEjGozrio?feature=shared)
* **Transformer Architecture**
    * Link - [Transformer Architecture Explained](https://youtu.be/3bPhDUSAUYI?feature=shared)
* All the above are just theoretical videos for practical implementation just do a simple search on the particular topic that you have finished and learn from it.

**Stage 3 ) AI engineering phase 🧠**

* **Chat Completion API Documentation**
    * Link - [OpenAI Chat Completion API](https://platform.openai.com/docs/guides/text?api-mode=responses)
    * Objective - Read it end to end as it is the heart of all the AI engineering advancements read it multiple times if needed but strong control over this is needed.
    * Project - Make the sarcastic CLI chatbot that gives witty replies (Use prompt engineering to make this)
* **Understanding Agents**
    * Link - [Building Agents from Scratch](https://youtu.be/1OLrT3dEzhA?feature=shared )
    * Objective - Know the underhood working of the agents using the chatcompletion API.
* **Understanding RAG**
    * Link - [Retrieval Augmented Generation (RAG) Explained](https://youtu.be/8sSHg1034r0?feature=shared)
    * Objective - To know what is RAG and how it works.
* **Langchain Framework**
    * Link - [Introduction to Langchain](https://youtube.com/playlist?list=PLKnIA16_RmvaTbihpo4MtzVm4XOQa0ER0&feature=shared)
    * Objective - Learn about the Langchain and get to know how to make LLM-powered applications.
    * Project - Make a production-ready RAG chatbot (resources you have to figure out)
* **LangGraph for Agents**
    * Link - [Introduction to LangGraph](https://youtube.com/playlist?list=PL0vKVrkG4hWoHDg46N85-9NDhmOaPWEwA&feature=shared)
    * Objective - Learn about the agents and its working.
    * Project - Make a deep research agent from the web with weblinks (resources to be figured out on own)

Once you have covered till here now make as much project that are production ready as possible and learning of backend for the ai engineering is also essential but due to your firm grasp on Python and knowing the SWE principles will make it easy for you.