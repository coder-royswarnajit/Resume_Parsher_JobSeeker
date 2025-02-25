# Resume Matcher - Job Recommendation System

## Overview
This is a Flask-based web application that allows users to upload their resumes, extract skills, and find matching job opportunities from a predefined dataset. Additionally, it features a chatbot that provides assistance with common queries.

## Features
- Upload resumes in **TXT, PDF, or DOCX** format.
- Extract skills from resumes.
- Match extracted skills with job postings from a CSV file.
- Display relevant job opportunities.
- Chatbot for answering user queries.

## Technologies Used
- **Python** (Flask, Pandas, NLTK, PyPDF2, python-docx)
- **HTML/CSS** (for rendering templates)
- **CSV** (for job listings storage)

## Installation & Setup
### Prerequisites
Ensure you have **Python 3.x** installed on your system.

### Steps to Run
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/resume-matcher.git
   cd resume-matcher
   ```

2. Install the required dependencies:
   ```sh
   pip install flask pandas nltk PyPDF2 python-docx
   ```

3. Download NLTK resources:
   ```sh
   python -c "import nltk; nltk.download('punkt')"
   ```

4. Ensure you have a `jobs.csv` file in the project directory. The file should contain job listings with a **'skills_desc'** column describing required skills.

5. Run the Flask app:
   ```sh
   python app.py
   ```

6. Open a browser and go to:
   ```
   http://127.0.0.1:5000/
   ```

## File Structure
```
resume-matcher/
│── app.py               # Main Flask application
│── templates/
│   ├── index.html       # Home page for file upload
│   ├── results.html     # Display matching jobs
│── jobs.csv             # Job listings database
│── README.md            # Project documentation
```

## API Endpoints
### 1. Home Page (Upload Resume)
- **Endpoint:** `/`
- **Method:** `GET, POST`
- **Description:** Allows users to upload their resumes, extract skills, and view job matches.

### 2. Chatbot API
- **Endpoint:** `/chatbot`
- **Method:** `POST`
- **Request Body:** `{ "message": "hello" }`
- **Response:** `{ "response": "Hi there! How can I assist you today?" }`

## Future Enhancements
- Expand chatbot capabilities using NLP.
- Improve job-matching algorithm.
- Enhance frontend design with Bootstrap or TailwindCSS.

## License
This project is open-source and available under the **MIT License**.

