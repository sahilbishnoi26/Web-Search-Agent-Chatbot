# Web-Search-Agent-Chatbot
An AI chatbot built using LangGraph, FastAPI, Tavily, and Streamlit, where users can define the agent's behavior through a prompt. The chatbot answers queries using large language models (LLMs) and integrated web search for real-time, context-aware responses.

## Features
- Support for multiple AI providers: Groq and OpenAI.
- Dynamic model selection with Groq and OpenAI language models.
- User-defined system prompts for tailored AI behavior.
- Integration of a web search tool for retrieval-augmented responses.
- User-friendly Streamlit interface for seamless interaction.
- Backend API built with FastAPI for scalable communication.

## Technologies Used
- **LangGraph** for AI agent setup.
- **FastAPI** for backend API.
- **Streamlit** for the frontend interface.
- **Pydantic** for request validation.
- **Tavily Search Results** for retrieval-augmented responses.

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/ai-chatbot-agents.git
cd ai-chatbot-agents
```

### 2. Create and Activate Virtual Environment
#### On Windows:
```bash
python -m venv env
env\Scripts\activate
```
#### On macOS/Linux:
```bash
python3 -m venv env
source env/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

## Usage

### 1. Start the Backend Server
Run the following command to launch the FastAPI server:
```bash
python backend.py
```

### 2. Launch the Frontend Interface
Start the Streamlit interface:
```bash
streamlit run frontend.py
```

### 3. Interact with the AI Agent
- Open the Streamlit interface in your browser (usually at `http://localhost:8501`).
- Define the system prompt, select a provider and model, and input your query.
- Click "Ask Agent!" to receive a response.

## Troubleshooting
### Common Issues and Solutions

1. **Missing API Keys**
   - Ensure `GROQ_API_KEY`, `TAVILY_API_KEY`, and `OPENAI_API_KEY` are set in your environment variables.
   - Use a `.env` file or export the keys manually:
     ```bash
     export GROQ_API_KEY=your_key
     export TAVILY_API_KEY=your_key
     export OPENAI_API_KEY=your_key
     ```

2. **Port Conflicts**
   - If `127.0.0.1:```9` is unavailable, change the port in `backend.py`:
     ```python
     uvicorn.run(app, host="127.0.0.1", port=YOUR_PORT)
     ```

3. **Dependencies Not Installed**
   - Ensure the virtual environment is activated and run:
     ```bash
     pip install -r requirements.txt
     ```

4. **Frontend Not Connecting to Backend**
   - Verify the backend is running at `http://127.0.0.1:```9`.
   - Check the `API_URL` in `frontend.py` matches the backend URL.

5. **Model Selection Error**
   - Ensure the model name selected is in the allowed list:
     ```python
     ALLOWED_MODEL_NAMES=["llama3-70b-8192", "mixtral-8x7b-32768", "llama-3.3-70b-versatile", "gpt-4o-mini"]
     ```
