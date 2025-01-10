# PDF-Based Conversational AI Assistant

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-Integration-brightgreen?logo=langchain)
![FAISS](https://img.shields.io/badge/FAISS-Vector_Store-orange)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Embeddings-yellow?logo=huggingface)
![License](https://img.shields.io/badge/License-MIT-green)
![Contributions](https://img.shields.io/badge/Contributions-Welcome-brightgreen?logo=github)

---

## Overview

This project implements a **Conversational AI Assistant** designed to help employees understand company policies by referencing a company-provided PDF document. It uses **LangChain**, **FAISS**, and **HuggingFace embeddings** for PDF content retrieval and a custom GroqLLM for dynamic query answering. 

The assistant can process complex queries, maintain conversational context, and provide precise responses based on the document.

---

## Table of Contents
- [Features](#features)
- [Setup](#setup)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Example Output](#example-output)
- [Contribution Guidelines](#contribution-guidelines)
- [Enhancements You Can Contribute To](#enhancements-you-can-contribute-to)
- [License](#license)

---

## Features

- **PDF Processing**: Extract and clean content from PDF documents using `PyPDFLoader`.
- **Conversational Context**: Retain query history for follow-up and context-aware responses.
- **Embeddings and Search**: Use FAISS and HuggingFace Sentence Transformers for semantic search.
- **Custom LLM Integration**: Utilize GroqLLM API for natural language generation.
- **Error Handling**: Implements retry logic for API rate limits and network errors.

---

## Setup

1. Open the `lcpdf.ipynb` notebook in [Google Colab](https://colab.research.google.com/).
2. Run the cells sequentially to set up the environment and execute the assistant.

No additional setup or installations are needed beyond running the notebook.

---

## How It Works

1. **PDF Loading**: Loads and splits PDF into manageable chunks for semantic search.
2. **Embeddings**: Converts text into vector embeddings using HuggingFace models.
3. **Query Retrieval**: Retrieves the most relevant chunks using FAISS.
4. **Custom LLM**: Constructs query-specific prompts for GroqLLM to generate precise responses.
5. **Memory Management**: Maintains a buffer of conversational history for dynamic interactions.

---

## Usage

### Step 1: Load a PDF
Replace the `pdf_path` with your own PDF file:
```python
pdf_path = "your_document.pdf"
loader = PyPDFLoader(pdf_path)
pages = loader.load()
```

### Step 2: Run a Query
Ask a question by calling:
```python
ask_question("What is the notice period required when an employee resigns?")
```

### Step 3: Customize Queries
Add more queries to the `test_queries` list for batch testing:
```python
test_queries = [
    "What is the policy for remote employees?",
    "Can I take vacation leave during my notice period?",
]
```

---

## Example Output
```plaintext
Q: What is the notice period required when an employee resigns?
A: Employees are required to serve a 30-day notice period before resignation.

Q: Can the notice period be waived?
A: Yes, under certain circumstances, the notice period may be waived by mutual agreement.
```

---

## Contribution Guidelines

We welcome contributions! Here’s how you can help:

1. Fork this repository.
2. Create a new branch (`git checkout -b feature-new-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-new-feature`).
5. Open a pull request.

---

## Enhancements You Can Contribute To

- [ ] Add multi-PDF support.
- [ ] Integrate additional LLM providers.
- [ ] Expand error-handling mechanisms.
- [ ] Include support for multilingual documents.

---


Feel free to clone, customize, and deploy this project! For any queries, reach out via Issues or Discussions.
