# 📄 ResumeParser - AI-Powered Resume Extraction Tool

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.3-green?logo=flask)
![NLTK](https://img.shields.io/badge/NLTK-3.8.1-orange)
![spaCy](https://img.shields.io/badge/spaCy-3.7-red)
![Render](https://img.shields.io/badge/Hosted%20on-Render-46B3E6?logo=render)
![MIT License](https://img.shields.io/badge/License-MIT-yellow)

A sophisticated resume parsing web application that automatically extracts and structures key information from resumes using advanced NLP techniques.

🌐 **Live Demo**: [https://resumeparser-9x3c.onrender.com](https://resumeparser-9x3c.onrender.com)

---

## ✨ Key Features

### 🔍 Smart Information Extraction
- **Personal Details**: Name, Email, Phone Number
- **Professional Summary**: Career objectives and key qualifications
- **Skills**: Technical and soft skills with proficiency detection
- **Experience**: Company names, job titles, durations, and responsibilities
- **Education**: Degrees, institutions, and graduation years
- **Certifications**: Professional certifications and licenses

---

## 🖥️ User Interface Preview

![Resume Management Dashboard](images/image.png)

*The dashboard allows you to:*
- Sort resumes by experience, education, or relevance
- Perform bulk actions on multiple resumes
- View all parsed information in a structured table
- Download or delete individual records

---

## 🚀 Tech Stack

### Frontend

| Technology      | Purpose      |
|-----------------|--------------|
| HTML5           | Structure    |
| CSS3/Bootstrap  | Styling      |
| Jinja2          | Templating   |

### Backend

| Technology      | Purpose             |
|-----------------|---------------------|
| Python 3.8+     | Core language        |
| Flask           | Web framework        |
| pdfminer.six    | PDF text extraction  |
| spaCy/NLTK      | NLP processing       |
| Regex           | Pattern matching     |

---

 
## Installation

To run this application locally:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Anwarsha7/resumeparser.git
Navigate to the project directory:

bash
Copy
Edit
cd resumeparser
Create virtual environment:

bash
Copy
Edit
python -m venv venv
Activate environment:

On Windows:

bash
Copy
Edit
venv\Scripts\activate
On macOS/Linux:

bash
Copy
Edit
source venv/bin/activate
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Download NLP models:

bash
Copy
Edit
python -m spacy download en_core_web_sm
python -m nltk.downloader punkt words
Run the application:

bash
Copy
Edit
python app.py
The application will be accessible at http://localhost:5000.

Deployment
This application is deployed using Render, a cloud application platform that simplifies the process of building, deploying, and scaling apps.

Contributing
We welcome contributions! Please follow these steps:

Fork the repository.

Create a new branch:

bash
Copy
Edit
git checkout -b feature-name
Make your changes.

Commit your changes:

bash
Copy
Edit
git commit -m 'Add feature'
Push to the branch:

bash
Copy
Edit
git push origin feature-name
Open a Pull Request.

License
This project is licensed under the MIT License. See the LICENSE file for details.

<div align="center"> <sub>Built with ❤️ by <a href="https://github.com/Anwarsha7">Anwar Sha</a></sub> </div> ```

📜 License
This project is licensed under the MIT License.
Copyright © 2023 Anwar Sha
