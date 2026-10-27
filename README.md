# Full Stack Application Development Capstone Project - Cars Dealership

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python](https://img.shields.io/badge/Python-3.10%20%7C%203.12-blue.svg)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-4.2-green.svg)](https://www.djangoproject.com/)
[![React](https://img.shields.io/badge/React-18.2-blue.svg)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-Express-green.svg)](https://nodejs.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-blue.svg)](https://www.docker.com/)

> **IBM Full Stack Software Developer Capstone Project**  
> A national car dealership network web application that enables users to browse dealership branches across the U.S., view detailed reviews with AI sentiment analysis, and submit new customer reviews.

---

## 📋 Project & Repository Details
- **Project Name:** Full Stack Application Development Capstone Project
- **Application Name:** Best Cars Dealership
- **Repository URL:** [https://github.com/AjCodes25/Full-Stack-Application-Development-Capstone-Project](https://github.com/AjCodes25/Full-Stack-Application-Development-Capstone-Project)
- **Author:** Ajinkya Mangave ([AjCodes25](https://github.com/AjCodes25))
- **Role:** Lead Full-Stack Software Developer

---

## 🛠️ Technology Stack & Architecture

### Architecture Overview
The application is built on a distributed microservices architecture:
1. **Frontend:** React application integrated with Django static templating and responsive UI.
2. **User Management & Backend:** Django REST Framework handling user authentication (session/cookies), SQLite database for Car Makes & Models, and proxy API endpoints.
3. **Dealership & Reviews Microservice:** Node.js Express server connected to MongoDB storing dealership locations and customer reviews.
4. **Sentiment Analysis Microservice:** Python/Flask microservice utilizing IBM Watson NLU / Natural Language Processing to analyze review sentiment (`positive`, `neutral`, `negative`).
5. **DevOps & CI/CD:** Docker containerization, Kubernetes orchestration, IBM Cloud Code Engine, and automated GitHub Actions workflows with `flake8` and `pytest`.

### Technology Breakdown
- **Frontend:** React, HTML5, CSS3, Bootstrap 5, JavaScript (ES6+)
- **Backend:** Python 3, Django, Django REST Framework
- **Databases:** MongoDB (NoSQL for Dealerships & Reviews), SQLite (Relational DB for Car Makes & Models)
- **Microservices:** Node.js / Express, Python / Flask Sentiment Analyzer
- **Deployment & Cloud:** Docker, Kubernetes, IBM Cloud Code Engine, GitHub Actions CI/CD

---

## 📂 Repository Structure

```
├── .github/workflows/main.yml    # CI/CD GitHub Actions workflow
├── .flake8                       # Python linter configuration
├── README.md                     # Project documentation and details
├── screenshots/                  # Submission screenshots for all tasks
│   ├── admin_login.png
│   ├── admin_logout.png
│   ├── get_dealers.png
│   ├── get_dealers_loggedin.png
│   ├── dealersbystate.png
│   ├── dealer_id_reviews.png
│   ├── dealership_review_submission.png
│   ├── added_review.png
│   ├── deployed_landingpage.png
│   ├── deployed_loggedin.png
│   ├── deployed_dealer_detail.png
│   └── deployed_add_review.png
├── Project-Deliverables/          # cURL commands, outputs, and log artifacts
│   ├── django_server
│   ├── loginuser
│   ├── logoutuser
│   ├── getdealerreviews
│   ├── getalldealers
│   ├── getdealerbyid
│   ├── getdealersbyState
│   ├── getallcarmakes
│   ├── analyzereview
│   ├── CICD
│   └── deploymentURL
└── server/
    ├── database/                 # Node.js Express + MongoDB service
    ├── djangoapp/                # Django application (views, models, APIs)
    ├── djangoproj/               # Django root project settings
    ├── frontend/                 # React frontend source & static pages
    │   ├── src/components/       # React components (Register, Dealers, etc.)
    │   └── static/               # Static pages (About.html, Contact.html)
    ├── Dockerfile                # Multi-stage Docker configuration
    └── requirements.txt          # Python dependencies
```

---

## 🚀 Running the Application Locally

### 1. Start Dealership & Reviews Database (Node.js & MongoDB)
```bash
cd server/database
npm install
node app.js
```

### 2. Start Sentiment Analyzer Microservice (Flask)
```bash
cd server/djangoapp/microservices
pip install -r requirements.txt
python3 app.py
```

### 3. Run Django Backend Server
```bash
cd server
pip install -r requirements.txt
python3 manage.py makemigrations
python3 manage.py migrate
python3 manage.py runserver 0.0.0.0:8000
```

---

## 📜 Key Endpoints

| Endpoint | Method | Description |
|---|---|---|
| `/about` | GET | Displays static "About Us" page |
| `/contact` | GET | Displays static "Contact Us" page |
| `/djangoapp/login` | POST | Authenticates user |
| `/djangoapp/logout` | GET | Logs out current user |
| `/djangoapp/register` | POST | Registers new user account |
| `/djangoapp/get_cars` | GET | Fetches all car makes and models |
| `/djangoapp/get_dealers` | GET | Fetches all dealerships |
| `/djangoapp/get_dealers/<state>` | GET | Filters dealerships by state |
| `/djangoapp/dealer/<id>` | GET | Fetches dealer details by ID |
| `/djangoapp/reviews/dealer/<id>` | GET | Fetches reviews for specific dealer |
| `/djangoapp/add_review` | POST | Submits customer review |

---

## 👤 Author
- **Developer:** Ajinkya Mangave
- **GitHub:** [@AjCodes25](https://github.com/AjCodes25)
- **Project:** Full Stack Application Development Capstone Project
