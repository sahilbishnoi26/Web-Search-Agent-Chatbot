# Web-Search-Agent-Chatbot
An AI chatbot built using LangGraph, FastAPI, Tavily, and Streamlit, where users can define the agent's behavior through a prompt. The chatbot answers queries using large language models (LLMs) and integrated web search for real-time, context-aware responses.

## Features
- Supports Groq and OpenAI models.
- Allows users to define custom system prompts.
- Optional integration with Tavily Search for web results.
- User-friendly Streamlit interface.
- FastAPI backend for request processing and API management.

## Technologies Used
- LangChain: Handles integrations with Groq and OpenAI models.
- Streamlit: Provides the frontend UI for users to interact with the chatbot.
- FastAPI: Manages backend communication and serves as the API.
- Pydantic: Validates input data from the frontend.
- Tavily Search: Adds optional web search functionality for enhanced responses.

## Installation

### Clone the repository
```
git clone https://github.com/yourusername/Web-Search-Agent-Chatbot.git
cd Web-Search-Agent-Chatbot
```

### Install dependencies
1. Create and activate a virtual environment:
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
2. Install required packages:
```
pip install -r requirements.txt
```

### Setup API Keys
1. Create a `.env` file in the project root:
```
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
OPENAI_API_KEY=your_openai_api_key
```
2. Save the file.

## Usage

### Run the backend
```
python backend.py
```
- The FastAPI server will be available at `http://127.0.0.1:9999`.

### Run the frontend
```
streamlit run frontend.py
```
- Open the Streamlit UI in your browser to interact with the chatbot.

![alt text](https://github.com/sahilbishnoi26/Web-Search-Agent-Chatbot/blob/main/pic.png)
![alt text](https://github.com/sahilbishnoi26/Web-Search-Agent-Chatbot/blob/main/pic2.png)

## Troubleshooting

### Common Issues
1. Invalid Model Name:
   - Ensure the selected model name matches one of the `ALLOWED_MODEL_NAMES` in `backend.py`.

2. Environment Variables Not Found:
   - Ensure the `.env` file is correctly configured and located in the project root.

3. Backend Server Not Running:
   - Verify that `backend.py` is running before interacting with the UI.

## Notes
- API documentation is available at `http://127.0.0.1:```9/docs`.
