# SmartResume AI 📄

SmartResume AI is a Streamlit web app that uses Google's Gemini API to help you analyze, score, and improve your resume — and prep for the job you're applying to.

**Live demo:** https://smartairesume.streamlit.app/

## Features

- **Resume Parsing & Scoring** — Upload a PDF resume and get a structured breakdown (skills, education, experience, projects, certifications, achievements) plus an overall quality score.
- **Job Description Matching** — Paste a job description and see how well your resume matches, with a gap analysis.
- **Interview Question Generation** — Get likely interview questions tailored to your resume and the target role.
- **Bullet Point Rewriting** — Turn weak resume bullets into stronger, impact-driven ones.
- **Cover Letter Generation** — Generate a tailored cover letter based on your resume and the job description.
- **PDF Report Export** — Download a polished PDF report summarizing your results.

## Tech Stack

- [Streamlit](https://streamlit.io/) — web app framework
- [Google Generative AI (Gemini)](https://ai.google.dev/) — resume parsing, scoring, and generation
- [PyMuPDF](https://pymupdf.readthedocs.io/) — PDF text extraction
- [Plotly](https://plotly.com/python/) — score visualizations
- [ReportLab](https://www.reportlab.com/) — PDF report generation

## Getting Started

### Prerequisites

- Python 3.11+
- A [Gemini API key](https://aistudio.google.com/apikey)

### Installation

```bash
# Clone the repo
git clone https://github.com/jashaneja/SmartResume.git
cd SmartResume

# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Configuration

Create a `.env` file in the project root:

```
GEMINI_API_KEY=your_api_key_here
```

### Run locally

```bash
streamlit run app.py
```

The app will open at `http://localhost:8501`.

## Deployment

This app is deployed on [Streamlit Community Cloud](https://share.streamlit.io/). To deploy your own copy:

1. Push this repo to your own GitHub account.
2. Go to [share.streamlit.io](https://share.streamlit.io) and create a new app pointing to `app.py`.
3. In the app's **Secrets** settings, add:
   ```toml
   GEMINI_API_KEY = "your_api_key_here"
   ```

## Project Structure

```
SmartResume/
├── app.py                     # Main Streamlit app
├── utils/
│   ├── gemini_helper_new.py   # Gemini API integration
│   ├── pdf_parser.py          # Resume PDF text extraction
│   ├── pdf_report.py          # PDF report generation
│   └── resume_rewriter.py     # Bullet point rewriting logic
├── .streamlit/
│   └── config.toml            # Streamlit theme config
├── requirements.txt
└── runtime.txt
```

## License

This project currently has no license specified. Add one (e.g. MIT) if you plan to accept contributions or want others to reuse the code.
