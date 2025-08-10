
# UdaPlay - AI Game Research Agent


This is the third project in Udacity AI Agent Nanodegree program.  
## Overview 

UdaPlay is an AI-powered research agent designed for the video game industry. It combines local knowledge retrieval with web search capabilities to provide accurate and comprehensive information about video games.

## Features
- Retrieval-Augmented Generation (RAG) system for local knowledge
- Web search integration for up-to-date information
- Structured response format
- Evaluation system for retrieval quality
- Memory management for maintaining conversation state

## Project Structure
```

project/
├── chromadb/          # Vector database storage
├── games/             # Game data JSON files
├── lib/               # Core library modules
└── ... .ipynb         # Jupyter notebooks
```
## Setup
1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Create `.env` file with required API keys:
   ```
   OPENAI_API_KEY="your-key"
   TAVILY_API_KEY="your-key"
   CHROMA_OPENAI_API_KEY="your-key"
   ```

## Usage
Run the Jupyter notebooks in order:
1. `Udaplay_01_starter_project.ipynb` - Sets up the vector database
2. `Udaplay_02_starter_project.ipynb` - Implements the AI agent

## Dependencies
- Python 3.11+
- ChromaDB
- OpenAI
- Tavily
- Other dependencies listed in requirements.txt

## License
[License](./LICENSE.md)


### Agent Performance Reflection

Based on the notebook execution results, here's an analysis of the agent's performance:

1. **Knowledge Retrieval**
   - The agent successfully uses the vector database for initial information retrieval
   - Effectively evaluates the quality of retrieved information
   - Seamlessly transitions to web search when local data is insufficient

2. **Query Handling Examples**
   - Answering using DB (e.g., "When was Pokémon Gold and Silver released?")
     - Demonstrates accurate retrieval from local database
     - Provides structured, clear responses

   - Answering using current information (e.g., "What is Rockstar Games working on right now?")
     - Successfully uses web search for up-to-date information
     - Maintains accuracy by citing reliable gaming news sources

3. **Strengths**
   - Structured output format
   - Clear source attribution
   - Effective evaluation of information quality
   - Smooth fallback to web search when needed

4. **Areas for Improvement**
   - Could benefit from more sophisticated memory management
   - Response formatting could be more consistent
   - Web search results could be better integrated with local knowledge

Overall, the agent demonstrates robust performance in handling various types of gaming-related queries, effectively combining local knowledge with web search capabilities.
