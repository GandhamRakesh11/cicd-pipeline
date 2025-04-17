# 🛠️ Deployment Setup: Flask + Gunicorn + GitHub CI/CD

## ✅ Local Development & Deployment

### 1. Create & Activate Virtual Env
```bash
python -m venv venv
source venv/bin/activate       # or venv\Scripts\activate
#### 2.install dependencies
  pip install -r requirements.txt
#### 3.Run with Gunicorn/waitress
    waitress-serve --host=0.0.0.0 --port=8000 app:app
##### 4. CI/CD with GitHub Actions
Workflow file: .github/workflows/flask-ci.yml

Triggers:
Every push or PR to main

Steps:
Check out the repo

Set up Python

Install requirements

Run a basic Gunicorn/waitress server

Check that it returns a response

Note:::here i used instead of gunicorn i used waitress server for flask application