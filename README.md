# Retrieval Augmented Generation (RAG) Implementation with Qdrant and Llamafile

This repository contains an end-to-end implementation of the **Retrieval Augmented Generation (RAG)** pattern. The project was developed as part of the "Introduction to Retrieval Augmented Generation (RAG)" course by **Duke University** on Coursera, under the guidance of instructor **Alfredo Deza**.

The implementation uses **Qdrant** as the vector database and **Llamafile** as the Large Language Model (LLM) engine to create a robust system capable of retrieving relevant data and generating meaningful responses based on user queries.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Learning Objectives](#learning-objectives)
- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [Steps to Run the Project](#steps-to-run-the-project)
- [Notebooks in This Repository](#notebooks-in-this-repository)
- [Technologies Used](#technologies-used)
- [Acknowledgements](#acknowledgements)

---

## Project Overview
This project demonstrates how to:
- Create a **Retrieval Augmented Generation (RAG)** system using your own dataset.
- Use embeddings generated by **Sentence Transformers** for vectorization of data.
- Query a **Qdrant** vector database to retrieve relevant context.
- Integrate the context with a Large Language Model (LLM) like **Llamafile** or OpenAI's API to generate meaningful responses.

---

## Learning Objectives
By completing this project, you will:
1. Understand the core components of a RAG system.
2. Learn to create embeddings for your dataset using **Sentence Transformers**.
3. Implement a vector search using **Qdrant**.
4. Connect to a local or cloud-based LLM (e.g., Llamafile or OpenAI API).
5. Build a fully functional RAG application capable of intelligent query handling.

---

## Features
- **Vectorization**: Embedding of dataset fields such as `description`, `requirements`, and `title`.
- **Vector Search**: Fast and efficient search using Qdrant for retrieving the most relevant data points.
- **LLM Integration**: Use of a local LLM (via Llamafile) or OpenAI API for generating responses based on retrieved context.
- **Custom Dataset Support**: Replace the sample dataset with your own formatted as a list of dictionaries.

---

## Setup Instructions
### Prerequisites
- Python 3.8 or higher
- Basic knowledge of Python and terminal operations
- Virtual environment tools like `venv` or `conda`

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Start the Qdrant instance:
   - For an in-memory instance (no persistence), Qdrant will automatically start when the code runs.
   - Alternatively, use Docker:
     ```bash
     docker run -p 6333:6333 -d qdrant/qdrant
     ```

5. Download and set up the **Phi-2 model** from Llamafile (or configure an OpenAI API endpoint).

---

## Steps to Run the Project
1. **Prepare the Dataset**:
   Replace the sample data with your own, formatted as a list of dictionaries.

2. **Run Notebooks**:
   - **`data_embedding.ipynb`**: This notebook creates embeddings for your dataset using Sentence Transformers and uploads them to the Qdrant vector database.
   - **`rag_implementation.ipynb`**: This notebook integrates Qdrant and Llamafile (or OpenAI) to build and query a Retrieval Augmented Generation system.

3. **Verify Results**:
   - Test the RAG implementation with various queries and observe the LLM's responses.
   - Analyze the relevance of retrieved data and generated text.

---

## Notebooks in This Repository
1. **`data_embedding.ipynb`**:
   - Prepares the dataset for vectorization.
   - Generates embeddings using Sentence Transformers.
   - Uploads embeddings to Qdrant.

2. **`rag_implementation.ipynb`**:
   - Implements the RAG system.
   - Integrates Qdrant for vector retrieval.
   - Connects to Llamafile or OpenAI for context-aware text generation.

---

## Technologies Used
- **Qdrant**: In-memory vector database for fast and scalable similarity search.
- **Sentence Transformers**: For creating embeddings from text data.
- **Llamafile**: A lightweight tool to run local LLMs.
- **OpenAI API**: Alternative option for cloud-based LLM queries.
- **Python**: Programming language used to implement the project.

---

###  Acknowledgements
- **Instructor**: Alfredo Deza, for providing detailed guidance and the Applied RAG Notebook as a starting point.
- **Duke University**: For offering the "Introduction to Retrieval Augmented Generation (RAG)" course.
- **Qdrant and Sentence Transformers**: For enabling robust vector search and embedding capabilities.

---

This repository provides a foundational implementation of RAG systems. Feel free to extend it by adding advanced features such as fine-tuned LLMs, hybrid search, or deployment as a web application. Happy coding!
