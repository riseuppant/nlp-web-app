# NLP Web App

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/riseuppant/nlp-web-app?style=for-the-badge)](https://github.com/riseuppant/nlp-web-app/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/riseuppant/nlp-web-app?style=for-the-badge)](https://github.com/riseuppant/nlp-web-app/network)
[![GitHub issues](https://img.shields.io/github/issues/riseuppant/nlp-web-app?style=for-the-badge)](https://github.com/riseuppant/nlp-web-app/issues)

**A Flask-based web application that performs Natural Language Processing tasks and stores interaction history.**

</div>

---

## Overview

This project is a simple web application built with **Flask** that allows users to perform Natural Language Processing (NLP) tasks through a web interface.

Users can submit text, process it using NLP functions such as **sentiment analysis or summarization**, and view the results directly in the browser. All interactions are stored in a **SQLite database**, allowing users to review their analysis history.

The application also provides **REST API endpoints** for programmatic access to its NLP features.

---

## Features

* Simple web interface for submitting text
* NLP processing through API endpoints
* Sentiment analysis and text summarization
* History of processed inputs and outputs
* SQLite database for lightweight storage
* Modular Flask project structure

---

## Tech Stack

### Backend

* Python
* Flask

### NLP

* Python NLP libraries (e.g., spaCy, NLTK, Transformers)

### Database

* SQLite

### Frontend

* HTML
* CSS
* Jinja2 Templates

---

## Installation

### Prerequisites

* Python 3.8+
* pip

### 1. Clone the repository

```bash
git clone https://github.com/riseuppant/nlp-web-app.git
cd nlp-web-app
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install flask
```

Install additional NLP libraries if used:

```bash
pip install spacy nltk transformers
```

### 4. Run the application

```bash
python app.py
```

Open your browser and visit:

```
http://localhost:5000
```

---

## Project Structure

```
nlp-web-app/
│
├── app.py
├── api.py
├── db.py
├── README.md
├── .gitignore
│
└── templates/
    ├── index.html
    ├── results.html
    └── history.html
```

**app.py** – Main Flask application
**api.py** – NLP API endpoints
**db.py** – SQLite database logic
**templates/** – HTML templates for the web interface

---

## API Endpoints

### Sentiment Analysis

`POST /api/sentiment`

Request:

```json
{
  "text": "This movie was amazing."
}
```

Response:

```json
{
  "text": "This movie was amazing.",
  "sentiment": "positive",
  "score": 0.92
}
```

---

### Text Summarization

`POST /api/summarize`

Request:

```json
{
  "text": "Long text to summarize..."
}
```

Response:

```json
{
  "original_text": "Long text to summarize...",
  "summary": "Short summarized version."
}
```

---

## Deployment

For production, run the application using a WSGI server such as **Gunicorn**.

Install Gunicorn:

```bash
pip install gunicorn
```

Run the server:

```bash
gunicorn -w 4 'app:app'
```

---

## Contributing

Contributions are welcome.
Please open an issue before submitting major changes.

---

## License

This project currently does not include a license file.

---

<div align="center">

⭐ Star this repository if you find it useful.

Made with ❤️ by riseuppant

</div>
