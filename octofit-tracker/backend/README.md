# OctoFit Tracker - Django Backend

This is the Django REST API backend for the OctoFit Tracker application.

## Setup

### 1. Create and activate virtual environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set up environment variables (optional)

For development, the application will use default values. For production, set:

```bash
export DJANGO_SECRET_KEY='your-secret-key-here'
export MONGODB_USERNAME='your-mongodb-username'
export MONGODB_PASSWORD='your-mongodb-password'
```

### 4. Set up MongoDB

Make sure MongoDB is running on localhost:27017 (default port).

### 5. Run migrations

```bash
python manage.py migrate
```

### 6. Populate the database (optional)

```bash
python manage.py populate_db
```

### 7. Run the development server

```bash
python manage.py runserver 0.0.0.0:8000
```

The API will be available at `http://localhost:8000/api/`

## API Endpoints

- `/api/users/` - User management
- `/api/teams/` - Team management
- `/api/activities/` - Activity tracking
- `/api/workouts/` - Workout catalog
- `/api/leaderboard/` - Team leaderboard

## Running in GitHub Codespaces

When running in a GitHub Codespace, the application automatically configures the correct URLs using the `CODESPACE_NAME` environment variable.
