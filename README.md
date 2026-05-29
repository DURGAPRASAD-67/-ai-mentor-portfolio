# ai-mentor-portfolio - Setti Durgaprasad

## AI Tool Usage

### ChatGPT

I would use ChatGPT for content creation because it explains ideas clearly and quickly.

### Claude

I would use Claude for file creation because it can provide downloadable documents and complete outputs.

### Gemini

I would use Gemini for simple step-by-step explanations when I want a basic answer, even if it is not always as strong as the others.

### Perplexity

I would use Perplexity for fast, source-backed research and clear explanations.

Day 1 — Setup complete

- ✅ Google AI Studio API key provisioned
- ✅ Groq API key provisioned
- ✅ Hello-Gemini call working — see
- 
- <img width="824" height="218" alt="image" src="https://github.com/user-attachments/assets/b5cb9ddc-9f5b-4893-9dca-d68ce1dbab48" />

4-tool comparison matrix from Lab 1A: see screenshot below
  
<img width="610" height="217" alt="image" src="https://github.com/user-attachments/assets/4a9c435d-ba02-4b8b-a0b2-9b9f2c176548" />


#4A Lab_Infosys_brief
# Unlock Your Tech Career: Ace Your Infosys Placement

A step-by-step guide for B.Tech students to crack one of India's most coveted campus placements — from eligibility to offer letter.

---

# Why Infosys?

With 350,000+ employees across 50+ countries, Infosys is a global powerhouse in digital transformation.

## Innovation at Scale
Leading AI, cloud, and digital solutions for Fortune 500 clients worldwide.

## Global Exposure
International projects, structured career programs, and continuous learning.

## Culture of Excellence
A dynamic environment fostering innovation, collaboration, and growth.

---

# Your Path to Infosys: The Hiring Process

Four stages stand between you and your offer letter. Know each one cold.

1. **Online Assessment**
   - Aptitude
   - Coding
   - Verbal via InfyTQ

2. **Technical Interview**
   - DSA
   - Projects
   - Problem-solving

3. **HR Interview**
   - Communication
   - Cultural fit

4. **Final Selection**
   - System Engineer
   - Specialist Programmer
   - Power Programmer

> Each stage is a filter — prepare strategically for all four to maximize your chances.

---

# Infosys's Technical Landscape

## Core Technologies
- Java
- Python
- C++
- .NET
- SQL
- JavaScript

## Emerging Tech
- AI
- ML
- Cloud (AWS, Azure, GCP)
- Data Analytics
- Cybersecurity
- DevOps

## Infosys Platforms

### InfyTQ
Learning & certification platform.

### HackWithInfy
Annual coding competition.

> Start your InfyTQ certification early — it's a strong differentiator in the selection process.

---

# Are You Eligible?

## Key Requirements

Infosys maintains consistent academic benchmarks across all hiring cycles. Check your college's placement cell for the exact criteria applicable to your batch.

### Degree
- B.E./B.Tech
- M.E./M.Tech
- MCA
- M.Sc. (CS/IT)

### Marks / CGPA
- Minimum 60% or 6.5 CGPA throughout
- Some hiring cycles may allow 55%

### Backlogs
- Zero active backlogs at onboarding

---

# Infosys in the News: Driving the Future

## Infosys Topaz — AI-First Strategy
Infosys is investing heavily in AI with Infosys Topaz, embedding AI across services and operations.

## Net-Zero by 2040
Committed to net-zero emissions by 2040 with green IT and sustainable practices.

## Expanding Global Partnerships
Deepening collaborations with AWS, Microsoft, and Google to deliver cutting-edge digital transformation.

---

# 5 Essential Prep Tips to Secure Your Spot

## 1. Master the Fundamentals
Solidify DSA and OOP concepts.

## 2. Practice Coding Daily
Solve problems on:
- LeetCode
- GeeksforGeeks
- InfyTQ

## 3. Ace Aptitude & Reasoning
Practice:
- Quantitative aptitude
- Logical reasoning
- Verbal ability

## 4. Mock Interviews
Simulate real interview conditions to refine your responses.

## 5. Stay Updated
Follow Infosys news, tech trends, and company values.

---

# Your Future Starts Now: Prepare This Week!

Every day you wait is a day someone else gets ahead. Start today.

## Download InfyTQ
Install the app and begin your certification journey.

## Register for HackWithInfy
Compete, learn, and get noticed by recruiters.

## Start Your Prep Plan
Block time daily for:
- Aptitude practice
- Coding
- Mock interviews

> Your dream career at Infosys is within reach. The only question is — are you ready to start?

````markdown id="krm2fp"
# Day 4 — n8n Daily News Digest

## Overview
Built an automated AI-powered placement news digest workflow using self-hosted n8n, RSS feeds, Groq AI summarization, and Gmail SMTP.

---

## Features
- ✅ Self-hosted n8n using Docker on AWS Ubuntu
- ✅ Automated workflow scheduled daily at 7:00 AM IST
- ✅ RSS feed integration for latest tech and placement news
- ✅ AI summarization using Groq (`llama-3.3-70b-versatile`)
- ✅ Email delivery using Gmail SMTP
- ✅ Workflow exported as JSON

---

## Workflow Architecture

```text
Schedule Trigger
      ↓
RSS Read
      ↓
Limit Node
      ↓
Code Node
      ↓
HTTP Request (Groq AI)
      ↓
Send Email (SMTP)
````

---

## Cron Schedule

Runs every day at 7:00 AM IST.

```cron
0 0 7 * * *
```

Cron format used in n8n:

```text
[Second] [Minute] [Hour] [Day of Month] [Month] [Day of Week]
```

Timezone:

```text
Asia/Kolkata
```

---

## Technologies Used

* n8n
* Docker
* AWS EC2 Ubuntu
* RSS Feeds
* Groq API
* Gmail SMTP

---

## Files

* `Day4_NewsDigest.json` — exported n8n workflow
* `daily_digest_test_email.png` — test email screenshot

---

## Test Email Screenshot

<img width="688" height="306" alt="image" src="https://github.com/user-attachments/assets/cdb1eabd-7548-4650-b2ff-db1c3cdaeccb" />


---

## Status

* ✅ Workflow tested successfully
* ✅ Email delivery working
* ✅ Daily automation configured

```
```
## Day 5 Lab 5B — Hugging Face Pulls

### Models tested
- `facebook/bart-large-mnli` — zero-shot classification
- `distilbert-base-uncased-finetuned-sst-2-english` — sentiment

### Timing comparison

| | min | avg | Notes |
|---|---|---|---|
| HF Inference API | N/A | N/A | DNS/network resolution failed in Colab runtime |
| Local in Colab | 1.92s | 2.31s | Stable after initial model download |

### When to use each

1. API is useful for lightweight apps and avoids downloading models locally.
2. Local inference is more reliable for batch processing and restricted environments.
3. Production rule: use API for small workloads, self-host/local for large-scale inference.

## Day 6 — Capstone Sprint 1: PlacementDataProcessor

### Engineer Answer

1. **PROBLEM** — JDs from Naukri / LinkedIn are messy text — placement cells need structured data to filter ("which JDs want Java + CGPA 7+?"). Manual extraction is unscalable for 50+ JDs.

2. **ARCHITECTURE** — JD URL → BeautifulSoup scraper (extract clean text) → Gemini structured-output call (response_schema=JD Pydantic) → JSON Lines file. Validation at each step; retry on schema fail.

3. **TRADE-OFFS** —
   - Cost: free Gemini ~1 JD/sec on average; ~30K tokens/day quota → ~5K JDs/day.
   - Accuracy: Pydantic catches schema violations but not semantic errors (e.g., model says skill is "Python" when source says "Python 3.12 specifically").
   - Latency: ~2-5s per JD (Gemini call dominant).
   - Complexity: scraping fragile (sites block automation). Cached fallback is mandatory.

4. **SCALE** —
   - 10 JDs/day: trivial. Today's lab.
   - 100 JDs/day: still in free quota. Add overnight batch + sleep between calls.
   - 10K JDs/day: free tier breaks. Move to paid Gemini OR self-host an open model.

5. **INTERVIEW ANSWER** — "I built a structured-output pipeline that turns scraped JDs into clean filterable JSON, using free Gemini and Pydantic. Schema-first design with retry-on-failure made it production-shaped on a free-tier API."

### Files
- `Day6_PlacementProcessor.ipynb` — the notebook
- `data/jds.jsonl` — output of this sprint, input for Day 7 RAG

# Hello-LangGraph Agent

A simple ReAct AI Agent built using LangGraph and Gemini.

This project demonstrates:
- Tool Calling
- ReAct Architecture
- AI Reasoning
- Web Search Integration
- Weather Tool Integration
- Trace Debugging

---

# Features

✅ Web Search Tool  
✅ Weather Tool  
✅ ReAct Agent  
✅ Full Conversation Trace  
✅ Multi-tool Agent Support  

---

# Technologies Used

- Python
- LangGraph
- LangChain
- Gemini API
- DuckDuckGo Search

---

# Installation

Install required libraries:

```bash
pip install langgraph langchain-google-genai langchain-community duckduckgo-search

readme = r"""# RAG Chatbot for Placement Preparation

LAB: 7B This project demonstrates a *Retrieval-Augmented Generation (RAG) Chatbot* built using:

- *ChromaDB* for vector storage
- *Sentence Transformers* for embeddings
- *LangChain* for orchestration
- *Google Gemini API* for conversational responses

The chatbot is designed to help students with:

- Placement job descriptions
- Required technical skills
- Semester syllabus topics
- Company hiring information
- Interview preparation queries

---

## Features

- Store placement/job data in a vector database
- Semantic search using embeddings
- Retrieval-based question answering
- Gemini-powered conversational responses
- Persistent local vector database using ChromaDB

---

## Technologies Used

- Python
- ChromaDB
- Sentence Transformers
- LangChain
- Google Gemini API
- HuggingFace Embeddings

---

## Project Workflow

1. Install required dependencies
2. Load embedding model
3. Create ChromaDB vector collection
4. Insert placement/job description data
5. Insert syllabus topic chunks
6. Configure LangChain retriever
7. Connect Gemini LLM
8. Ask placement-related question

Day 9 — Capstone Sprint 4: Career Agent
Multi-tool LangGraph ReAct agent
3 tools integrated:
jd_fetcher
skills_gap
answer_scorer
Failure recovery tested successfully
Reflection
Agents choose tools dynamically.
Tool docstrings guide reasoning.
Explicit ERROR handling prevents hallucination.
