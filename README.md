# AI Travel Planning System (LangGraph Multi-Agent)

An AI-powered travel planning system built with **LangGraph**, **PostgreSQL**, **Groq**, and **Streamlit**. Multiple specialized agents collaborate to search flights and hotels, build a day-by-day itinerary, and return a unified trip plan with persistent conversation memory per user.

## Key Features

- **Flight Search Agent:** Looks up flight options and travel details via AviationStack API (`tools/flight_tool.py`).
- **Hotel Search Agent:** Gathers accommodation ideas and travel info using Tavily search (`tools/tavily_tool.py`).
- **Itinerary Planning Agent:** Organizes daily schedules, sightseeing, and budget constraints.
- **Final Response Agent:** Merges flight, hotel, and itinerary outputs into a cohesive travel plan.
- **Persistent Memory:** Stores checkpoints and conversation state in PostgreSQL via `langgraph-checkpoint-postgres`.
- **Interactive UI:** Streamlit web app (`frontend.py`) with per-user session IDs alongside CLI testing (`main.py`).

## Tech Stack

- **Orchestration & Memory:** LangGraph, LangChain, `langgraph-checkpoint-postgres`, `psycopg` / `psycopg_pool`
- **LLM Inference:** Groq (`openai/gpt-oss-120b` / `openai/gpt-oss-20b`)
- **APIs & Tools:** Tavily API, AviationStack API
- **Database:** PostgreSQL
- **Frontend:** Streamlit

## Project Structure

```text
AI-Travel-Planning-System-using-LangGraph/
├── tools/
│   ├── flight_tool.py
│   └── tavily_tool.py
├── frontend.py
├── main.py
├── .env.example
└── README.md