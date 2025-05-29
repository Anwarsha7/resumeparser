 # 📄 ResumeParser - AI-Powered Resume Extraction Tool

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.3-green?logo=flask)
![NLTK](https://img.shields.io/badge/NLTK-3.8.1-orange)
![spaCy](https://img.shields.io/badge/spaCy-3.7-red)
![Render](https://img.shields.io/badge/Hosted%20on-Render-46B3E6?logo=render)
![MIT License](https://img.shields.io/badge/License-MIT-yellow)

A sophisticated resume parsing web application that automatically extracts and structures key information from resumes using advanced NLP techniques. Effortlessly transform unstructured resume data into actionable insights!

🌐 **Live Demo**: [https://resumeparser-9x3c.onrender.com](https://resumeparser-9x3c.onrender.com)

---

## 📝 Table of Contents

- [About The Project](#-about-the-project)
- [✨ Key Features](#-key-features)
- [⚙️ How It Works](#️-how-it-works)
- [🖥️ User Interface Preview](#️-user-interface-preview)
- [🚀 Tech Stack](#-tech-stack)
- [🛠️ Installation](#️-installation)
- [▶️ Usage](#️-usage)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [📧 Contact](#-contact)

---

## 🎯 About The Project

ResumeParser streamlines the hiring process by automating the tedious task of sifting through resumes. By leveraging Natural Language Processing (NLP), this tool intelligently extracts crucial information from PDF resumes, presenting it in a structured and easily manageable format. This allows recruiters and hiring managers to quickly identify candidate qualifications and make informed decisions.

---

## ✨ Key Features

### 🔍 Smart Information Extraction
-   👤 **Personal Details**: Name, Email, Phone Number, LinkedIn Profile (if available)
-   📝 **Professional Summary**: Career objectives and key qualifications
-   🛠️ **Skills**: Technical and soft skills, with proficiency detection (e.g., "Expert in Python")
-   🏢 **Experience**: Company names, job titles, employment durations, and key responsibilities/achievements
-   🎓 **Education**: Degrees, institutions, fields of study, and graduation years
-   📜 **Certifications**: Professional certifications and licenses

### Other Notable Features:
-   📄 **PDF Support**: Handles resumes in PDF format.
-   📊 **Structured Output**: Presents parsed data in an organized table.
-   🚀 **User-Friendly Interface**: Simple and intuitive web interface for easy uploads and viewing.
-   ☁️ **Cloud Hosted**: Accessible anywhere via the Render deployment.

---

## ⚙️ How It Works

The application follows a streamlined process to extract information:

1.  **📄 Resume Upload**: Users upload resumes in PDF format through the web interface.
2.  **⛏️ Text Extraction**: `pdfminer.six` is used to accurately extract raw text content from the PDF files.
3.  **🧠 NLP Processing**:
    *   **spaCy**: Utilized for Named Entity Recognition (NER) to identify entities like names, organizations, dates, and locations. It also helps with sentence segmentation and tokenization.
    *   **NLTK**: Employed for tasks like part-of-speech (POS) tagging, and accessing lexical resources (e.g., `punkt` for tokenization, `words` for vocabulary checks).
    *   **Custom Regex**: Regular expressions are used to identify specific patterns like email addresses, phone numbers, and other structured data points that might be missed or need refinement.
4.  **🏗️ Data Structuring**: The extracted information is categorized and organized into predefined fields (Name, Email, Skills, Experience, etc.).
5.  **💻 Display**: The structured data is then presented to the user in a clear, tabular format on the web application's dashboard.

---

## 🖥️ User Interface Preview

![Resume Management Dashboard](images/image.png)

*The dashboard allows you to:*
- Upload new resumes for parsing.
- View all parsed information in a structured table.
- Sort resumes by experience, education, or relevance (future enhancement idea!).
- Perform bulk actions on multiple resumes (future enhancement idea!).
- Download or delete individual records.


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

5.  **Download NLP models:**
    ```bash
    python -m spacy download en_core_web_sm
    python -m nltk.downloader punkt words stopwords
    ```
    *(Added `stopwords` as it's commonly used with NLTK for text processing)*

6.  **Run the application:**
    ```bash
    python app.py
    ```

The application will be accessible at: `http://localhost:5000`

---

## ▶️ Usage

Once the application is running locally:

1.  Open your web browser and navigate to `http://localhost:5000`.
2.  You will see the main page with an option to upload a resume.
3.  Click on "Choose File", select a PDF resume from your local machine, and click "Upload".
4.  The application will process the resume and display the extracted information in a structured format on the dashboard.
5.  You can then view the details or upload another resume.

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

Distributed under the MIT License. See `LICENSE` file for more information.
 

---

## 📧 Contact

Anwarsha K - [@Anwarsha7](https://github.com/Anwarsha7) - ynetfli894@gmail.com  

Project Link: [https://github.com/Anwarsha7/resumeparser](https://github.com/Anwarsha7/resumeparser)
