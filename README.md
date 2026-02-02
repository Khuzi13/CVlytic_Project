# CVlytics

CVlytics is an advanced Resume Analyzer and Applicant Tracking System (ATS) support tool built with Django and Machine Learning. It helps job seekers and recruiters evaluate resumes by analyzing content, formatting, and relevance to job descriptions.

## 🚀 Features

*   **ATS Scoring:** Utilizes a trained XGBoost machine learning model (`ats_xgb_model.pkl`) to predict how well a resume performs in standard ATS systems.
*   **Resume Parsing:** robustly extracts text from PDF resumes using `pdfplumber`.
*   **Job Description Matching:** semantic analysis to compare resumes against specific Job Descriptions (JD) for relevance scoring.
*   **Parse Rate Analysis:** Checks how readable the resume is for automated machines.
*   **AI Suggestions:** Provides actionable, AI-driven feedback to improve resume quality (e.g., adding keywords, fixing formatting).
*   **Detailed Breakdown:** Granular scoring on various metrics including skills, experience, and education.
*   **Recruiter Dashboard:** Tools for recruiters to analyze multiple candidates effectively.

## 🛠️ Tech Stack

*   **Framework:** Django 4.3 (Python)
*   **Machine Learning:** XGBoost, Scikit-Learn, Pandas, NumPy
*   **Data Processing:** PDFPlumber, Joblib
*   **Frontend:** HTML5, CSS3, JavaScript (Django Templates)
*   **Database:** SQLite (Development), PostgreSQL (Production-ready config available)

## 📋 Prerequisites

*   Python 3.9+
*   pip (Python Package Manager)

## ⚙️ Installation

1.  **Clone the repository:**
    ```bash
    git clone <repository_url>
    cd CVlytics
    ```

2.  **Create and activate a virtual environment (optional but recommended):**
    ```bash
    python -m venv venv
    # Windows
    venv\Scripts\activate
    # macOS/Linux
    source venv/bin/activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Apply database migrations:**
    ```bash
    python manage.py migrate
    ```

5.  **Run the development server:**
    ```bash
    python manage.py runserver
    ```

6.  **Access the application:**
    Open your browser and navigate to `http://127.0.0.1:8000/`

## 📂 Project Structure

```
CVlytics/
├── CVlytics/               # Main project and app configuration
│   ├── settings.py         # Django settings
│   ├── urls.py             # URL routing
│   ├── views.py            # View logic
│   ├── models.py           # Database models
│   ├── predict_ats_score.py # Core ML scoring logic
│   ├── pdf_pipeline.py     # PDF text extraction
│   └── ... (ML models and helpers)
├── templates/              # HTML templates
├── static/                 # CSS, JS, and Images
├── media/                  # User uploaded files (Resumes)
├── manage.py               # Django management script
└── requirements.txt        # Python dependencies
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1.  Fork the project
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request
