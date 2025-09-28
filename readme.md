# FastAPI CRUD Application
A simple CRUD API using **FastAPI**, **SQLite**, and **SQLAlchemy**.

## Features
- CRUD operations for **Students** and **Courses**
- Automatic interactive API docs at `/docs`

## Setup
```bash
git clone https://github.com/your-username/fastapi_crud_app.git
cd fastapi_crud_app
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --reload
