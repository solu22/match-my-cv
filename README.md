# match-my-cv

✨ Features

Upload CV in Excel format

Extract skills from the Skills section

Compare against multiple job descriptions

Identify:

Matching strengths

Missing skills (gaps)

Improvement suggestions

Clean JSON output for automation and analysis

Uses Google Gemini API

🛠️ Tech Stack

Python

Google Colab

Pandas

Gemini LLM (via google.genai)

JSON & Regex

🚀 How to Run in Google Colab
1️⃣ Open Google Colab

Go to: https://colab.research.google.com

Create a New Notebook.

2️⃣ Install Required Libraries

Run this in a Colab cell:

!pip install pandas openpyxl google-generativeai

3️⃣ Add Your Gemini API Key

In Colab:

Click on 🔒 Secrets (left sidebar)

Add a new secret:

Name: GEMINI_API_KEY

Value: your API key

Your code will automatically load it using:

from google.colab import userdata
API_KEY = userdata.get("GEMINI_API_KEY")

4️⃣ Upload Your CV File

Your CV must be in Excel format (.xlsx) and contain:

A column named Section

A column named Details

A row where Section = "Skills"

Example:

Section	Details
Skills	Python, Machine Learning, Data Analysis

Upload the file when prompted:

from google.colab import files
uploaded = files.upload()

5️⃣ Run the Script

Execute the notebook cells. The program will:

Read the uploaded Excel file

Extract skills from the Skills section

Compare them against predefined job descriptions

Output:

Candidate skills

Strengths per job

Weaknesses (missing skills)

Suggestions

📤 Output Example
Candidate Skills: ['Python', 'Machine Learning', 'Pandas']

Job ID: desc1
Strengths: Python, Machine Learning
Weaknesses: patent analysis, NLP, AI frameworks
Suggestions: Learn NLP for document analysis, explore patent analytics tools

📁 Expected File Format

Your Excel CV must include:

Column: Section

Column: Details

A row with Section = Skills

If the "Skills" row is missing, the script will stop with an error.

🔒 Notes on Data Privacy

Your CV is processed only within your Colab session.

No files are stored after the session ends.

API calls are made securely using your own Gemini API key.

📌 Future Improvements

Add UI / Web interface

Support PDF and DOCX CVs

Scoring system for job fit

Batch processing of multiple CVs

Visualization of skill gaps

📄 License

This project is open-source. You may use, modify, and distribute it with attribution.

🤝 Contributing

Pull requests and suggestions are welcome!
If you find bugs or want to extend functionality, feel free to open an issue.
