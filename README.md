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
3. **Install Dependencies**

    Ensure you have `pip` updated:

    ```bash
    pip install --upgrade pip
    ```

    Then install the required packages using the provided `requirements.txt`:

    ```bash
    pip install -r requirements.txt
    ```

    **Note:** If you prefer, you can install dependencies directly within the Jupyter Notebook by uncommenting the installation line in the code:

    ```python
    # !pip install google-generativeai langchain chromadb tiktoken pypdf docx2txt openpyxl langchain-google-genai ipywidgets
    ```

---

## 📁 Configuration

### 1. Obtain a Google API Key

- Sign up for access to Google's Generative AI (PaLM) API.
- Ensure your API key has permissions to access the required models (`gemini-pro` and `models/embedding-001`).

### 2. Set Up API Key Securely

**Option 1: Environment Variables (Recommended)**

1. **Install `python-dotenv`:**

    ```bash
    pip install python-dotenv
    ```

2. **Create a `.env` File:**

    In the project root directory, create a file named `.env` and add your API key:

    ```makefile
    GOOGLE_API_KEY=your_actual_google_api_key_here
    ```

3. **Modify the Notebook Code to Load Environment Variables:**

    ```python
    from dotenv import load_dotenv
    import os

    load_dotenv()

    GOOGLE_API_KEY = os.getenv("GOOGLE_API_KEY")
    ```

**Option 2: Direct Replacement (Not Recommended for Shared Environments)**

1. Open the Jupyter Notebook.
2. Locate the configuration section and replace the placeholder with your actual API key:

    ```python
    GOOGLE_API_KEY = "YOUR_GOOGLE_API_KEY"  # Replace with your actual API key
    ```

⚠️ **Security Warning:** Avoid hardcoding sensitive API keys directly into notebooks, especially if the notebooks are to be shared or stored in version control systems.

---

## 📝 Usage

1. **Launch Jupyter Notebook**

    ```bash
    jupyter notebook
    ```

2. **Open the Notebook**

    Navigate to the cloned repository folder and open the `RAG_Document_QA.ipynb` notebook.

3. **Run All Cells**

    Execute each cell in order by selecting `Cell > Run All` or running them individually. Ensure that the configuration cell is executed after setting up the API key.

4. **Interact with the Interface**

    - **Upload Documents**
        - Click on the "📄 Upload Files" button.
        - Select one or more PDF, Word (`.doc`, `.docx`), or Excel (`.xls`, `.xlsx`) files from your local machine.

    - **Process Documents**
        - After uploading, click the "✅ Process Documents" button.
        - The notebook will display processing status and information about each uploaded document.

    - **Ask Questions**
        - Once processing is complete, a question input box labeled "❓ Your Question:" will be available.
        - Type your question related to the content of the uploaded documents and click the "💬 Get Answer" button.
        - The answer will be displayed below in a clean, formatted manner.
        - If you check the "📜 Show Source Documents" option, snippets from the relevant documents will also be displayed.

    - **Review History**
        - All your questions and corresponding answers will be logged in the "🗒️ History" section for easy reference.

---

## 🐛 Troubleshooting

If you encounter issues with the retrieval and Q&A functionality, consider the following steps:

1. **Verify API Access and Model Availability**
    - Ensure your Google API key has access to the PaLM API and the specified models (`gemini-pro` and `models/embedding-001`).
    - If you don't have access to `gemini-pro`, switch to a model you have access to, such as `text-bison`.

2. **Check for Errors in the Output**
    - Look for error messages in the output cells after processing documents or asking questions.
    - Common issues include empty text extraction, embedding failures, or model access errors.

3. **Test with Simple Documents**
    - Upload a simple PDF or DOCX file with known text content to verify that text extraction works correctly.
    - Ensure documents are not encrypted or scanned images without OCR.

4. **Update Libraries**
    - Ensure all libraries are up-to-date to maintain compatibility.

    ```bash
    pip install --upgrade langchain google-generativeai
    ```

5. **Inspect the Retriever**
    - After building the retriever, perform a test query to ensure it's retrieving documents.

    ```python
    test_docs = retriever.get_relevant_documents("test")
    print(f"Number of documents retrieved: {len(test_docs)}")
    ```

    - If no documents are retrieved, there may be an issue with the embeddings or text extraction.

6. **Review API Key and Permissions**
    - Double-check that the API key is correct and active.
    - Ensure no typos or extra spaces are present when setting the API key.

7. **Consult Documentation and Support**
    - Refer to the [LangChain Documentation](https://langchain.com/docs/) for detailed guidance.
    - Reach out to Google Cloud Support if you suspect issues with API access.

---

## 📂 Project Structure

```bash
rag-document-qa/
│
├── RAG_Document_QA.ipynb      # Main Jupyter Notebook
├── requirements.txt           # Python dependencies
├── README.md                  # Project documentation
└── .env                       # Environment variables (optional)
