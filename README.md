# RAG-using-LangChain
The RAG-based Document Q&amp;A Interface is a Jupyter Notebook tool that allows users to upload PDF, Word, and Excel files, extract and index their content, and ask questions. Powered by Google's Generative AI and LangChain, it delivers accurate, context-aware answers and maintains interaction history for a seamless experience.
# 📚 RAG-based Document Q&A Interface

The RAG-based Document Q&A Interface is a Jupyter Notebook tool that allows users to upload PDF, Word, and Excel files, extract and index their content, and ask questions. Powered by Google's Generative AI and LangChain, it delivers accurate, context-aware answers and maintains interaction history for a seamless experience.
![Screenshot 2024-12-21 013916](https://github.com/user-attachments/assets/23ed8d14-3cb7-421c-8d73-be7c758dd2e3)
![Screenshot 2024-12-21 013948](https://github.com/user-attachments/assets/9bcecb51-317a-41c3-83de-2718697394b5)

---

## 📖 Table of Contents

1. [Features](#features)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Configuration](#configuration)
5. [Usage](#usage)
6. [Troubleshooting](#troubleshooting)
7. [Project Structure](#project-structure)
8. [Contributing](#contributing)
9. [License](#license)
10. [Acknowledgements](#acknowledgements)
11. [Contact](#contact)

---

## 🎯 Features

- **Document Upload:** Supports uploading multiple PDF, Word (`.doc`, `.docx`), and Excel (`.xls`, `.xlsx`) files.
- **Text Extraction:** Extracts text content from uploaded documents for processing.
- **Intelligent Retrieval:** Utilizes LangChain and Chroma for embedding and indexing document content.
- **Interactive Q&A:** Provides a user-friendly interface to ask questions and receive answers based on the uploaded documents.
- **Source Documentation:** Option to display source document snippets alongside answers for context.
- **Interaction History:** Maintains a history of all questions and answers for easy reference.
- **Customizable Interface:** Styled using `ipywidgets` and custom CSS for a professional look and feel.

---

## 🚀 Prerequisites

Before you begin, ensure you have met the following requirements:

- **Python 3.7 or higher**
- **Jupyter Notebook:** Install via Anaconda or `pip`.
- **Google API Key:** Access to Google's Generative AI API (PaLM).
- **Internet Connection:** Required for API calls and library installations.

---

## 🛠 Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/rag-document-qa.git
   cd rag-document-qa
2. **Create a Virtual Environment (Optional but Recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate

