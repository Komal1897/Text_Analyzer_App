# Text Summarizer App

A web-based Text Summarization application built using **Python, FastAPI, and Hugging Face Transformers**. The application uses a fine-tuned T5 model to generate concise summaries from long text inputs.

## Features

- Summarizes long text into concise, meaningful content.
- Uses a T5 Transformer model for text summarization.
- Provides a web interface for entering text and viewing summaries.
- Displays a character counter for the input text.
- Includes Clear and Copy Summary buttons.
- Exposes a REST API endpoint for summarization.
- Supports CPU and compatible GPU acceleration.

## Tech Stack

- **Language:** Python
- **Backend:** FastAPI
- **AI Model:** T5 (Text-to-Text Transfer Transformer)
- **NLP Framework:** Hugging Face Transformers
- **Deep Learning:** PyTorch
- **Frontend:** HTML, CSS, JavaScript
- **Templating:** Jinja2

## Project Structure

```text
Text_Analyzer_App/
├── app.py
├── index.html
├── requirements.txt
├── README.md
├── .gitignore
└── saved_summary_model/   # Local model files; not included in Git
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Komal1897/Text_Analyzer_App.git
cd Text_Analyzer_App
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the model files

Place your trained or saved T5 model and tokenizer files inside the `saved_summary_model/` directory.

The application expects this local path:

```text
saved_summary_model/
```

**Note:** Model weights are not included in this repository because of their file size. You must obtain the model files separately before running the application.

### 5. Run the application

```bash
uvicorn app:app --reload
```

Open the application in your browser:

http://127.0.0.1:8000

## API Usage

The application exposes a REST API endpoint:

**Endpoint:** `POST /summarize/`

**Request body:**

```json
{
  "dialogue": "Enter the text you want to summarize here."
}
```

**Example response:**

```json
{
  "summary": "A concise summary of the provided text."
}
```

You can also test the endpoint using the interactive API documentation:

http://127.0.0.1:8000/docs

## Future Improvements

- Support summarization of PDF and text files.
- Add adjustable summary length.
- Deploy the application to a cloud platform.
- Host the model separately for easier deployment.

## Author

**Komal Maurya**

GitHub: [Komal1897](https://github.com/Komal1897)