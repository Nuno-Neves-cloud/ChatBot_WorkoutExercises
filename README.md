# Home Workouts Chatbot

Home Workouts Chatbot is a Retrieval-Augmented Generation (RAG) project that builds a personal fitness assistant from workout documents. It ingests PDF workout guides, stores their content in a vector database, and provides a conversational chatbot that answers home exercise questions using context retrieved from the ingested materials.

## What This Project Does

- Loads and preprocesses workout PDFs from the `files/` folder.
- Detects the topic of each document and enriches metadata accordingly.
- Splits text into retrievable chunks and stores them in Chroma.
- Uses OpenAI embeddings and chat models to build a RAG-powered workout assistant.
- Supports follow-up questions and conversational context.
- Includes a Gradio demo that provides an interactive trainer-style chat experience.

## Key Features

- **Home workout focus**: Built around exercise guides and training manuals.
- **Document ingestion pipeline**: Cleans, chunks, and indexes PDF content.
- **Retrieval-enhanced responses**: Uses relevant document passages to generate accurate answers.
- **Conversation memory**: Maintains recent chat history to support follow-up questions.
- **Trainer demo**: Provides an interactive interface for workout-related conversations.

## Setup & Configuration

1. Create and populate a `.env` file with the required secrets (see `.env.example`);
2. Run "setup_environment.sh";
3. Run "main.py";

## Files

- `files/100-workouts-vol1.pdf`
- `files/100-workouts-vol2.pdf`
- `files/100-workouts-vol3.pdf`
- `files/100-workouts-vol4.pdf`

Example workout documents used for ingestion.

## Notes

- The assistant is designed to answer questions using only the ingested workout documents.
- If the requested information is not available in the indexed documents, the assistant will indicate that it cannot answer the question based on the available content.
- This project is ideal for prototyping a fitness-focused chatbot using RAG techniques.
