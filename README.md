# Prompt Engineering with Groq and LangChain

## Project Description

This project demonstrates how to use Prompt Engineering with Groq's Large Language Models (LLMs) using LangChain.

The project covers:

- Installing required libraries
- Loading API keys securely
- Connecting to Groq
- Sending prompts
- Receiving AI responses
- Understanding Prompt Engineering basics

---

# Prerequisites

Before starting, install:

- Python 3.10+
- VS Code (or Google Colab)
- Groq Account
- Groq API Key

---

# Required Libraries

Install using:

```bash
pip install groq
```

or

```bash
pip install groq langchain-groq python-dotenv
```

or

```bash
pip install groq langchain-core langchain-groq python-dotenv
```

---

# Project Structure

```
Project/
│
├── .env
├── PromptEngineering.ipynb
├── README.md
```

---

# Create .env File

Create a file named

```
.env
```

Add

```
GROQ_API_KEY=your_api_key_here
```

Example

```
GROQ_API_KEY=gsk_xxxxxxxxxxxxxxxxx
```

---

# Import Required Libraries

```python
from dotenv import load_dotenv
import os
from langchain_groq import ChatGroq
from langchain_core.prompts import PromptTemplate
```

---

# Load API Key

```python
load_dotenv()

groq_api_key = os.getenv("GROQ_API_KEY")
```

Purpose

- Reads API key securely
- Avoids hardcoding credentials

---

# Create LLM

```python
llm = ChatGroq(
    model="llama-3.3-70b-versatile",
    api_key=groq_api_key
)
```

Purpose

Creates a connection between Python and Groq's LLM.

---

# Send Prompt

```python
response = llm.invoke("What is Prompt Engineering?")
```

Purpose

Sends the prompt to the AI model.

---

# Display Output

```python
print(response.content)
```

Purpose

Displays the AI-generated response.

---

# Technologies Used

- Python
- Groq API
- LangChain
- Prompt Engineering
- dotenv

---

# Concepts Covered

- Environment Variables
- API Keys
- Prompt Engineering
- LLMs
- LangChain
- ChatGroq
- invoke()
