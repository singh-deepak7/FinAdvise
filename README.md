# 💰 FinAdvise

An AI-powered Financial Assistant built using LangGraph, Streamlit, and Groq.

## Features

- LangGraph Workflow
- Human-in-the-Loop
- ReAct Agent
- Stock Price Lookup
- Budget Planning
- Expense Tracking
- User Profile Extraction
- Memory
- Checkpointing
- Resume with Command()

---

## Architecture

```

                 Streamlit

                      │

                      ▼

              LangGraph Graph

                      │

             Risk Assessment

                      │

           High Risk?

          /          \

interrupt()      ReAct Agent

         \          /

          Human Approval

                │

                ▼

            Tool Calling

                │

                ▼

          Final Response

```

---

## Project Structure

```

finance-hitl/

├── app.py

├── graph.py

├── nodes.py

├── tools.py

├── prompts.py

├── config.py

├── state.py

├── agent.py

├── requirements.txt

└── README.md

```

---

## Install

```bash
python -m venv .venv

source .venv/bin/activate
```

Windows

```powershell
.venv\Scripts\activate
```

Install packages

```bash
pip install -r requirements.txt
```

---

## Configure

Create a `.env`

```text
GROQ_API_KEY=xxxxxxxx

ALPHA_VANTAGE_API_KEY=xxxxxxxx
```

---

## Run

```bash
streamlit run app.py
```

---

## Human Approval Workflow

```

User

↓

Risk Assessment

↓

High Risk?

↓

interrupt()

↓

Human Approves

↓

Command(resume="approve")

↓

Continue Graph

↓

Answer

```

---

## Technologies

- LangGraph
- LangChain
- Streamlit
- Groq Llama 3.3
- Alpha Vantage
- Python

---

## Future Enhancements

- Persistent memory using SQLite/PostgreSQL checkpointer
- RAG over financial documents
- Multi-agent supervisor architecture
- MCP tool integration
- LangSmith tracing
- Authentication and user profiles
- Portfolio analytics
- Financial news integration