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

The assistant can process complex queries, maintain conversational context, and provide precise responses based on the given document.

---

## Table of Contents
- [Features](#features)
- [How to Use](#how-to-use)
- [How It Works](#how-it-works)
- [Example Output](#example-output)
- [Future Enhancements](#future-enhancements)
- [How to Contribute](#how-to-contribute)

---

## Features

- **PDF Processing**: Extract and clean content from PDF documents using `PyPDFLoader`.
- **Conversational Context**: Retain query history for follow-up and context-aware responses.
- **Embeddings and Search**: Use FAISS and HuggingFace Sentence Transformers for semantic search.
- **Custom LLM Integration**: Utilize GroqLLM API for natural language generation.
- **Error Handling**: Implements retry logic for API rate limits and network errors.

---

## How to Use

1. Open the project notebook in **Google Colab**: [Run on Google Colab](https://colab.research.google.com/).
2. Upload your PDF file in the notebook when prompted.
3. Follow the notebook instructions to run each cell sequentially.
4. Ask questions about the uploaded PDF and get precise, context-aware answers.

No installation or setup is required besides having a Google account to access Colab.

---

## How It Works

1. **PDF Loading**: Loads and splits PDF into manageable chunks for semantic search.
2. **Embeddings**: Converts text into vector embeddings using HuggingFace models.
3. **Query Retrieval**: Retrieves the most relevant chunks using FAISS.
4. **Custom LLM**: Constructs query-specific prompts for GroqLLM to generate precise responses.
5. **Memory Management**: Maintains a buffer of conversational history for dynamic interactions.

---

## Example Output
```plaintext
Q: What is the notice period required when an employee resigns?
A: Employees are required to serve a 30-day notice period before resignation.

Q: Can the notice period be waived?
A: Yes, under certain circumstances, the notice period may be waived by mutual agreement.
```

---

## Future Enhancements

- **Multi-PDF Support**: Enable the assistant to work with multiple PDFs simultaneously.
- **Multilingual Support**: Add capabilities to handle documents in various languages.
- **Advanced Models**: Explore integration with LayoutLMv3 for processing complex document layouts.
- **OCR Integration**: Improve text extraction for scanned documents.
- **Customizable Output**: Allow users to configure response formats and styles.

---

## How to Contribute

We welcome contributions! Here’s how you can get involved:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-new-feature`).
3. Submit a pull request with a detailed description of changes.

For major changes, please open an issue first to discuss your ideas.

---


Feel free to explore, customize, and deploy this project! For any queries, reach out via Issues or Discussions.
