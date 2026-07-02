# Secure Software Monitoring Platform

**Author:** Pedro Yanez Melendez

## Overview

The increasing adoption of AI systems in business environments creates the need for software platforms capable of monitoring prompt activity, classifying operational risk, persisting security events, and presenting actionable information through technical and executive views.

This repository contains a Python-based secure software monitoring platform focused on AI prompt risk analysis. The application combines backend risk classification, data persistence, API structure, automated testing, technical documentation, and a Streamlit-based monitoring interface.

## Purpose

The platform analyzes AI prompts and classifies potential operational, security, and privacy risks. Each analyzed prompt is converted into a structured event containing metadata, risk score, severity level, findings, and a recommended operational action.

The system is designed as a complete software application with separated components for business logic, persistence, API structure, frontend visualization, automated validation, and documentation.

## Core Capabilities

- Live AI prompt analysis.
- Risk scoring based on weighted detection rules.
- Severity classification: SAFE, LOW, MEDIUM, and HIGH.
- Detection of prompt injection patterns.
- Detection of sensitive data extraction attempts.
- Detection of credential exposure patterns.
- Detection of privacy-sensitive content.
- Detection of workplace misuse patterns.
- SQLite-based event persistence.
- Monitoring dashboard with operational metrics.
- Incident history with structured event records.
- Risk score distribution visualization.
- Severity aggregation visualization.
- Executive incident report generation.
- FastAPI backend service structure.
- Automated tests using Pytest.
- Reproducible execution from Google Colab.

## Architecture

The application follows a modular Python structure:

```text
secure-software-monitoring-platform/
│
├── src/
│   └── prompt_security/
│       ├── risk_engine.py
│       ├── storage.py
│       ├── traffic_generator.py
│       └── api.py
│
├── tests/
│   └── test_risk_engine.py
│
├── docs/
│   └── ARCHITECTURE.md
│
├── streamlit_app.py
├── requirements.txt
├── README.md
└── .gitignore
```

## Main Components

### Risk Engine

The backend risk engine evaluates prompt content using rule categories, regular expressions, weighted scoring, finding aggregation, severity classification, and recommended operational actions.

The detection logic covers:

- Prompt injection.
- Sensitive data extraction.
- Credential exposure.
- Privacy-related content.
- Workplace misuse.

### Persistence Layer

The storage layer uses SQLite to persist analyzed events. Each event includes timestamp, user identifier, source channel, prompt content, risk score, severity, findings, and recommended action.

### API Layer

The FastAPI structure provides backend service endpoints for:

- Health checks.
- Prompt analysis.
- Event retrieval.
- Operational prompt traffic generation.

### Monitoring Interface

The Streamlit frontend provides:

- Live prompt analysis.
- Alert visualization.
- KPI metrics.
- Severity distribution charts.
- Risk score distribution charts.
- Incident history.
- Executive incident report.

### Automated Testing

The project includes Pytest-based automated validation for core classification behavior. Tests verify that normal prompts, prompt injection attempts, and data extraction requests are classified consistently.

## Technologies

- Python
- Streamlit
- FastAPI
- SQLite
- Pandas
- Plotly
- Pytest
- Pydantic
- Regular expressions
- Modular backend architecture
- Event persistence
- API structure
- Automated testing
- Technical documentation

## How to Run

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
streamlit run streamlit_app.py
```

## How to Test

Run automated tests:

```bash
pytest -q
```

## Repository

https://github.com/p1y1m/secure-software-monitoring-platform
