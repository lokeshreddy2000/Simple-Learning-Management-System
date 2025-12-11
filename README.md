# Simple Learning Management System API (Django REST Framework)

A simple Learning Management System (LMS) backend built with **Django** and **Django REST Framework**.

## Features

- Manage **courses** with title, description, level, published flag
- Add **lessons** under each course
- **Enroll** users into courses
- Track **lesson progress** (completed / not completed) per enrollment
- Basic permission rules (only logged-in users can enroll & track progress)
- Django admin panel to manage all data

## Tech Stack

- Python
- Django
- Django REST Framework
- SQLite (default, can be replaced with PostgreSQL/MySQL)

## Setup

```bash
python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate
pip install -r requirements.txt

python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

## API Endpoints (Main)

- `GET /api/courses/` – list courses
- `POST /api/courses/` – create course (auth required)
- `GET /api/courses/<id>/` – retrieve course
- `PUT/PATCH /api/courses/<id>/` – update course
- `DELETE /api/courses/<id>/` – delete course

- `GET /api/courses/<course_id>/lessons/` – list lessons for a course
- `POST /api/courses/<course_id>/lessons/` – create lesson

- `GET /api/enrollments/` – list your enrollments
- `POST /api/enrollments/` – enroll into a course

- `GET /api/enrollments/<enrollment_id>/progress/` – list progress for an enrollment
- `POST /api/enrollments/<enrollment_id>/progress/` – create progress entry for a lesson
- `PATCH /api/progress/<id>/` – update progress (mark completed)

## How to Use for Portfolio / GitHub

- Fork or clone this repo
- Add more fields (e.g., quizzes, assignments, certificates)
- Deploy to a platform like Render / Railway / Heroku
- Link it from your resume and portfolio as **"LMS Backend API in Django"**
