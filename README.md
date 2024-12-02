Retrieval-Augmented Generation with OpenAI Embeddings and Chroma

This project demonstrates the implementation of Retrieval-Augmented Generation (RAG) using OpenAI's Embedding API and the Chroma vector database. The workflow focuses on extracting contextual information from a dataset of documents, storing vectorized representations, and performing semantic search to retrieve relevant information based on user queries.

Features
Document Processing:

Load and preprocess documents from a directory.
Split large documents into smaller, manageable chunks using RecursiveCharacterTextSplitter.
Embedding Generation:

Use OpenAI's embedding model to generate vector representations of document chunks for semantic search.
Vector Database:

Store and manage embeddings in a persistent Chroma database.
Perform similarity search to retrieve context for queries.
Query Handling:

Input user queries to the system.
Retrieve relevant document chunks based on semantic similarity.
Generate responses using retrieved context and OpenAI's ChatGPT model.

Project Workflow
Data Preprocessing:

Load Markdown files from the specified directory (data/books).
Split the documents into smaller chunks with overlap to preserve context.
Embedding Storage:

Generate embeddings for each chunk using OpenAI's text-embedding-ada-002 model.
Persist embeddings in a Chroma vector database.
Query Execution:

Accept user queries via the command line.
Retrieve relevant chunks using similarity_search_with_relevance_scores from Chroma.
Construct a prompt with the retrieved context and query.
Response Generation:

Use OpenAI's ChatGPT API to generate responses based on the retrieved context.
Display responses along with the sources of information.
