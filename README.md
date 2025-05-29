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
    python -m nltk.downloader punkt words
    ```

6.  **Run the application:**
    ```bash
    python app.py
    ```

The application will be accessible at: `http://localhost:5000`

---
### Option 2: As a single executable script (`setup.sh`)

This is a more automated approach. You'd tell users to download this script and run it.

**1. Create a file named `setup.sh` in the root of your repository:**

```bash
#!/bin/bash
set -e # Exit immediately if a command exits with a non-zero status.

REPO_URL="https://github.com/Anwarsha7/resumeparser.git"
PROJECT_DIR="resumeparser"

echo "--- Starting local application setup ---"

# 1. Clone the repository (if not already cloned)
if [ -d "$PROJECT_DIR" ]; then
    echo "Directory '$PROJECT_DIR' already exists. Skipping clone."
else
    echo "Cloning the repository..."
    git clone "$REPO_URL"
fi

# 2. Navigate to the project directory
echo "Navigating to the project directory..."
cd "$PROJECT_DIR"

# 3. Create virtual environment
echo "Creating virtual environment..."
python -m venv venv

# 4. Activate environment
echo "Activating virtual environment..."
# Check OS for activation command
if [[ "$OSTYPE" == "linux-gnu"* || "$OSTYPE" == "darwin"* ]]; then
    # Linux or macOS
    source venv/bin/activate
elif [[ "$OSTYPE" == "msys" || "$OSTYPE" == "cygwin" || "$OSTYPE" == "win32" ]]; then
    # Git Bash on Windows, MSYS2, or WSL
    source venv/Scripts/activate
else
    echo "Warning: Unrecognized OS type '$OSTYPE'. Attempting macOS/Linux activation."
    source venv/bin/activate || { echo "Failed to activate venv. Please activate manually or report an issue."; exit 1; }
fi

# 5. Install dependencies
echo "Installing Python dependencies..."
pip install -r requirements.txt

# 6. Download NLP models
echo "Downloading NLP models (spaCy and NLTK)..."
python -m spacy download en_core_web_sm
python -m nltk.downloader punkt words

echo "--- Local setup complete! ---"
echo ""
echo "To run the application, ensure your virtual environment is active and run:"
echo "  python app.py"
echo ""
echo "The application will be accessible at: http://localhost:5000"
echo "To deactivate the environment when done: deactivate"
