# 🤖 HireGenie — AI-Powered Recruitment Automation Platform

> **A multi-agent AI recruitment system built by Priyanka Kumari, a 4th-year Data Science student.**

HireGenie is an **AI-powered recruitment automation platform** designed to streamline the early stages of the hiring process using **Large Language Models (LLMs), Natural Language Processing (NLP), and multi-agent AI systems**.

The project automates resume screening, candidate information extraction, skill-gap analysis, and personalized interview-question generation by using specialized AI agents working together through the **Microsoft AutoGen framework**.

---

## 👩‍💻 About the Developer

### Priyanka Kumari

**4th-Year Data Science Student | AI/ML & Data Science Enthusiast**

Priyanka is a final-year Data Science student interested in building practical applications using **Artificial Intelligence, Machine Learning, NLP, Generative AI, and intelligent agent systems**.

This project demonstrates her work in applying modern AI technologies to solve a real-world problem in **recruitment and talent assessment**.

🔗 **GitHub:** [priyankakumari0203](https://github.com/priyankakumari0203)

---

# 🎯 Project Overview

Traditional recruitment processes often require recruiters to manually review large numbers of resumes, compare candidates with job requirements, identify missing skills, and prepare interview questions.

HireGenie aims to automate these repetitive tasks through a collaborative **multi-agent AI architecture**.

### The system can:

* 📄 Parse candidate resumes
* 🔍 Compare resumes with job descriptions
* 🤖 Perform AI-assisted candidate screening
* 🧠 Identify candidate skill gaps
* 💬 Generate personalized interview questions
* 📊 Extract structured candidate information
* 💾 Store recruitment results in CSV format

---

# 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │    Job Description   │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    Candidate Resume  │
                    │      PDF / DOCX      │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Resume Processing &  │
                    │ Information Extraction│
                    └──────────┬───────────┘
                               │
                               ▼
              ┌────────────────────────────────┐
              │       Screening Agent           │
              │                                │
              │ Resume ↔ Job Description       │
              │ Matching & Evaluation          │
              └───────────────┬────────────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │      Skill-Gap Analysis        │
              │                                │
              │ Required Skills vs Candidate   │
              └───────────────┬────────────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │       Interview Agent          │
              │                                │
              │ Personalized Question          │
              │ Generation                     │
              └───────────────┬────────────────┘
                              │
                              ▼
              ┌────────────────────────────────┐
              │    Data Management Agent       │
              │                                │
              │ Candidate Information &        │
              │ Screening Results              │
              └───────────────┬────────────────┘
                              │
                              ▼
                     ┌─────────────────┐
                     │   CSV Output    │
                     └─────────────────┘
```

---

# 🤖 Multi-Agent System

HireGenie uses multiple specialized agents, each responsible for a specific recruitment task.

### 🔍 1. Screening Agent

Analyzes the candidate's resume against the provided job description.

**Responsibilities:**

* Resume analysis
* Job-description comparison
* Keyword-based matching
* AI-assisted candidate evaluation

---

### 💬 2. Interview Agent

Generates interview questions based on the candidate's profile and identified skill gaps.

**Responsibilities:**

* Analyze missing skills
* Generate technical questions
* Generate role-specific questions
* Create personalized interview preparation

---

### 📊 3. Data Management Agent

Handles structured candidate information and screening results.

**Responsibilities:**

* Extract candidate information
* Store candidate details
* Store screening results
* Generate structured CSV output

---

### 🧑‍💻 4. User Proxy Agent

Coordinates the overall workflow and facilitates communication between the specialized agents.

```text
                 User Proxy Agent
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
     Screening     Interview      Data
       Agent         Agent      Management
```

---

# 🛠️ Technology Stack

| Technology            | Purpose                           |
| --------------------- | --------------------------------- |
| **Python**            | Core development                  |
| **Microsoft AutoGen** | Multi-agent orchestration         |
| **GPT-4o-mini**       | LLM-based analysis and generation |
| **spaCy**             | NLP and text processing           |
| **pdfplumber**        | PDF resume extraction             |
| **docx2txt**          | DOCX processing                   |
| **CSV**               | Candidate data storage            |
| **python-dotenv**     | Environment configuration         |

---

# ✨ Key Features

### 📄 Resume Processing

Supports resume processing and extraction of relevant candidate information from documents.

### 🔎 Intelligent Screening

Compares candidate profiles against job requirements using keyword matching and AI-based evaluation.

### 🧠 Skill-Gap Detection

Identifies differences between the skills required for a role and the skills present in a candidate's resume.

### 💬 Personalized Interview Questions

Generates interview questions based on the candidate's identified skill gaps and target role.

### 🤝 Multi-Agent Collaboration

Different AI agents specialize in different recruitment tasks instead of relying on a single monolithic workflow.

### 📊 Structured Candidate Data

Candidate information and screening results can be stored in a structured CSV file for further processing.

---

# 🔄 End-to-End Workflow

```text
Resume Upload
      │
      ▼
Resume Information Extraction
      │
      ▼
Job Description Processing
      │
      ▼
Candidate Screening
      │
      ▼
Skill-Gap Analysis
      │
      ▼
Interview Question Generation
      │
      ▼
Candidate Data Management
      │
      ▼
Structured Recruitment Output
```

---

# 📁 Project Structure

```text
HireGenie/
│
├── assets/
│   ├── CV-English.pdf
│   ├── job_description.txt
│   └── candidate_data.csv
│
├── config/
│   └── agent configuration files
│
├── tools/
│   └── utility functions
│
├── app.py
├── .env-example
├── .gitignore
├── LICENSE
└── README.md
```

---

# ⚙️ Installation

## 1. Clone the repository

```bash
git clone https://github.com/priyankakumari0203/HireGenie-AI-Powered-Recruitment-Automation-Platform.git

cd HireGenie-AI-Powered-Recruitment-Automation-Platform
```

## 2. Create a virtual environment

```bash
python -m venv venv
```

### macOS / Linux

```bash
source venv/bin/activate
```

### Windows

```bash
venv\Scripts\activate
```

---

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

Install the required spaCy model:

```bash
python -m spacy download en_core_web_sm
```

---

# 🔑 Environment Configuration

Create a `.env` file:

```env
OPENAI_API_KEY=your_openai_api_key
```

Replace the value with your OpenAI API key.

> ⚠️ Never commit API keys, passwords, or other credentials to GitHub.

---

# ▶️ Running the Project

Place the candidate resume inside:

```text
assets/CV-English.pdf
```

Add the target job description:

```text
assets/job_description.txt
```

Then run:

```bash
python app.py
```

The system processes the recruitment workflow and generates the corresponding candidate analysis and interview information.

---

# 📊 Example Workflow

### Input

**Job Role:**

```text
Machine Learning Engineer
```

**Required Skills:**

```text
Python
Machine Learning
TensorFlow
PyTorch
SQL
MLOps
```

**Candidate Resume:**

```text
Python
Machine Learning
TensorFlow
SQL
Docker
```

### Processing

HireGenie analyzes:

```text
Required Skills
       │
       ▼
Candidate Skills
       │
       ▼
Matching Skills
       +
Skill Gaps
       │
       ▼
Interview Questions
```

### Output

The system can generate:

* Candidate information
* Screening analysis
* Matching skills
* Skill gaps
* Interview questions
* Structured candidate data

---

# 🚀 Future Enhancements

The current system can be extended into a complete AI-powered Applicant Tracking System.

### Planned / Potential Improvements

* 🌐 Recruiter web dashboard
* 🗄️ MongoDB / PostgreSQL database
* 📊 AI-based candidate scoring
* 🔎 Semantic resume-job matching
* 🧠 RAG-based candidate knowledge retrieval
* 🔗 GitHub profile analysis
* 📧 Automated candidate communication
* 📅 Interview scheduling
* 🔐 Recruiter authentication
* 📈 Recruitment analytics
* 🤖 Automated candidate shortlisting
* 🔄 Integration with ATS platforms
* 📑 Support for multiple resumes simultaneously

---

# 🎓 Academic & Technical Learning

This project provides practical experience in:

* **Data Science**
* **Artificial Intelligence**
* **Machine Learning**
* **Natural Language Processing**
* **Generative AI**
* **Large Language Models**
* **Multi-Agent Systems**
* **Prompt Engineering**
* **Document Processing**
* **AI Automation**
* **Python Development**

---

# 💡 Why This Project?

Recruitment involves a large amount of repetitive document analysis and candidate evaluation.

HireGenie explores how **AI agents can collaborate to automate these tasks**, reducing manual effort while producing structured information that recruiters can use during the hiring process.

The project combines concepts from **Data Science, NLP, Generative AI, and Agentic AI** into a practical recruitment use case.

---

# 👩‍💻 Developer

### Priyanka Kumari

**4th-Year Data Science Student**

Interested in:

```text
Data Science
     │
     ├── Artificial Intelligence
     ├── Machine Learning
     ├── NLP
     ├── Generative AI
     └── AI Agents
```

🔗 GitHub: [github.com/priyankakumari0203](https://github.com/priyankakumari0203)

---

# 📜 License

This project is licensed under the **MIT License**.

---

⭐ If you find this project useful, consider giving the repository a star!
