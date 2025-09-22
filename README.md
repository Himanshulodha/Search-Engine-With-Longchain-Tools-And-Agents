"C:\Users\himan\Downloads\d2ffd8b5-1ec3-4fbf-bdcc-f2e04c590589.webm"
# Search-Engine-With-Longchain-Tools-And-Agents

This project demonstrates how to build a search-powered conversational AI agent using LangChain and Groq LLMs, wrapped in a clean Streamlit UI.
The chatbot doesn’t just generate answers from a single model — instead, it uses LangChain Agents that can reason, choose tools, and act before responding.

🔧 How It Works

LLM Backbone (Groq LLM)

The core reasoning engine is powered by Groq’s llama-3.1-8b-instant model.
It interprets the user’s queries and decides how to solve them.

LangChain Agent

The app uses ZERO_SHOT_REACT_DESCRIPTION agent type.
This means the agent can “think step by step,” deciding when to search and which tool to use — without any predefined training examples.

Integrated Tools

📰 Wikipedia Tool – fetches concise, reliable summaries for general knowledge queries.
📚 Arxiv Tool – retrieves abstracts of academic research papers, useful for technical/scientific queries.
🔍 DuckDuckGo Tool – performs real-time web searches for the latest information or broader topics.

Agent Execution Flow

User enters a query in the Streamlit chat.
The agent analyzes the query and selects the most relevant tool (Wikipedia, Arxiv, or DuckDuckGo).
The tool fetches external data.
The agent integrates the results and responds conversationally.

Interactive UI

Powered by Streamlit, showing both the chat and the agent’s thought process (via StreamlitCallbackHandler).
Maintains chat history so the conversation feels natural and continuous.

⚙️ Installation

Clone the repo

git clone https://github.com/your-username/Search-Engine-With-Langchain-Tools-And-Agents.git
cd Search-Engine-With-Langchain-Tools-And-Agents


Create a virtual environment

python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows


Install dependencies

pip install -r requirements.txt


If requirements.txt is not created yet, generate one:

pip freeze > requirements.txt

🔑 Environment Variables

Create a .env file in the project root:

GROQ_API_KEY=your_groq_api_key_here
HF_TOKEN=your_huggingface_token_here


⚠️ Important: Do not commit .env to GitHub (already added to .gitignore).

▶️ Usage
Run the Streamlit app:
streamlit run app.py


Open your browser at:
👉 http://localhost:8501

You’ll see a chatbot interface where you can:
Ask research-based queries → answered via Arxiv
General knowledge → answered via Wikipedia
Broader topics → answered via DuckDuckGo

📸 Demo (Screenshot/GIF)
(Add a screenshot of your Streamlit app here)

🛠️ Tech Stack

Python
Streamlit
LangChain
Groq API
Arxiv API
Wikipedia API
DuckDuckGo Search

🧑‍💻 Author
Himanshu Lodha
💼 LinkedIn
📂 GitHub
