# 🧠 AI CV–Job Matcher

An AI-powered tool that analyzes a candidate’s CV and compares their listed skills against multiple job descriptions using a large language model (Gemini). The system outputs structured insights including strengths, gaps, and improvement suggestions.

This project is designed to run in **Google Colab**, so no local setup is required.

---

## 🚀 Run in Google Colab

Click below to open the notebook directly in Colab:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/REPO_NAME/blob/main/NOTEBOOK_NAME.ipynb)

---

## ✨ Features

- Upload CV in **Excel (.xlsx)** format  
- Extracts skills from the *Skills* section  
- Matches against multiple job descriptions  
- Identifies:
  - Strengths (matching skills)
  - Weaknesses (missing skills)
  - Suggestions (how to improve fit)
- Structured **JSON output**
- Secure API key handling using Colab secrets

---

## 🛠️ Tech Stack

- Python  
- Google Colab  
- Pandas  
- Gemini LLM (`google.genai`)  
- JSON, Regex  

---

## 📂 Expected CV Format

Your Excel file must include:

| Column  | Description |
|--------|-------------|
| Section | CV section name (e.g., Skills, Education) |
| Details | Content for that section |

There must be a row where:

```text
Section = Skills
