# Sentiment Responder

A Streamlit app that classifies a customer review as positive or negative and drafts a matching reply.

## Why this exists
Practice with LangChain conditional branching: choosing the next step based on an LLM's earlier answer.

## What it does
- Classifies the review's sentiment with GPT-4 into a fixed schema (positive or negative)
- Routes to a different reply prompt for each sentiment with `RunnableBranch`
- Shows the detected sentiment and the drafted reply

## Project structure
```
SentimentResponder/
├── conditionalchain.py  Streamlit app and LangChain chain
└── requirements.txt     Python dependencies
```

## Getting started
Requirements: Python 3.10+, an OpenAI API key.
```bash
git clone https://github.com/abhijha8287/SentimentResponder.git
cd SentimentResponder
pip install -r requirements.txt streamlit
mkdir -p .streamlit && echo 'api_key = "sk-..."' > .streamlit/secrets.toml
streamlit run conditionalchain.py
```

## Configuration
| Variable | Purpose |
|:--|:--|
| `api_key` in `.streamlit/secrets.toml` | OpenAI API key |

## Tech stack
Python, LangChain, OpenAI GPT-4, Streamlit

## Notes
Live demo: https://sentimentresponder.streamlit.app (on the free Streamlit tier it may take a few seconds to wake up). `requirements.txt` lists more LangChain integrations than the app uses; only OpenAI is needed.
