
# Instructions


```
# Download QA data in txt format under some path eg. data/serverless
# Save in a file named qa.txt.

Disclaimer: The sample data in this repo are generated automatically by an LLM for a fictional product and meant to have no relation with an existing product. Any resemblance is purely coincidental.

# Install Ollama and pull the models
ollama pull llama3:instruct
olllama pull mxbai-embed-large

# Ingest txt Q&A data in Chroma DB
uv run src/data/qa_ingest.py ./data/serverless/qa.txt /tmp/ch_db

# Run the Chat Streamlit app
source .venv/bin/activate

python -m streamlit run ./src/qa/qa_st.py

# Alternatively:

uv run python -m streamlit run ./src/qa/qa_st.py
```

# Interacting with the Q&A Assistant

![ui](./ui.png)