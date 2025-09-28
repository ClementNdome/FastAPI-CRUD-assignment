# 🎯 FastAPI CRUD Application
A simple **FastAPI** project demonstrating full CRUD (Create, Read, Update, Delete) operations  
for **Students** and **Courses** using **SQLite** and **SQLAlchemy**.

---

## 🚀 Features
- FastAPI backend with automatic Swagger UI
- SQLite database (no external setup required)
- Full CRUD for two entities:
  - **Students**: name, email
  - **Courses**: title, description
- Pydantic v2 models for input/output validation

---

## 🛠️ Tech Stack
| Component   | Technology           |
|-------------|----------------------|
| Backend     | [FastAPI](https://fastapi.tiangolo.com/) |
| Database    | SQLite + SQLAlchemy ORM |
| Validation  | Pydantic v2 |
| Server      | Uvicorn (ASGI) |

---

## 📦 Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/fastapi_crud_app.git
cd fastapi_crud_app
```
### 2️⃣ Create and activate a virtual environment
bash
python -m venv venv
##### Windows
```bash
venv\Scripts\activate
```
##### Linux/Mac
```bash
source venv/bin/activate
```
### 3️⃣ Install dependencies
```python
pip install -r requirements.txt
```
### 4️⃣ Start the development server
```bash
uvicorn app.main:app --reload
```
### 5️⃣ Access the API
Swagger UI → http://127.0.0.1:8000/docs

ReDoc → http://127.0.0.1:8000/redoc

## 🔗 API Endpoints
Students
Method	Endpoint	Description	Request Body (JSON)
POST	/students/	Create a student	{ "name": "Alice", "email": "alice@mail.com" }
GET	/students/	List all students	–
PUT	/students/{id}	Update a student	{ "name": "New Name", "email": "new@mail.com" }
DELETE	/students/{id}	Delete a student	–

Courses
Method	Endpoint	Description	Request Body (JSON)
POST	/courses/	Create a course	{ "title": "Math 101", "description": "Intro to Math" }
GET	/courses/	List all courses	–
PUT	/courses/{id}	Update a course	{ "title": "New Title", "description": "Updated description" }
DELETE	/courses/{id}	Delete a course	–

### Example Requests
Create a Student:


```bash
curl -X POST http://127.0.0.1:8000/students/ \
-H "Content-Type: application/json" \
-d '{"name":"Alice","email":"alice@mail.com"}'
```
Fetch All Courses:

```bash
curl http://127.0.0.1:8000/courses/
```
## Notes
- Database file crud.db is auto-created on first run.
- Pydantic v2 is used; the config key from_attributes replaces the old orm_mode.

