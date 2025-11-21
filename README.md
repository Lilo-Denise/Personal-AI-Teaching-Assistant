# Personal AI Teaching Assistant 🎓

> A local, multimodal RAG-based teaching assistant that answers questions strictly from lecture slides with accurate citations.

![Project Screenshot](screenshots/main_ui.png)
*(Replace this path with your actual screenshot filename)*

## 📖 Project Overview
This tool allows students/researchers to upload lecture notes (PDFs) into a **secure local knowledge base**. It uses a Local LLM (Qwen2-1.5B) to generate answers grounded in the uploaded materials, ensuring zero hallucinations.

**Key Features:**
* **Obsidian UI:** A clean, high-contrast dark mode interface designed for focus.
* **Privacy First:** Runs entirely on Google Colab's GPU; data is stored in your private Google Drive.
* **Strict Citations:** Every answer includes inline citations (e.g., `[Page 5]`) and a visual source list.
* **Multimodal Processing:** Capable of processing PDF text and visual descriptions.
* **Knowledge Management:** Upload, view, and delete files from the vector database.

## 🛠️ Tech Stack
* **Frontend:** Gradio (Custom CSS for Dark Mode)
* **LLM:** Qwen2-1.5B-Instruct (via HuggingFace)
* **RAG Engine:** LangChain + ChromaDB
* **Embeddings:** Sentence-Transformers (`all-MiniLM-L6-v2`)
* **Storage:** Google Drive Integration

## 🚀 How to Run (Easy)

You don't need to install anything on your computer. Run it directly in the cloud:

1.  **Open the Notebook:**
    [![](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/YOUR_USERNAME/Personal-AI-Teaching-Assistant/blob/main/Personal_AI_TA.ipynb)
    *(Click the badge above)*

2.  **Setup Environment:**
    * In Colab, go to `Runtime` -> `Change runtime type` -> Select **T4 GPU**.
    * Click `Runtime` -> `Run all`.

3.  **Authorize:**
    * Allow Google Drive mounting when prompted (to save your knowledge base).

4.  **Launch:**
    * Scroll to the bottom cell and click the **Gradio Public Link** (e.g., `https://xxxx.gradio.live`).

## 📂 File Structure
* `Personal_AI_TA.ipynb`: The core source code.
* `data/`: Sample lecture slides for testing.
* `requirements.txt`: List of Python dependencies.

---
*Final Project | Fall 2025*
