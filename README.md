 # Retrieval Augmented Generation (RAG) with LangChain

This project demonstrates how to build a Retrieval Augmented Generation (RAG) system using LangChain and IBM Granite models. It is part of the AICTE - IBM Internship on AI & Cloud Technologies by Edunet Foundation.

## What is RAG?

Retrieval Augmented Generation is a technique that enhances the capabilities of Large Language Models (LLMs) by integrating factual information from external knowledge bases. Instead of relying solely on the model's internal knowledge, RAG retrieves relevant information and combines it with the model's generation process, resulting in more accurate and context-aware answers.

**Typical RAG Use Cases:**
- Customer support: Answering product or service questions using documentation.
- Domain expertise: Providing facts from specialized articles or papers.
- News chat: Discussing current events using recent articles.

## Project Overview

This notebook walks through the process of setting up and running a RAG pipeline using LangChain and IBM Granite models. It covers:

1. **Environment Setup:**  
   Ensuring compatibility with Python 3.10–3.12 and installing necessary libraries.

2. **Selecting System Components:**  
   - Embeddings Model: Uses IBM Granite Embedding model via HuggingFace.
   - Vector Database: Stores embeddings using Milvus.
   - LLM: Answers questions using an IBM Granite 8B model via Replicate.

3. **Building the Vector Database:**  
   - Downloads a sample document (President Biden's State of the Union address).
   - Splits the document into manageable chunks.
   - Generates embeddings for each chunk and stores them in the vector database.

4. **Querying and Generating Answers:**  
   - Retrieves relevant document chunks based on user queries.
   - Uses a RAG pipeline to generate context-aware responses.

## How to Use

1. **Clone the repository and set up a Python (3.10–3.12) virtual environment.**
2. **Install dependencies:**  
   See the notebook for `pip install` instructions.

3. **Configure your API keys:**  
   For Replicate, set the `REPLICATE_API_TOKEN` as an environment variable.

4. **Run the notebook or script:**  
   - The notebook will download the sample document, process it, and store embeddings.
   - You can query the system with questions; relevant context is retrieved and used to answer.

## Example Workflow

- The system indexes knowledge-base passages (text chunks) for retrieval.
- For each user query:
  - Retrieves relevant passages using vector similarity.
  - Feeds those passages, along with the query, to the LLM for answer generation.

## Technologies Used

- **LangChain:** Orchestrates the RAG pipeline.
- **IBM Granite Models:** For embeddings and LLM responses.
- **Milvus:** Vector database for storing and retrieving embeddings.
- **Replicate:** For LLM API access.
- **Transformers/HuggingFace:** For model loading and tokenization.

## References

- [LangChain Documentation](https://python.langchain.com/)
- [IBM Granite Community](https://github.com/ibm-granite-community)
- [Milvus Vector Database](https://milvus.io/)
- [Replicate API](https://replicate.com/ibm-granite)

---

**Note:** This repository is primarily implemented in Jupyter Notebook and Python.
