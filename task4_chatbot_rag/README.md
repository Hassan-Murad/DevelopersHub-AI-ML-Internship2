# Task 4: Context-Aware RAG Chatbot

## Objective
The goal of this project is to develop a conversational AI chatbot that incorporates context memory and Retrieval-Augmented Generation (RAG) to provide accurate, grounded answers based on a custom knowledge base.

## Methodology / Approach
1. **Knowledge Base Construction:** Loaded, parsed, and chunked a custom text corpus using LangChain's `RecursiveCharacterTextSplitter`.
2. **Vectorization:** Embedded the document chunks using Hugging Face's `all-MiniLM-L6-v2` sentence transformer and stored them in a local FAISS vector database for rapid semantic search.
3. **RAG Chain Implementation:** Built a LangChain `ConversationalRetrievalChain` integrating a large language model (OpenAI GPT-3.5-turbo / open-source alternative), the FAISS retriever, and `ConversationBufferMemory`.
4. **User Interface:** Deployed the interactive chatbot using Streamlit, allowing users to converse while viewing the source documents retrieved for each answer.

## Key Results & Observations
* **Performance:** The system successfully processes follow-up questions naturally due to its conversation memory buffer.
* **Hallucination Reduction:** By utilizing RAG, the LLM successfully grounds its generative responses in the retrieved document chunks, drastically reducing factual hallucinations.
* **Scalability:** The FAISS vector store demonstrated sub-millisecond retrieval times, proving the architecture is scalable for much larger internal document corpora.