# AI Agentic Chatbot Using Multi-LLM Pipeline

This project implements an AI chatbot that represents **Oluwatosin** on their website by answering questions related to their career, background, skills, and experience. The chatbot uses a multi-LLM pipeline integrating OpenAI and Groq AI models for response generation and quality evaluation.

---

## Features

- **Context-aware chatbot:** Uses a detailed system prompt including a summary and LinkedIn profile to maintain persona fidelity.
- **Multi-LLM evaluation:** Chat responses are evaluated for quality and relevance by a secondary LLM (Groq AI) before being delivered.
- **Dynamic re-generation:** If a response is deemed unacceptable, the chatbot retries generating a better answer.
- **PDF text extraction:** Parses LinkedIn profile PDF for enriching chatbot context.
- **Gradio-based web UI:** Simple, interactive chat interface accessible locally or deployed with a public link.

---

## Setup and Usage

1. **Environment variables:**  
   Create a `.env` file with the following keys:  
   ```env
   OPENAI_API_KEY=your_openai_api_key
   groq_api_key=your_groq_api_key
2. Install dependencies:

   pip install -r requirements.txt
(Make sure you have packages like openai, pypdf, gradio, pydantic, and python-dotenv installed.)

3. Prepare resources:

Place Profile.pdf and summary.txt in the me/ directory for the chatbot context.

4. Run the chatbot:


python your_script_name.py

When you run the script, you will see an output like:

* Running on local URL:  http://127.0.0.1:7877
* To create a public link, set `share=True` in `launch()`.
Passed evaluation - returning reply
