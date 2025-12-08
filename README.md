# User Management System (Django + DRF + JWT + React)

A full-stack user management system with:

- User registration and login
- JWT authentication
- Protected profile
- Admin user management
- React frontend with API integration

---

## Backend: Django + DRF + JWT

### Features

- Custom user model with roles
- JWT authentication (access & refresh tokens)
- API endpoints:
  - `/api/register/` → Create new user
  - `/api/login/` → Obtain JWT
  - `/api/refresh/` → Refresh access token
  - `/api/profile/` → Retrieve logged-in user profile
  - `/api/users/` → Admin-only: list all users

### Screenshots
### Register Page
![Alt text](images/register.png)
### Login Page
![Alt text](images/login.png)
### Dashbaord
![Alt text](images/dashbaord.png)
### Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/dalyzhee/Django-DRF-JWT-React-User-Management-System.git
cd config
```

2. Create a virtual environment and install dependencies:

```
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
pip install -r requirements.txt
```

3. Run migrations:

```
python manage.py makemigrations
python manage.py migrate
```

4. Create superuser (optional, for admin access):
```
python manage.py createsuperuser
```

Run the server:
```
python manage.py runserver
```

API will be available at:

http://127.0.0.1:8000/api/

## Project Structure

backend/
├─ config/
│  ├─ settings.py
│  └─ urls.py
├─ users/
│  ├─ models.py
│  ├─ serializers.py
│  ├─ views.py
│  └─ urls.py
└─ manage.py

# Frontend: React
## Features

1. Registration page
2. Login page with JWT authentication
3. Protected profile page
4. Axios with JWT interceptor
5. Routing with react-router-dom

## Setup Instructions

Navigate to the frontend folder:

```
cd client
```

Install dependencies:
```
npm install
```

Run the development server:
```
npm start
```

React app will be available at:
```
http://localhost:3000/
```

## Project Structure

client/
├─ src/
│  ├─ api.js          # Axios instance with JWT interceptor
│  ├─ App.js          # Routing
│  ├─ Register.js
│  ├─ Login.js
│  └─ Profile.js
└─ package.json

# Usage

1. Start Django backend first (python manage.py runserver)

2. Start React frontend (npm start)

3. Open browser at http://localhost:3000

4. Register a new user or login with an existing account

5. Access protected profile page after login

# Notes

JWT tokens are stored in localStorage
React automatically sends token in Authorization header for protected endpoints

For development, CORS is enabled for all origins

Admin can access /api/users/ to see all users

# Next Steps / Improvements

- Add password reset functionality

- Implement role-based dashboards

- Add refresh token logic on frontend

- Use environment variables for API URL in React

- Deploy backend (e.g., Heroku, DigitalOcean) and frontend (Netlify, Vercel)

# Contact / Author

Name: Levis Odhiambo

Email: odhiambolevis967@gmail.com