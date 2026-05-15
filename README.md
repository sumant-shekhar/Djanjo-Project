# Travello Django Project

A full-stack web application built with Django that allows users to browse travel destinations. It includes user authentication and a dynamic frontend that displays destinations from the database.

## ✨ Features

- **User Authentication**: Complete user registration, login, and logout functionality with appropriate validation (e.g., password matching, unique email/username checks).
- **Travel Destinations**: Browse a variety of travel destinations with details like images, descriptions, prices, and special offers.
- **Dynamic Content**: Destinations and their details are dynamically loaded from the database.
- **Media Handling**: Support for uploading and displaying images for each destination.

## 🛠️ Technologies Used

- **Backend Framework**: Django (Python)
- **Database**: PostgreSQL (configured via `psycopg`)
- **Image Processing**: Pillow
- **Task Queue & Caching**: Celery & Redis
- **Dependency Management**: `pyproject.toml`

## 📂 Project Structure

```text
Djanjo-Project/
├── accounts/           # User authentication app (Login, Register, Logout)
├── travello/           # Main app for handling travel destinations
│   ├── models.py       # Destination database schema
│   └── views.py        # Views for rendering the destination page
├── static/             # Static files (CSS, JS, images)
├── templates/          # HTML Templates (index, login, register)
├── media/              # User-uploaded media (Destination images)
├── pyproject.toml      # Project dependencies and configurations
└── manage.py           # Django command-line utility
```

## 🚀 Getting Started

### Prerequisites

- Python 3.11+
- PostgreSQL
- Redis (optional, for Celery/Caching)

### Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   cd Djanjo-Project
   ```

2. **Set up the virtual environment and install dependencies**:
   You can use `pip` or modern tools like `uv`:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   pip install -e .
   ```
   *(Alternatively, if using `uv`, run `uv sync` or `uv pip install -e .`)*

3. **Run Migrations**:
   Set up your database schema:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Create a Superuser (Optional)**:
   To access the Django Admin panel and add destinations:
   ```bash
   python manage.py createsuperuser
   ```

5. **Start the Development Server**:
   ```bash
   python manage.py runserver
   ```

6. **Access the App**:
   Open your browser and visit `http://127.0.0.1:8000` to see the application. You can manage destinations by visiting `http://127.0.0.1:8000/admin`.

## 📝 License

This project is open-source and available under the MIT License.
