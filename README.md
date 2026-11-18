# Personal AI Teaching Assistant

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lilo-Denise/Personal-AI-Teaching-Assistant/blob/main/Personal_AI_Teaching_Assistant_revised.ipynb)

A study assistant that answers questions from your own lecture PDFs and shows which page each answer came from. Built as a Yale SOM course project in Fall 2025.

## Why I built it

When revising, I wanted answers grounded in the course material itself, with a page reference I could check, instead of a general chatbot answer.

## What it does

- Upload lecture PDFs; they are stored in your own Google Drive.
- Reads both the text and the slide images (an image-captioning model describes visuals).
- Splits the material into chunks and stores them in a local vector database.
- Answers a question using only the retrieved chunks, with the source file and page number.
- Lets you view and delete uploaded files; the database refreshes automatically.

## How it works

PDF → text + image captions → chunks (LangChain) → embeddings (FastEmbed) → ChromaDB → retrieve top chunks → Qwen2-1.5B-Instruct answers with citations → Gradio web interface

## Run it

1. Open `Personal_AI_Teaching_Assistant_revised.ipynb` in Google Colab (button above).
2. Set Runtime → Change runtime type → T4 GPU, then Run all.
3. Allow Google Drive access when asked.
4. Open the Gradio link printed in the last cell.

## Files

- `Personal_AI_Teaching_Assistant_revised.ipynb`: current version
- `Personal_AI_Teaching_Assistant.ipynb`: first version
- `requirements.txt`: Python dependencies

## Limits

It runs a small model on a free Colab GPU, so answers are short and depend on how well the slides are retrieved. It is a course prototype, not a production tool.
