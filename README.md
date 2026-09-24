# AI Finance Operations Agent

AI-assisted invoice processing and finance analytics portfolio project.

> **Portfolio project:** an end-to-end workflow that turns invoice PDFs into structured finance data, applies deterministic business validation and anomaly checks, and presents the results in an interactive Streamlit dashboard.

## 🌐 Live Demo

**[🚀 Launch Live Demo](https://ai-finance-operations-agent-thkprarbd4kpd38cbba2qg.streamlit.app/)**

## Workflow

**Invoice PDF → Text Extraction → Gemini AI / Fallback Extraction → Validation → Duplicate Detection → Vendor Anomaly Detection → Risk Classification → Persistent CSV → Streamlit Dashboard**

## What it demonstrates

- PDF invoice extraction
- Gemini AI-assisted field extraction
- Deterministic fallback parsing when Gemini is unavailable or quota-limited
- Independent invoice-total validation
- Duplicate invoice detection
- Vendor spending anomaly detection
- Risk classification
- Persistent invoice analysis
- Interactive finance KPIs and filters
- Upload and process new invoice PDFs

## Architecture

```text
Invoice PDF
    ↓
PDF text extraction
    ↓
Gemini AI extraction ──→ Fallback parser if AI unavailable
    ↓
Business validation + duplicate detection + anomaly detection
    ↓
Risk classification
    ↓
CSV persistence + Streamlit dashboard
```

## Tech stack

Python • Streamlit • Pandas • Pydantic • PyPDF • Google Gemini

## Repository structure

```text
dashboard/app.py              # Streamlit application
data/sample_invoices/         # Sample-data documentation
docs/architecture.md          # Architecture notes
docs/linkedin-post.md         # LinkedIn launch draft
output/dashboard_data.csv     # Demo dataset
tests/test_project.py         # Dataset tests
requirements.txt              # Python dependencies
```

## Run locally

```bash
pip install -r requirements.txt
streamlit run dashboard/app.py
```

For Gemini-powered extraction, configure `GEMINI_API_KEY` as an environment variable or Streamlit secret. **Never commit API keys to GitHub.**

## Deployment

This project is designed for Streamlit Community Cloud.

- Repository: `akkisakpal/AI-Finance-Operations-Agent`
- Branch: `main`
- Entry point: `dashboard/app.py`
- Secret: `GEMINI_API_KEY`

## Demo dataset

The repository includes a seven-invoice demo dataset covering:

- approved invoices
- invalid totals
- duplicate invoices
- vendor spending anomalies
- multiple risk levels

## Demo results

The included demo dataset contains **7 invoices** with **3 requiring review**, including:

- 1 vendor-spending anomaly
- 1 potential duplicate
- 1 invoice with an invalid total
- Low, Medium and High risk examples
- €20,511.50 total demo invoice value

These examples are included to demonstrate how the validation and risk rules behave across different invoice conditions.

## CI

GitHub Actions runs a Python syntax check and dataset tests on repository changes.

## Author

**Akshay Sakpal**

Data Analytics • Python • AI • Machine Learning • Data Engineering