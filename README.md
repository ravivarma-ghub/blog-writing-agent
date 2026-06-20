# AI Blog Writer Agent

An intelligent multi-agent blog generation system built using **LangGraph**, **Streamlit**, **LLMs**, **Web Research**, and **AI Image Generation**.

The application automatically researches a topic, creates a content plan, generates high-quality blog sections in parallel, produces technical diagrams using AI, and exports a complete blog with downloadable assets.

---

## Features

### Intelligent Blog Planning

* Automatically analyzes the topic
* Determines whether web research is required
* Creates a structured blog outline
* Generates section-wise writing tasks

### Multi-Agent Content Generation

* Built using LangGraph
* Uses a Planner → Worker → Reducer architecture
* Parallel content generation for faster execution
* Supports technical, educational, and research-based blogs

### Automated Web Research

* Searches the web for recent information
* Collects and filters evidence
* Adds citations for factual content
* Supports evergreen and time-sensitive topics

### AI Image Generation

* Automatically identifies sections that need diagrams
* Generates technical illustrations using AI
* Inserts images directly into markdown
* Supports architecture diagrams, workflows, and visual explanations

### Blog Export

* Download generated markdown
* Download images separately
* Download complete blog bundle (Markdown + Images)

### Blog History

* Load previously generated blogs
* Preview and re-download existing content

---

## Architecture

```text
User Topic
    │
    ▼
Router
    │
    ├── Research Required?
    │
    ▼
Research Agent
    │
    ▼
Orchestrator
    │
    ▼
Parallel Worker Agents
    │
    ▼
Reducer
 ├── Merge Content
 ├── Plan Images
 └── Generate Images
    │
    ▼
Final Blog
```

---

## Tech Stack

### Frontend

* Streamlit

### Workflow Orchestration

* LangGraph

### LLMs

* Groq / Grok / OpenAI (Configurable)

### Search

* Tavily Search API

### Image Generation

* Google Gemini Image Models

### Data Validation

* Pydantic

### Environment Management

* Python Dotenv

---

## Project Structure

```text
project/
│
├── app.py
├── bwa_backend.py
├── .env
├── images/
├── generated_blogs/
├── requirements.txt
└── README.md
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/ai-blog-writer.git
cd ai-blog-writer
```

### Create Virtual Environment

```bash
python -m venv venv
```

Activate environment:

Windows

```bash
venv\Scripts\activate
```

Linux/Mac

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file:

```env
GROQ_API_KEY=your_groq_api_key

TAVILY_API_KEY=your_tavily_api_key

GOOGLE_API_KEY=your_google_api_key
```

---

## Running the Application

```bash
streamlit run app.py
```

Open:

```text
http://localhost:8501
```

---

## Example Topics

### AI Agents

```text
How AI Agents Work: Architecture, Memory, Planning, Tool Use, and Multi-Agent Systems
```

### RAG Systems

```text
Building a Production-Ready RAG System with LangGraph, FastAPI, FAISS, and Groq
```

### Generative AI

```text
The Evolution of Artificial Intelligence: From Perceptrons to Large Language Models and Agentic AI
```

### Career Roadmap

```text
The Complete Roadmap to Becoming an AI Engineer in 2026
```

---

## Workflow Details

### Router Agent

Determines whether the topic requires:

* Closed-book generation
* Hybrid generation
* Open-book generation with research

### Research Agent

Collects and filters relevant information from the web.

### Orchestrator Agent

Creates a detailed blog plan and writing tasks.

### Worker Agents

Generate blog sections independently in parallel.

### Reducer Agent

Combines sections into a complete blog.

### Image Planner

Determines where images improve understanding.

### Image Generator

Creates technical diagrams and inserts them into the blog.

---

## Future Improvements

* PDF Export
* Word Document Export
* SEO Optimization
* Blog Publishing to Medium
* WordPress Integration
* Multi-language Support
* Human Feedback Loop
* Agent Performance Analytics

---

## Author

Ravi Varma

B.Tech CSE (AI & ML)
CVR College of Engineering

Passionate about AI Engineering, Generative AI, Agentic Systems, LangGraph, and Large Language Models.

---

