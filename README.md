
This Conversational Q&A Chatbot is a Generative AI project built using LangChain (with llama3-8b-8192 model) to enable intelligent, context-aware interactions. The chatbot retains memory of past exchanges, ensuring a seamless and coherent conversation flow.



To incorporate chat history effectively, the project implements two approaches:

1. Chains: A structured method that always retrieves relevant context before generating a response.

2. Agents: A more flexible approach where the LLM dynamically decides when and how to retrieve past information, allowing for multiple retrieval steps if needed.



By leveraging LangChain's retrieval-augmented generation (RAG) capabilities, the chatbot delivers more accurate and contextually relevant answers. This project showcases the power of Generative AI in building interactive, intelligent assistants.

---------------------------------------------------------------------------------------------

Pre-requisites
Before running this Conversational Q&A Chatbot, ensure you have the following dependencies and configurations set up.

1️⃣ Environment Setup
Ensure you have:

Python 3.8+ installed

A virtual environment (recommended):

bash
Copy
Edit
# Create a virtual environment
python -m venv venv  

# Activate the virtual environment  
# Windows  
venv\Scripts\activate  

# macOS/Linux  
source venv/bin/activate  
2️⃣ Required Libraries
Install the necessary dependencies:

bash
Copy
Edit

pip install langchain langchain_community chromadb faiss-cpu openai tiktoken python-dotenv

Additional Libraries (as per your use case):

Vector storage → chromadb (or faiss-cpu as an alternative)

Embeddings → huggingface

LLM Integration → openai, ollama, groq, huggingface_hub

3️⃣ Generate and Store API Keys
To use Grok AI and Hugging Face, obtain API keys from:

🔑 Grok AI API Key → Grok AI Developer Portal

🔑 Hugging Face API Key → Hugging Face Tokens

Store API Keys Securely

Create a .env file in your project directory and add:

ini
Copy
Edit

GROQ_API_KEY=your_groq_api_key_here

HUGGINGFACE_API_KEY=your_huggingface_api_key_here

Load API Keys in Code
python
Copy
Edit

from dotenv import load_dotenv
import os

load_dotenv()

GROQ_API_KEY = os.getenv("GROQ_API_KEY")

HUGGINGFACE_API_KEY = os.getenv("HUGGINGFACE_API_KEY")


4️⃣ Knowledge Base & Data
📂 Dataset for retrieval → PDFs, text files, or structured documents

🧠 Preprocessed embeddings for efficient search and retrieval

✅ Once these pre-requisites are met, you're ready to run the Conversational Q&A Chatbot powered by Generative AI! 🚀








