# Learning Management System (LMS)

A simple Learning Management System built with Flask that allows students and instructors to manage courses, track progress, and interact through a discussion forum.

## Features

- User authentication (Student/Instructor roles)
- Course management
- Course enrollment
- Progress tracking
- Discussion forum
- Certificate generation
- Email notifications

## Setup

1. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Configure email settings:
Edit `app.py` and update the following settings with your email credentials:
```python
app.config['MAIL_USERNAME'] = 'your-email@gmail.com'
app.config['MAIL_PASSWORD'] = 'your-app-password'
```

4. Initialize the database:
```bash
flask shell
>>> from app import db
>>> db.create_all()
>>> exit()
```

5. Run the application:
```bash
python app.py
```

The application will be available at `http://localhost:5000`

## Usage

1. Register as either a student or instructor
2. Login to your account
3. Browse available courses
4. Enroll in courses (students only)
5. Track your progress
6. Participate in discussions
7. Download certificates upon completion

## Security Notes

- Change the `SECRET_KEY` in `app.py` before deploying
- Use environment variables for sensitive information
- Implement proper password hashing (already included)
- Set up proper email authentication

## Contributing

Feel free to submit issues and enhancement requests! 