![CI/CD Pipeline](https://github.com/prabhkaur6119/flask-cicd-pipeline/actions/workflows/ci-cd.yml/badge.svg)
# Flask CI/CD Pipeline Using GitHub Actions and Docker

## Project Overview
This project demonstrates a Continuous Integration (CI) workflow for a Python Flask application using GitHub Actions. It automatically runs application tests and builds a Docker image when code is pushed to the main branch.

## Technologies Used
- Python 3.12
- Flask
- Pytest
- Git and GitHub
- GitHub Actions
- Docker

## Application Features
- Flask home endpoint (`/`)
- Health-check endpoint (`/health`)
- Automated tests for both endpoints
- Automated Docker image build

## CI/CD Workflow
1. Code is pushed to GitHub.
2. GitHub Actions checks out the repository.
3. Python is configured and dependencies are installed.
4. Pytest runs the automated tests.
5. If the tests pass, Docker builds the application image.

## Project Structure
```text
flask-cicd-pipeline/
├── app.py
├── requirements.txt
├── test_app.py
├── Dockerfile
└── .github/
    └── workflows/
        └── ci-cd.yml
```

## How to Run Locally
Install the dependencies:

```bash
pip install -r requirements.txt
```

Start the Flask application:

```bash
python app.py
```

Open `http://127.0.0.1:5000/` in your browser.

## Run Automated Tests
```bash
pip install pytest
pytest -v
```

## Build the Docker Image
```bash
docker build -t flask-cicd-pipeline .
```

## Learning Outcomes
- Configuring a GitHub Actions workflow
- Writing automated tests with Pytest
- Building Docker images
- Understanding CI/CD automation

**Note:** The workflow builds the Docker image but does not publish it to a registry or deploy the application.
