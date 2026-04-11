# CICD Workflow Demo

A sample Django application demonstrating a full CI/CD pipeline using GitHub Actions.

---

## Features

- **Automated Tests & Build:**  
  Runs on push and PR to `main`. Checks out code, sets up Python, installs dependencies, runs migrations, and executes tests.
- **Customizable Pipeline:**  
  Easily edit `.github/workflows/main.yml` for your own build steps.
- **Modern Python Tooling:**  
  Uses Python 3.9, pip, pytest, and Django best practices.

---

## Quick Start

### Prerequisites

- Python 3.9+
- pip

### Setup

```bash
git clone https://github.com/frex1/cicd_workflow.git
cd cicd_workflow
pip install -r requirements.txt
python manage.py migrate
python manage.py test      # or pytest -v
```

---

## CI/CD with GitHub Actions

Workflow: [.github/workflows/main.yml](https://github.com/frex1/cicd_workflow/blob/main/.github/workflows/main.yml)

#### Pipeline Steps:
1. **Trigger:** On push/PR to `main` or manual dispatch.
2. **Checkout:** Checks out the repo.
3. **Setup Python:** Uses Python 3.9.
4. **Install dependencies:** Upgrades pip; installs from `requirements.txt`.
5. **Migrate database:** Runs Django migrations.
6. **Test:** Runs all tests using pytest (verbose).

---

## Requirements

From `requirements.txt`:

```
django==3.2.2
gunicorn==20.0.4
djangorestframework==3.12.4
pytest==6.2.5
pytest-django==4.4.0
```

---

## Project Structure

```
cicd_workflow/
├── .github/workflows/main.yml
├── manage.py
├── requirements.txt
└── ...
```

---

## License

MIT

---

## Author

[@frex1](https://github.com/frex1)

---

## Issues

Open issues for improvements or questions: https://github.com/frex1/cicd_workflow/issues
