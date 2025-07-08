


# 🚀 Langchain Notebook Setup



This project demonstrates how to use Langchain and OpenAI in Jupyter notebooks for two main workflows:

- **lang.ipynb**: Automatically break down a complex question into multiple sub-questions using a Pydantic model and a system prompt.
- **RAG-lang.ipynb**: Retrieval-Augmented Generation (RAG) workflow, where the LLM answers a question using relevant context retrieved from a set of documents.

### lang.ipynb: Sub-question Decomposition
It leverages a **Pydantic model** to enforce structured output (a list of sub-questions), and uses a **system prompt** together with an actual question (e.g., "What are the main components of an LLM-powered autonomous agent system?") to instruct the LLM to decompose the query into actionable sub-tasks.

**What does the code do?**

The notebook (`lang.ipynb`) loads your OpenAI API key from a `.env` file and uses the Langchain library to:

- 🧩 **Define a Pydantic model** for structured output, ensuring the response is always a list of sub-questions.
- 📝 **Set up a system prompt** that instructs the AI to break down any main question into sub-questions.
- ❓ **Send an actual question** (e.g., "What are the main components of an LLM-powered autonomous agent system?") to the OpenAI model, together with the system prompt.
- 📋 **Receive and print a list of sub-questions**, each representing a smaller part of the original query.

You can modify the Pydantic model or the system prompt, and use this pattern to decompose any complex query into actionable sub-tasks using LLMs.

### RAG-lang.ipynb: Retrieval-Augmented Generation
This notebook demonstrates how to use a simple in-memory FAISS vectorstore and OpenAI to answer questions using retrieved context:

- 📄 **Store example documents** in a vector database (FAISS) with OpenAI embeddings.
- 🔍 **Retrieve relevant context** for a user question.
- 🧠 **Format a system prompt** with the retrieved context and the user's question.
- 🤖 **Use the OpenAI model** to generate a concise answer based on the context.

You can adapt this workflow to use your own documents for more advanced RAG applications.

## 1️⃣ Create and Activate Virtual Environment

🛠️ Open your terminal and run:
```cmd
python -m venv venv
venv\Scripts\activate
```

## 2️⃣ Install Required Packages

📦 Install dependencies with:
```cmd
pip install -r requirements.txt
```

💡 Or, to install manually:
```cmd
pip install langchain-openai langchain-core python-dotenv
```

## 3️⃣ Set Up OpenAI API Key

🔑 Create a file named `.env` in the project folder with this content:
```
OPENAI_API_KEY=sk-<your-openai-key-here>
```

## 4️⃣ Start Jupyter Notebook

📓 Launch Jupyter with:
```cmd
jupyter notebook
```

➡️ Open `lang.ipynb` and run the cells to get started!
