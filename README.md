
#  XcelerateIT AI/ML Hiring Test – Resume Matcher

Welcome to the AI/ML Developer technical evaluation for XcelerateIT.

This assignment simulates a real-world mini-project and evaluates your ability to build a practical ML or LLM-powered solution.

---

##  Objective

Design a simple **Resume Matcher** engine that can:

- Accept a resume file (PDF, DOCX, or TXT)
- Extract meaningful skills and keywords
- Match the candidate's profile against a dataset of job descriptions
- Return the **Top 3 matching jobs** with:
  - A match score
  - A brief explanation (matched keywords/phrases)

---

##  Key Features to Implement

### 1. Resume Input

- Upload support: `.pdf`, `.docx`, `.txt`
- Parse and clean the text
- Extract skills, tools, and keywords

### 2. Job Dataset

- Use a local dataset (`.csv` or `.json`) of **minimum 5 job descriptions**
- Each job entry should have:
  - `job_id`
  - `title`
  - `description`

**Example (`jobs.csv`):**
```csv
job_id,title,description
1,Java Developer,"Spring Boot, REST APIs, SQL, Microservices"
2,ML Engineer,"Python, Scikit-learn, NLP, Classification"
3,Frontend Dev,"React, JavaScript, APIs, UI/UX"
````

### 3. Matching Logic

* Match resume content with job descriptions using:

  * Keyword overlap
  * TF-IDF + Cosine similarity
  * (Optional) LLM-based embeddings for semantic matching

### 4. Output

Return the **top 3 job matches** with:

* Job Title & ID
* Match Score (0–100)
* Reason (e.g., "Matched: Python, NLP, Scikit-learn")

---

##  Recommended Tech Stack

* **Language:** Python 3.x
* **NLP Libraries:** spaCy / NLTK / Scikit-learn
* **Optional Enhancements:**

  * HuggingFace Transformers
  * Sentence Transformers
  * LangChain
* **Backend (for API):** Flask or FastAPI
* **Frontend UI (optional):** Streamlit or Gradio

---

##  Setup Instructions

1. **Clone the repo**

   ```bash
   git clone https://github.com/your-username/resume-matcher-ai-test.git
   cd resume-matcher-ai-test
   ```

2. **Create virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the app (example using Streamlit or Flask)**

   ```bash
   streamlit run app.py
   # OR
   python app.py
   ```

---

##  Example Input & Output

### Input: `resume.pdf`

**Extracted Skills:**

```
Python, NLP, Scikit-learn, Transformers
```

### Output (JSON):

```json
[
  {
    "job_id": 2,
    "title": "ML Engineer",
    "score": 92.5,
    "reason": "Matched: Python, NLP, Scikit-learn"
  },
  {
    "job_id": 1,
    "title": "Java Developer",
    "score": 45.2,
    "reason": "Matched: SQL"
  },
  {
    "job_id": 3,
    "title": "Frontend Dev",
    "score": 25.1,
    "reason": "Matched: APIs"
  }
]
```

---

##  Submission Instructions

* **Fork this repo** to your GitHub account
* Complete and commit your code with clear commit messages
* Ensure your `README.md` includes:

  * Setup instructions
  * Tech stack and method used
  * Input/output example
  * (Optional) Link to deployed demo

 Submit your repo link via the following form:
**[Google Form →](https://forms.gle/your-form-link-here)**

---

##  Evaluation Criteria

| Area             | What We’re Looking For                        |
| ---------------- | --------------------------------------------- |
| Skill Extraction | Can extract meaningful data from resumes      |
| Matching Logic   | Effective comparison between resumes and jobs |
| AI Reasoning     | Proper model/method choice and justification  |
| Code Quality     | Modular, readable, and well-commented code    |
| Bonus            | LLM-based matcher, demo UI, extra test cases  |

---

##  Time Expectation

* Estimated time: **1-2 days**
* Submit earlier if you're done!

---

##  FAQs

**Q: Can I use ChatGPT or HuggingFace models?**
Yes — as long as you can clearly explain your logic and decisions.

**Q: Is it mandatory to use LLMs?**
No — TF-IDF, rule-based, or classic NLP methods are equally acceptable.

**Q: Will I present my solution?**
Yes — you may be asked to explain your code in a short walkthrough.

**Q: Will my code be reused?**
No — this project is for internal hiring evaluation only.

---

##  Good Luck!

— **Team XcelerateIT**
 [https://xcelerateit.ai](https://xcelerateit.ai)

```
