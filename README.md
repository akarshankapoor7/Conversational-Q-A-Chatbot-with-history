
This Conversational Q&A Chatbot is a Generative AI project built using LangChain (with llama3-8b-8192 model) to enable intelligent, context-aware interactions. The chatbot retains memory of past exchanges, ensuring a seamless and coherent conversation flow.



To incorporate chat history effectively, the project implements two approaches:

1. Chains: A structured method that always retrieves relevant context before generating a response.

2. Agents: A more flexible approach where the LLM dynamically decides when and how to retrieve past information, allowing for multiple retrieval steps if needed.



By leveraging LangChain's retrieval-augmented generation (RAG) capabilities, the chatbot delivers more accurate and contextually relevant answers. This project showcases the power of Generative AI in building interactive, intelligent assistants.

---------------------------------------------------------------------------------------------

Pre-requisites

Before running this Conversational Q&A Chatbot, ensure you have the following:

1. Environment Setup
   
Python 3.8+

Virtual environment (recommended) → venv or conda


2. Required Libraries
   
Install dependencies using:


pip install langchain langchain_community chromadb faiss-cpu openai tiktoken python-dotenv

Additional libraries based on your use case:

For vector storage: chromadb (or faiss-cpu as an alternative)

For embeddings: huggingface


For LLM integration: openai, ollama, groq, or huggingface_hub


3. Generate and Store API Keys
4. 
To use Grok AI and Hugging Face, generate API keys from:


Grok AI API Key → Obtain from Grok AI Developer Portal


Hugging Face API Key → Obtain from Hugging Face


Store them securely in a .env file in your project directory:


ini
Copy
Edit

GROQ_API_KEY=your_groq_api_key_here

HUGGINGFACE_API_KEY=your_huggingface_api_key_here
Load them in your Python script using:


python
Copy
Edit
from dotenv import load_dotenv
import os

load_dotenv()


GROQ_API_KEY = os.getenv("GROQ_API_KEY")

HUGGINGFACE_API_KEY = os.getenv("HUGGINGFACE_API_KEY")

4. Knowledge Base & Data
   
A document dataset for retrieval (e.g., PDFs, text files)


Preprocessed embeddings for efficient search


With these pre-requisites set up, you can run the chatbot and enable context-aware Q&A! 🚀
