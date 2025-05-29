# 📄 ResumeParser - AI-Powered Resume Extraction & Management Tool

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.3-green?logo=flask)
![NLTK](https://img.shields.io/badge/NLTK-3.8.1-orange)
![spaCy](https://img.shields.io/badge/spaCy-3.7-red)
![Render](https://img.shields.io/badge/Hosted%20on-Render-46B3E6?logo=render)
![MIT License](https://img.shields.io/badge/License-MIT-yellow)

A sophisticated resume parsing web application designed for both **Candidates** and **Recruiters**. Candidates can easily upload their resumes, while Recruiters can manage, download, parse, and analyze these resumes using advanced NLP techniques to extract and structure key information. Effortlessly transform unstructured resume data into actionable insights!

🌐 **Live Demo**: [https://resumeparser-9x3c.onrender.com](https://resumeparser-9x3c.onrender.com)

---

## 📝 Table of Contents

- [About The Project](#-about-the-project)
- [👥 User Roles & Workflow](#-user-roles--workflow)
  - [For Candidates](#-for-candidates)
  - [For Recruiters](#-for-recruiters)
- [✨ Key Features](#-key-features)
- [⚙️ Core Parsing Engine - How It Works](#️-core-parsing-engine---how-it-works)
- [🖥️ User Interface Preview](#️-user-interface-preview)
- [🚀 Tech Stack](#-tech-stack)
- [🛠️ Installation](#️-installation)
- [▶️ Usage Instructions](#️-usage-instructions)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [📧 Contact](#-contact)

---

## 🎯 About The Project

ResumeParser streamlines the hiring process by providing a dedicated platform for candidates to submit their resumes and for recruiters to efficiently process them. By leveraging Natural Language Processing (NLP), this tool intelligently extracts crucial information from PDF resumes, presenting it in a structured and easily manageable format. This allows recruiters to quickly identify candidate qualifications and make informed decisions, while providing a simple submission portal for candidates.

---

## 👥 User Roles & Workflow

ResumeParser offers distinct functionalities tailored to two primary user roles:

### 👤 For Candidates
1.  **Register/Login**: Candidates create an account or log in securely.
2.  **Resume Upload**: Upon logging in, candidates are directed to a page where they can easily upload their resume (PDF format).
3.  **Submission Confirmation**: Candidates receive confirmation of their resume submission.

### 👨‍💼 For Recruiters
1.  **Register/Login**: Recruiters create an account or log in securely to access the admin dashboard.
2.  **Admin Dashboard**: Recruiters land on a dashboard where they can view and manage resumes.
3.  **Download Resumes**: Recruiters can download all resumes uploaded by candidates.
4.  **Navigate to Parser**: After downloading, recruiters can navigate to the parsing section of the application.
5.  **Parse Resumes**: Recruiters upload the downloaded (or any other) PDF resumes one by one into the parsing engine.
6.  **View & Analyze Parsed Data**: The system extracts key information (personal details, skills, experience, education).
7.  **Sort & Filter**: Recruiters can sort the parsed resume data based on various criteria (e.g., experience, education) to efficiently find suitable candidates.

---

## ✨ Key Features

### For All Users:
-   🔐 **Secure Authentication**: Separate registration and login for candidates and recruiters.

### For Candidates:
-   ⬆️ **Simple Resume Upload**: Dedicated interface for easy PDF resume submission.

### For Recruiters:
-   📊 **Admin Dashboard**: Centralized view for managing candidate resumes.
-   📥 **Bulk Resume Access**: Ability to download all submitted candidate resumes.
-   🔍 **Smart Information Extraction (via Parsing Engine)**:
    -   **Personal Details**: Name, Email, Phone Number, LinkedIn Profile (if available).
    -   **Professional Summary**: Career objectives and key qualifications.
    -   **Skills**: Technical and soft skills.
    -   **Experience**: Company names, job titles, durations, and key responsibilities.
    -   **Education**: Degrees, institutions, and graduation years.
    -   **Certifications**: Professional certifications and licenses.
-   📋 **Structured Data Output**: Parsed information presented in an organized, tabular format.
-   ⚙️ **Advanced Sorting**: Ability to sort parsed resumes based on extracted criteria.
-   📄 **PDF Support**: Handles resumes in PDF format for parsing.
-   ☁️ **Cloud Hosted**: Accessible anywhere via the Render deployment.

---

## ⚙️ Core Parsing Engine - How It Works

The resume parsing functionality used by recruiters involves the following steps:

1.  **📄 Resume Upload (by Recruiter for Parsing)**: Recruiters upload individual PDF resumes (typically those downloaded from the candidate pool) into the parsing interface.
2.  **⛏️ Text Extraction**: `pdfminer.six` is used to accurately extract raw text content from the PDF files.
3.  **🧠 NLP Processing**:
    *   **spaCy**: Utilized for Named Entity Recognition (NER) to identify entities like names, organizations, dates, and locations. It also helps with sentence segmentation and tokenization.
    *   **NLTK**: Employed for tasks like part-of-speech (POS) tagging, and accessing lexical resources (e.g., `punkt` for tokenization, `words` for vocabulary checks, `stopwords` for noise reduction).
    *   **Custom Regex**: Regular expressions are used to identify specific patterns like email addresses, phone numbers, and other structured data points.
4.  **🏗️ Data Structuring**: The extracted information is categorized and organized into predefined fields.
5.  **💻 Display & Sorting**: The structured data is then presented to the recruiter in a clear, sortable table.

---

## 🖥️ User Interface Preview

*   **Candidate View**: Candidates are presented with a straightforward login/registration page, leading to a dedicated resume upload interface.
*   **Recruiter Admin Dashboard**: Recruiters have access to a dashboard to view and download candidate resumes.
*   **Recruiter Parsing View & Results**: After navigating to the parsing section, recruiters can upload resumes for extraction. The parsed data is displayed in a structured table, similar to the image below, allowing for sorting and analysis.

![Resume Management Dashboard for Parsed Data](images/image.png)
*(This image primarily showcases the recruiter's view after parsing a resume, where data is structured and sortable.)*


---

 

## 🚀 Tech Stack

### Frontend

| Technology      | Purpose         |
|-----------------|-----------------|
| HTML5           | Structure       |
| CSS3/Bootstrap  | Styling         |
| Jinja2          | Templating      |

### Backend

| Technology      | Purpose                |
|-----------------|------------------------|
| Python 3.8+     | Core language           |
| Flask           | Web framework, Routing |
| **MongoDB Atlas** | Cloud Database Service |
| **Pymongo**     | MongoDB Python Driver  |
| pdfminer.six    | PDF text extraction     |
| spaCy/NLTK      | NLP processing          |
| Regex           | Pattern matching        |
| Werkzeug        | User Authentication (if used directly) |

*(Note: Pymongo is the standard Python driver for MongoDB. Please ensure it's in your `requirements.txt` if you're using MongoDB Atlas from Python.)*

### Deployment
| Service         | Purpose             |
|-----------------|---------------------|
| Render          | Cloud Hosting       |

---

## 🛠️ Installation

To run this application locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Anwarsha7/resumeparser.git
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd resumeparser
    ```

3.  **Create and activate a virtual environment:**
    *   Create:
        ```bash
        python -m venv venv
        ```
    *   Activate (choose based on your OS):
        *   **On Windows:**
            ```bash
            venv\Scripts\activate
            ```
        *   **On macOS/Linux:**
            ```bash
            source venv/bin/activate
            ```

4.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Ensure your `requirements.txt` includes `pymongo` and all other necessary packages).*

5.  **Configure Environment Variables (MongoDB Atlas Connection):**
    This application requires a connection string to your MongoDB Atlas cluster. It's best practice to store this in an environment variable.
    *   Create a `.env` file in the root of your project (ensure `.env` is listed in your `.gitignore` file to avoid committing credentials).
    *   Add your MongoDB Atlas connection string to the `.env` file, for example:
        ```env
        MONGODB_URI="mongodb+srv://<username>:<password>@<cluster-url>/<database-name>?retryWrites=true&w=majority"
        ```
    *   Replace `<username>`, `<password>`, `<cluster-url>`, and `<database-name>` with your actual credentials and database details.
    *   Your application code (e.g., in `app.py`) should be configured to read this environment variable (e.g., using `os.getenv('MONGODB_URI')` or a library like `python-dotenv`).

6.  **Download NLP models:**
    ```bash
    python -m spacy download en_core_web_sm
    python -m nltk.downloader punkt words stopwords
    ```

7.  **Run the application:**
    ```bash
    python app.py
    ```

The application will be accessible at: `http://localhost:5000`

 
---

## ▶️ Usage Instructions

Once the application is running locally or accessed via the live demo link:

### For Candidates:
1.  Navigate to `http://localhost:5000` (or the live demo link).
2.  Register for a new candidate account or log in if you already have one.
3.  You will be directed to the resume upload page.
4.  Click "Choose File", select your PDF resume, and click "Upload".

### For Recruiters:
1.  Navigate to `http://localhost:5000` (or the live demo link).
2.  Register for a new recruiter account or log in.
3.  You will be directed to the admin dashboard where you can see candidate resumes.
4.  Download the resumes you wish to process.
5.  Navigate to the "Resume Parser" section/page (the main index page as you described).
6.  Upload a downloaded (or any other) PDF resume for parsing.
7.  View the extracted information.
8.  Utilize the sorting features to analyze and compare candidate data.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1.  Fork the Project (`https://github.com/Anwarsha7/resumeparser/fork`)
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License.

See the [LICENSE](LICENSE) file for full license rights and limitations.
You can also find more information about the MIT License at [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT).

---

## 📧 Contact

Anwarsha K - [@Anwarsha7](https://github.com/Anwarsha7) - ynetflix894@gmail.com

Project Link: [https://github.com/Anwarsha7/resumeparser](https://github.com/Anwarsha7/resumeparser)
