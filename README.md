# Campus-Event-Management-System
Campus Event Management System enables staff to create events, track student registration, attendance, and feedback, while students can browse, register, attend, and submit feedback efficiently.
# API Connectivity
Authentication

  POST /api/auth/register/ → Register new student

  POST /api/auth/login/ → Login with credentials

  POST /api/auth/logout/ → Logout user

Events

  GET /api/events/ → Get all events
  GET /api/events/{id}/ → Get event details
  POST /api/events/ → Create new event (Admin only)
  PUT /api/events/{id}/ → Update event (Admin only)
  DELETE /api/events/{id}/ → Delete event (Admin only)

Registrations

  POST /api/register/ → Student registers for an event
  DELETE /api/register/{id}/ → Cancel registration

Attendance

  POST /api/attendance/mark/ → Mark student attendance

Feedback

  POST /api/feedback/ → Submit event feedback
  GET /api/feedback/{event_id}/ → View event feedback

# bash

campusevents/
│── campusevents/               # Project config (settings, urls, wsgi, asgi)
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
│
│── events/                     # Main app (business logic)
│   ├── models.py               # Database models (User, Event, Registration, etc.)
│   ├── views.py                # Views for staff & students
│   ├── forms.py                # Forms for signup & event creation
│   ├── urls.py                 # App-specific routing
│   ├── templates/              # HTML templates
│   │   ├── base.html
│   │   ├── login.html
│   │   ├── signup.html
│   │   ├── staff_dashboard.html
│   │   ├── student_dashboard.html
│   │   └── reports/            # Report templates
│   └── admin.py                # Django admin customization
│
│── templates/                  # Global templates folder
│── static/                     # CSS, JS, images (optional)
│── .env                        # Environment variables
│── manage.py                   # Django project manager



# Technologiies Used

  Backend Framework → Django 5.x (Python 3.13)
  Database → PostgreSQL (with Django ORM)
  Frontend → Django Templates + Bootstrap
  Authentication → CustomUser model (email login)
  Reports → CSV Export (Django + Python CSV module)
  
  Deployment Ready → Supports .env for secure configs
  
