This is a Personalized AI Profile Assistant web application. Users submit personal information, and the AI generates personalized advice, recommendations, and career guidance.

It supports two models:

Base Model: generic AI responses

Trained Model: pseudo-trained, personalized responses using collected user data

Features

Collects user information (Full Name, Origin, Residence, Purpose, Preferred Language)

Saves user data locally (users.json)

Generates AI responses via Base or Trained model

Responses persist on screen until user manually refreshes

Minimal, functional frontend (no styling required)

Project Structure
project/
│
├─ backend/
│   ├─ main.py           # FastAPI backend
│   ├─ services.py       # AI response & pseudo-training logic
│   ├─ users.json        # Saved user data
│   └─ requirements.txt
│
└─ frontend/
    ├─ index.html        # User form
    └─ script.js         # Frontend logic

Installation & Run
Backend
cd backend
python -m venv venv
venv\Scripts\activate   # Windows
pip install -r requirements.txt
uvicorn main:app --reload

Frontend

Open frontend/index.html in your browser (or use VS Code Live Server)

Usage

Fill in the form with user details

Select Base Model or Trained Model

Click Submit

Response appears below the form and stays until manual refresh

Notes

The Trained Model is pseudo-trained — it simulates personalized responses using stored data.

CORS is enabled for local testing (localhost)
