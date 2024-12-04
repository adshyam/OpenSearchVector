Overall Summary

This FastAPI application facilitates the ingestion and processing of multimodal data, such as PDF
files, for retrieval-augmented generation (RAG). It integrates tools like OpenSearch for vector
search, Azure Blob Storage for managing file storage, and OpenAI’s GPT models for generating
embeddings and summarizations. The main API endpoint, /SFRAG/retrieval, accepts PDF files
and processes their contents by extracting text, tables, and images. Extracted data is summarized
and indexed into a vector database to enable efficient semantic search and retrieval. The application
uses OpenSearchVectorSearch for managing the vectorized embeddings of documents and employs
LangChain modules for splitting and structuring text data for embedding generation. Summaries
are prepared for extracted text, tables, and images to optimize their use in retrieval systems,
emphasizing searchable and meaningful content.

The application’s functionality is highly modular, covering multiple tasks like validating and up-
loading files, extracting structured data from PDFs, and summarizing data using AI models like
GPT. For images, it identifies and resizes base64-encoded images, while for tables and text, it
generates detailed summaries that include structural and contextual information. Metadata associ-
ated with each data type is also enriched for efficient search and retrieval. The application further
integrates AWS OpenSearch Service for indexing and storing data while maintaining robust con-
figurations for SSL, retries, and timeouts. Additionally, it provides comprehensive error handling
for operations like file uploads, data extraction, and indexing. The entire system is designed to
deliver a seamless and efficient pipeline for processing and retrieving multimodal data in enterprise
applications.
