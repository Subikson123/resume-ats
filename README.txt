# 🧠 ResumeRanker – Smart ATS Resume Score Analyzer

**ResumeRanker** is a lightweight, AI-powered web app designed to help job seekers evaluate how well their resume aligns with a specific job description. By using deep language understanding through sentence embeddings, ResumeRanker offers a smart and accurate similarity score—giving users insight into how their resume might perform in an Applicant Tracking System (ATS).

---

## 🔍 Project Motivation

In today’s competitive job market, resumes are often screened by automated systems before reaching a human recruiter. These Applicant Tracking Systems (ATS) filter resumes based on keyword matching and semantic relevance to the job posting.

**ResumeRanker** aims to simulate this process by analyzing:
- How closely your resume matches a job description
- Semantic keyword alignment using advanced NLP models
- Opportunities for improvement before applying

---

## 🚀 Features

✅ Upload your resume in **PDF format**  
✅ Paste the job description manually  
✅ Calculate an **ATS match score** using **Sentence-BERT embeddings**  
✅ Real-time feedback on match percentage  
✅ User-friendly web interface powered by Flask  
✅ Secure upload and parsing with text extraction from PDF

---

## 🎯 Use Cases

- ✅ **Job Seekers**: Optimize your resume before applying
- ✅ **Career Coaches**: Provide clients with quantitative resume feedback
- ✅ **Universities & Career Services**: Automate resume evaluation in workshops
- ✅ **Recruiters**: Quickly compare applicant resumes to job descriptions

---

## 🧠 How It Works

1. **Upload Resume** – Users upload their resume in PDF format.
2. **Paste Job Description** – Paste the job listing or description into the textbox.
3. **Text Extraction** – The app extracts text from the resume PDF using PyMuPDF.
4. **Semantic Embeddings** – Both resume text and job description are encoded using `SentenceTransformer` with the `all-MiniLM-L6-v2` model.
5. **Similarity Score** – The system computes **cosine similarity** between the two vectors and returns a percentage match.
6. **Display Result** – The match score is shown on the web page for quick feedback.

---

## 🛠️ Tech Stack

| Component         | Tech / Library                     |
|------------------|------------------------------------|
| Framework        | Flask                              |
| Language         | Python                             |
| NLP Model        | SentenceTransformers (MiniLM-L6-v2)|
| Resume Parsing   | PyMuPDF (`fitz`)                   |
| Similarity       | Cosine Similarity (sklearn)        |
| Frontend         | HTML with Jinja2 (via Flask)       |

---

## 📦 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/ResumeRanker.git
cd ResumeRanker
2. Create a Virtual Environment (Optional)
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4. Run the Flask App
bash
Copy
Edit
python app.py
5. Open in Browser
Visit http://127.0.0.1:5000

📝 Example
Resume Content: "Python Developer with 3+ years of experience in backend systems..."

Job Description: "Looking for a backend Python developer with experience in APIs and databases..."

Score Output: 87.65% Match ✅

🔧 Planned Enhancements
🔄 DOCX resume support

📊 Detailed skill/keyword breakdown

📝 Resume improvement suggestions

🖨️ PDF report generation with feedback

🎨 Enhanced UI/UX with Bootstrap or Streamlit version

📁 File Structure
bash
Copy
Edit
ResumeRanker/
├── app.py                  # Flask server logic
├── templates/
│   └── index.html          # Web interface
├── uploads/                # Directory for storing resumes
├── requirements.txt        # Dependencies
└── README.md               # Project description
📄 License
This project is licensed under the MIT License. Feel free to fork, use, and modify!

🙌 Acknowledgments
HuggingFace SentenceTransformers

PyMuPDF

Scikit-learn

