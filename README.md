# AI Clinical Trial Matcher
 
> Built during IBM Internship 2025 · Gemini 1.5 Pro · Django · 93.57% Classification Accuracy
 
An intelligent web application that takes a patient's plain-text medical description, classifies their condition using the Gemini 1.5 Pro API, and matches them against a dataset of **370,000+ clinical trials** — returning the most relevant results in seconds.
 
---
 
## What it does
 
Patients and clinicians often struggle to find relevant clinical trials manually. This system automates that process end-to-end:
 
1. The user describes their condition in plain text
2. Gemini 1.5 Pro classifies it into one or more of **14 medical categories** (cardiac, pulmonary, neurological, etc.)
3. A backend matching engine filters 370,000+ trials based on those categories
4. Results are displayed in a clean table with an option to **download the top 50 matches as CSV**
---
 
## Performance
 
Evaluated on a dataset of 140 test cases:
 
| Metric | Result |
|---|---|
| Gemini Classification Accuracy | **93.57%** |
| Retrieval Relevance (Jaccard Index) | **0.41** |
 
---
 
## Tech Stack
 
| Layer | Technology |
|---|---|
| Backend | Python, Django |
| AI / Classification | Google Gemini 1.5 Pro API |
| Data Processing | Pandas |
| Database | SQLite3 |
| Frontend | HTML, CSS, JavaScript |
 
---
 
## Features
 
- **Condition Classification** — Gemini 1.5 Pro maps free-text patient descriptions to medical categories
- **Trial Matching Engine** — Pandas-based filtering across 370,000+ trials
- **User Authentication** — Registration, login, and password reset flow
- **CSV Export** — Download top 50 matched trials for offline use
- **Responsive UI** — Dark-themed, mobile-friendly interface
---
 
## Setup & Installation
 
Requires Python 3.12 and Django 5.2.4.
 
```bash
# Clone the repository
git clone https://github.com/Er0ze-Barua/AI-Clinical-Trial-Matcher.git
cd AI-Clinical-Trial-Matcher
 
# Create and activate virtual environment
python -m venv venv
.\venv\Scripts\activate        # Windows
source venv/bin/activate       # macOS / Linux
 
# Install dependencies
pip install -r requirement.txt
 
# Set up the database
python manage.py makemigrations
python manage.py migrate
 
# Create a superuser (optional)
python manage.py createsuperuser
 
# Run the development server
python manage.py runserver
```
 
> **Note:** You will need a valid Google Gemini API key. Add it to your environment or the appropriate config file before running.
 
---
 
## Project Context
 
This project was developed as part of an **IBM internship (2025)**, with the goal of reducing the time and effort required for clinical trial discovery using AI-assisted classification.
