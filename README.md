Conversational AI with ChatGroq

Uses GROQ’s Llama 3-8B-8192 model as the LLM for generating responses.
Takes user questions and provides accurate answers based on retrieved document context.
PDF Document Processing & Vector Embeddings

Loads PDF files from the ./us_census directory using LangChain’s PyPDFDirectoryLoader.
Splits documents into chunks using RecursiveCharacterTextSplitter (Chunk Size: 1000, Overlap: 200).
Creates embeddings using OpenAI’s Embedding Model.
Stores embeddings in a FAISS vector database for efficient retrieval.
Retrieval-Augmented Generation (RAG) Pipeline

Retrieves relevant document chunks from FAISS using similarity search.
Uses LangChain’s Retrieval Chain to fetch contextual information from the documents.
Generates answers based on retrieved context using the LLM model (ChatGroq).
Streamlit UI for User Interaction

Users can embed PDF documents into the vector database with a single button click.
Provides a text input field where users enter questions related to the uploaded documents.
Displays AI-generated responses and similar document excerpts for transparency.
Uses Streamlit expander to show document similarity results alongside answers.
Technologies Used:
Streamlit – For building the interactive web app.
LangChain – For document processing, embeddings, and retrieval chain.
GROQ Chat (Llama 3-8B-8192) – As the LLM for answering questions.
FAISS – For vector-based document retrieval.
OpenAI Embeddings – To generate numerical representations of text.
PyPDFDirectoryLoader – For loading PDF documents from a directory.
