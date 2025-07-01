# MapReduce PDF Summarizer

This project demonstrates context-aware parsing and summarization of large PDF documents using Adobe PDF Services, LangChain, Pinecone, and OpenAI. It extracts structured data from PDFs, chunks the content, indexes it for semantic search, and summarizes it using a MapReduce approach with LLMs.

## Features

- **PDF Extraction:** Uses Adobe PDF Services API to extract text and tables from PDFs.
- **Chunking:** Splits extracted content into contextual sections.
- **Indexing:** Embeds and indexes chunks in Pinecone for semantic search.
- **Summarization:** Summarizes large documents using LangChain's MapReduce chains and OpenAI models.

## Requirements

- Python 3.8+
- Adobe PDF Services API credentials
- Pinecone API key and environment
- OpenAI API key

## Installation

1. **Clone the repository:**
   ```bash
   git clone <repo-url>
   cd MapReduce
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables:**

   Create a `.env` file in the project root with the following content:
   ```
   PINECONE_API_KEY=your_pinecone_api_key
   PINECONE_ENV=your_pinecone_env
   OPENAI_API_KEY=your_openai_api_key
   pdf_extract_client_id=your_adobe_client_id
   pdf_extract_client_secret=your_adobe_client_secret
   ```

## Usage

1. **Configure file paths** in `parse.py` for your PDF input and output directories.

2. **Run the script:**
   ```bash
   python parse.py
   ```

3. **Steps performed:**
   - Extracts and chunks the PDF (uncomment the relevant line in `__main__`).
   - Loads chunks as documents.
   - (Optional) Indexes documents in Pinecone.
   - Summarizes the content using MapReduce with OpenAI.

## References

- [LangChain Summarization]([https://python.langchain.com/docs/use_cases/summarization](https://python.langchain.com/docs/tutorials/summarization/))
- [Adobe PDF Services API](https://developer.adobe.com/document-services/docs/overview/pdf-extract-api/)
- [Pinecone Vector Database](https://www.pinecone.io/)
- [OpenAI API](https://platform.openai.com/)

## License

MIT License

---

**Note:** Make sure you have valid API keys and sufficient quota for Adobe, Pinecone, and OpenAI services.
