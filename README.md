# Debugging LangGraph Agents with LangSmith

Learn how to debug and trace LangGraph agent workflows using LangSmith.

## What You'll Learn

- **LangSmith Tracing** — Enable tracing to monitor every step of your agent
- **LangGraph Studio** — Deploy and test agents locally with LangGraph Studio
- **Tool Calling** — Build an agent with tool-calling capabilities and trace its execution

## Project Structure

```
debugging_with_langsmith/
├── agent.py           # Deployable agent (for LangGraph Studio)
├── debugging.py       # Interactive debugging script
├── langgraph.json     # LangGraph Studio configuration
├── requirements.txt
├── .env.example
└── README.md
```

## Setup

```bash
pip install -r requirements.txt
cp .env.example .env   # Add your API keys
python debugging.py
```

## LangGraph Studio

To use with LangGraph Studio, ensure `langgraph.json` points to the correct agent:

```json
{
    "dependencies": ["."],
    "graphs": {
        "tool_agent": "./agent.py:tool_agent"
    },
    "env": ".env"
}
```
