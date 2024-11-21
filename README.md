# NAVATAR-Helper

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Streamlit](https://img.shields.io/badge/Framework-Streamlit-red)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/Library-LangChain-yellow)](https://python.langchain.com/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)


NAVATAR-Helper is an AI-driven chatbot developed to assist with health-related NEET (Not in Education, Employment, or Training) queries. It leverages the **Retrieval-Augmented Generation (RAG)** framework to provide accurate, bilingual answers in **Norwegian** and **English** based on verified sources, while minimizing hallucinations.

## Overview

- **Project Goal**: Develop a fully working MVP of a RAG-based chatbot that delivers accurate, sourced & verified answers to NEET-related queries while minimizing hallucinations. 
- **Technology Stack**:
  - **Backend**: Python, LangChain, custom LLMs.
  - **Frontend**: Streamlit for user interface.
  - **Embedding Model**: `Alibaba-NLP/gte-multilingual-base` for question vectorization.
  - **Vector Database**: Milvus for storing and retrieving vectorized data.
  - **LLM**: `norallm/normistral-7b-warm-instruct` for generating responses.
  - **GPU Server**: Nvidia GeForce GTX 1080 Ti (11GB VRAM).

## Key Features
- **RAG Framework**: Integrates retrieval and generation for precise answers.
- **Bilingual Support**: Handles both Norwegian and English queries.
- **Source Attribution**: Provides references for each response.
- **Reduced Hallucinations**: Strict use of retrieved, relevant data ensures factual outputs.
- **Extensive Testing**: Both RAG and non-RAG approaches for performance comparison

## Architecture

1. **User Input**: Processes user questions via a Streamlit-based frontend.
2. **Language Detection**: Determines the input language (Norwegian or English).
3. **Embedding**: Converts questions into vectors using `Alibaba-NLP/gte-multilingual-base`.
4. **Context Retrieval**: Utilizes Milvus to find relevant document chunks.
5. **Response Generation**: Uses `norallm/normistral-7b-warm-instruct` to produce context-informed answers.
6. **Attribution**: Displays sources for user verification.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/sirin-koca/NAVATAR-Helper.git
   cd NAVATAR-Helper

2. Install dependencies:
   ```bash
   pip install -r requirements.txt

3. Run NAVATAR-Helper:
   ```bash
   streamlit run app.py

### Backend scripts:
* popDB.py: Prepares the vector database with embeddings.
* setupLLM.py: Initializes the LLM for use.
* ragMain.py: Main interaction handler for user queries.

### Prerequisites
- Python 3.8 or higher
- PyCharm or any Python IDE
- A virtual environment for dependency management
- Access to a GPU server (e.g., Nvidia GeForce GTX 1080 Ti or higher)
- Git for version control

### Team Members: Sirin, Rafey, Younes, Morten, Valerie

---

DATA3750 Applied AI & Data Science | Group Project | OsloMet H2024 ©

---





