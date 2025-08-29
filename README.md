# Document Chunking Strategies

This project demonstrates 5 different types of document chunking strategies using LangChain for text processing and analysis.

## Overview

Document chunking is a crucial preprocessing step in many NLP applications, especially for Retrieval-Augmented Generation (RAG) systems. This repository explores various chunking strategies to help you understand which approach works best for your specific use case.

## Chunking Strategies Covered

1. **Character Text Splitting** - Basic splitting based on character count
2. **Token-based Chunking** - Basic splitting based on token count
3. **Recursive Character Text Splitting** - Smart splitting that preserves structure
4. **Markdown Header Text Splitting** - Splits based on markdown headers
5. **Semantic Chunking** - AI-powered chunking based on semantic similarity

## Setup

### Prerequisites
- Python 3.9+
- Conda or virtual environment (recommended)

### Installation

1. Clone this repository
2. Activate your environment:
   ```bash
   conda activate /path/to/your/environment
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### API Key Configuration

**Important:** For semantic chunking functionality, you need an OpenAI API key.

1. Get your API key from [OpenAI Platform](https://platform.openai.com/api-keys)
2. Set it as an environment variable:
   ```bash
   export OPENAI_API_KEY="your-api-key-here"
   ```
3. Or pass it directly to the OpenAIEmbeddings function:
   ```python
   from langchain_openai import OpenAIEmbeddings
   embeddings = OpenAIEmbeddings(api_key="your-api-key-here")
   ```

**Note:** The semantic chunking examples using `OpenAIEmbeddings` will not work without a valid API key.

## Usage

Open the Jupyter notebook `Chunking-strategies/5-Types-langchain-chunking.ipynb` and run the cells to explore different chunking strategies.

### Sample Files Included
- `SteveJobsSpeech.txt` - Sample text file for basic chunking examples
- `examplemdfile.md` - Sample markdown file for header-based chunking

## Dependencies

Key packages used in this project:
- `langchain` - Main framework for text processing
- `langchain-community` - Community extensions
- `langchain-experimental` - Experimental features (for semantic chunking)
- `langchain-openai` - OpenAI integrations
- `langchain-text-splitters` - Text splitting utilities

See `requirements.txt` for the complete list of dependencies.

## Contributing

Feel free to contribute by adding new chunking strategies or improving existing examples.

