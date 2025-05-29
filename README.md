# 📄 ResumeParser - AI-Powered Resume Extraction Tool

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.3-green?logo=flask)
![NLTK](https://img.shields.io/badge/NLTK-3.8.1-orange)
![spaCy](https://img.shields.io/badge/spaCy-3.7-red)
![Render](https://img.shields.io/badge/Hosted%20on-Render-46B3E6?logo=render)
![MIT License](https://img.shields.io/badge/License-MIT-yellow)

A sophisticated resume parsing web application that automatically extracts and structures key information from resumes using advanced NLP techniques.

🌐 **Live Demo**: [https://resumeparser-9x3c.onrender.com](https://resumeparser-9x3c.onrender.com)

## ✨ Key Features

### 🔍 Smart Information Extraction
- **Personal Details**: Name, Email, Phone Number
- **Professional Summary**: Career objectives and key qualifications
- **Skills**: Technical and soft skills with proficiency detection
- **Experience**: Company names, job titles, durations, and responsibilities
- **Education**: Degrees, institutions, and graduation years
- **Certifications**: Professional certifications and licenses

## 🖥️ User Interface Preview

![Resume Management Dashboard](images/image.png)

*The dashboard allows you to:*
- Sort resumes by experience, education, or relevance
- Perform bulk actions on multiple resumes
- View all parsed information in a structured table
- Download or delete individual records

## 🚀 Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| HTML5 | Structure |
| CSS3/Bootstrap | Styling |
| Jinja2 | Templating |

### Backend
| Technology | Purpose |
|------------|---------|
| Python 3.8+ | Core language |
| Flask | Web framework |
| pdfminer.six | PDF text extraction |
| spaCy/NLTK | NLP processing |
| Regex | Pattern matching |

## 🏗️ Project Structure

```bash
.
├── app.py                  # Flask application entry point
├── requirements.txt        # Python dependencies
├── Procfile               # Render deployment configuration
├── .env                   # Environment variables
├── .gitignore             # Git exclusion rules
├── resume_parser.log      # Application logs
├── res/                   # Core parsing modules
│   ├── ress.py            # Main parsing logic
│   └── resu.py            # Utility functions
├── static/                # Static assets
│   ├── css/               # Stylesheets
│   └── js/                # JavaScript files
└── templates/             # HTML templates
    ├── index.html         # Main interface
    └── results.html       # Parsing results display
