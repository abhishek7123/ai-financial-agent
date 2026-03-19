# AI Financial Agent

A local-inference ReAct-style AI agent for personal finance tracking 
using LangGraph, SQLite, and Splitwise integration.

## What it does
- Answers natural language expense queries  
  ("How much did I spend on groceries last month?")
- Syncs shared expenses from Splitwise with INR→USD currency conversion
- Generates category breakdowns and month-over-month spending comparisons
- Runs entirely on local hardware — no cloud API costs or data sharing

## Tools
| Tool | What it does |
|------|-------------|
| `add_expense` | Adds a new expense to SQLite |
| `run_query` | Executes dynamically generated SQL |
| `analyze_spending` | Month-over-month spending insights |
| `get_spending_trends` | Time-series trend data |
| `get_category_breakdown` | Category-wise spending breakdown |
| `sync_splitwise` | Syncs and converts Splitwise expenses |

## Tech stack
Python · LangGraph · SQLite · Splitwise API · Gradio

## Setup
```bash
git clone https://github.com/abhishek7123/ai-financial-agent
cd ai-financial-agent
pip install -r requirements.txt
cp .env.example .env
python db.py
python agent.py
```

## Evaluation
100% tool-selection accuracy across 6 structured benchmark queries.  
End-to-end latency: 12–15s on local hardware.
