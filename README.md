![Python](https://img.shields.io/badge/python-3.9+-blue?logo=python)
![Flask](https://img.shields.io/badge/flask-2.0+-black?logo=flask)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Made with CS50](https://img.shields.io/badge/Made%20with-CS50-red)
![Status](https://img.shields.io/badge/status-active-brightgreen)
![Contributions](https://img.shields.io/badge/contributions-welcome-orange)

🎉 Birthday Tracker Flask App

A simple yet effective web app to store and display birthdays using Flask and SQLite. Add birthdays, view the list of saved entries, and make sure you never forget your friends' special days again!

🚀 Features

✅ Add birthdays via a clean form

✅ View all stored birthdays

✅ Input validation (no blank names or invalid dates)

✅ Data stored using SQLite and CS50’s SQL library

✅ Flashy Flask routing and template rendering

✅ Lightweight and easy to run

🧠 Technologies Used

Python 3

Flask – lightweight WSGI web application framework

SQLite – self-contained SQL database

CS50's SQL Library – simplified interface to interact with SQLite

HTML/CSS (Jinja2) – for templating and rendering frontend

Bootstrap (optional but recommended) – for styling

📂 Project Structure
/birthday-app
├── app.py               # Main Flask application
├── birthdays.db         # SQLite database file
├── templates/
│   └── index.html       # Main HTML template
├── static/              # (Optional) For CSS/JS files
├── requirements.txt     # Dependencies (Flask, cs50)
└── README.md            # You're reading it 😉

⚙️ Setup & Installation
🐍 1. Clone the Repository
git clone https://github.com/6kristian/birthday-tracker.git
cd birthday-tracker

📦 2. Create a Virtual Environment (optional but recommended)
python3 -m venv venv
source venv/bin/activate

🛠️ 3. Create the SQLite Database

Make sure you have a birthdays.db file with the following schema:

CREATE TABLE birthdays (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    month INTEGER NOT NULL,
    day INTEGER NOT NULL
);


You can create it using:

sqlite3 birthdays.db < schema.sql


Where schema.sql contains the SQL above.

💻 Running the App
export FLASK_APP=app.py
export FLASK_ENV=development  # Optional: enables debug mode
flask run


Visit http://127.0.0.1:5000
 in your browser.

🧪 Usage

Fill in the name, month, and day fields in the form

Submit to save the birthday

See all saved birthdays listed below the form

🧼 Input Validation

Name must not be empty

Month must be between 1 and 12

Day must be between 1 and 31

Redirects safely on invalid input to prevent bad data

🛡️ Security Notes

No direct SQL is written by hand – all queries are parameterized via CS50 library

Basic request validation to prevent bad form submissions

Caching disabled to always show fresh data

✨ Example Screenshot (optional)

Insert a screenshot of the app here showing the form and birthday list

🤝 Contributing

Contributions are welcome! Here’s how:

Fork the repo

Create a new branch: git checkout -b feature/your-feature-name

Commit your changes: git commit -m 'Add some feature'

Push to the branch: git push origin feature/your-feature-name

Open a pull request

📜 License

