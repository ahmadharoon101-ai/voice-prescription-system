# Voice-Based Medicine Prescription Entry System

A web-based **Voice Prescription System** designed to help doctors and healthcare professionals enter medicine prescriptions efficiently using voice input, medicine search, and prescription management.

The system converts the doctor's spoken input into text and assists in identifying medicines from a medicine database. It combines **speech-to-text technology, fuzzy medicine matching, and prescription management** into a single application.

## 🚀 Features

* 🎤 **Voice-to-Text Prescription Entry**

  * Record the doctor's voice through the browser.
  * Convert spoken instructions into text.
  * Supports voice-based medicine entry.

* 🔎 **Medicine Search**

  * Search medicines from the medicine database.
  * Supports fuzzy matching for medicine names.
  * Displays medicine matching results and percentage scores.

* 💊 **Prescription Management**

  * Add medicines to a prescription.
  * Manage selected medicines.
  * Enter medicine information manually when required.

* 🗃️ **Medicine Database**

  * Uses a CSV-based medicine catalog.
  * Contains more than 12,000 medicine records.
  * Medicine names are loaded automatically when the backend starts.

* 🔌 **REST API**

  * FastAPI-based backend.
  * Provides API endpoints for frontend-backend communication.
  * Supports medicine search and prescription-related operations.

* 🔐 **Backend Database**

  * Database initialization and management through the backend.
  * Supports storing application data and prescription information.

## 🏗️ System Architecture

```text
Doctor
   │
   ▼
Frontend Web Application
   │
   ├── Voice Recording
   ├── Speech-to-Text
   ├── Medicine Search
   └── Prescription Management
   │
   ▼
FastAPI Backend
   │
   ├── API Routes
   ├── Medicine Search
   ├── Fuzzy Matching
   ├── Prescription Management
   └── Database Operations
   │
   ├───────────────┐
   ▼               ▼
Medicine CSV     Database
```

## 🛠️ Technologies Used

### Frontend

* HTML
* CSS
* JavaScript
* Browser Audio Recording
* WebSocket communication

### Backend

* Python
* FastAPI
* Uvicorn
* SQLAlchemy
* Pydantic

### AI / Speech Processing

* Whisper Speech-to-Text
* Fuzzy Medicine Matching

### Database / Data

* CSV Medicine Dataset
* SQL Database

### Development Tools

* Visual Studio Code
* Git
* GitHub

## 📁 Project Structure

```text
voice-prescription-system/
│
├── backend/
│   ├── data/
│   │   └── medicine.csv
│   │
│   ├── models/
│   │   └── whisper/
│   │
│   ├── __init__.py
│   ├── main.py
│   ├── config.py
│   ├── models.py
│   ├── schemas.py
│   └── ...
│
├── frontend/
│   ├── index.html
│   ├── css/
│   ├── js/
│   └── ...
│
├── .env.example
├── .gitignore
├── README.md
└── requirements.txt
```

> The exact files and folders may vary depending on the current project version.

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/ahmadharoon101-ai/voice-prescription-system.git
```

Navigate into the project:

```bash
cd voice-prescription-system
```

### 2. Create a Virtual Environment

On Windows:

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file based on `.env.example`.

Example:

```env
DATABASE_URL=your_database_connection_string
```

Do not upload your actual `.env` file to GitHub if it contains passwords, API keys, database credentials, or other secrets.

## ▶️ Running the Backend

Start the FastAPI development server with:

```bash
uvicorn backend.main:app --reload --host 0.0.0.0 --port 8000
```

The backend will be available at:

```text
http://127.0.0.1:8000
```

FastAPI documentation:

```text
http://127.0.0.1:8000/docs
```

Alternative API documentation:

```text
http://127.0.0.1:8000/redoc
```

## 🌐 Running the Frontend

Start the frontend using your preferred local development server.

For example, if using the VS Code Live Server extension, open the frontend entry page and launch it with **Live Server**.

The frontend communicates with the FastAPI backend through the configured API endpoints.

## 🎤 Voice Prescription Workflow

```text
Doctor speaks prescription
          │
          ▼
     Audio Recording
          │
          ▼
   Speech-to-Text Model
          │
          ▼
    Recognized Text
          │
          ▼
     Medicine Search
          │
          ▼
   Fuzzy Medicine Matching
          │
          ▼
    Matching Medicines
          │
          ▼
   Doctor Selects Medicine
          │
          ▼
 Prescription Management
          │
          ▼
    Save Prescription
```

## 🔎 Medicine Search

The system loads the medicine catalog from:

```text
backend/data/medicine.csv
```

The application automatically loads the medicine data when the backend starts.

The medicine search functionality can use fuzzy matching to identify medicines even when the doctor's voice input does not exactly match the stored medicine name.

Example:

```text
Voice Input:
"Panadol"

        ↓

Medicine Search

        ↓

Matching Results

        ↓

Panadol
Panadol Extra
Other Similar Medicines
```

## 📊 Medicine Dataset

The current medicine catalog contains approximately **12,909 medicine records**.

The application detects the medicine-name field from the CSV dataset and uses it for medicine searching.

## 🔐 Security

The project uses environment variables for configuration values that should not be publicly exposed.

Before pushing the project to GitHub, make sure sensitive files are excluded:

```gitignore
.env
__pycache__/
*.pyc
.venv/
venv/
env/
.vscode/
*.log
```

Never commit:

* Database passwords
* API keys
* Secret keys
* Authentication credentials
* Private configuration files

## 🧪 Testing

The system can be tested by verifying:

1. Backend startup.
2. Medicine catalog loading.
3. API availability.
4. Medicine search.
5. Voice recording.
6. Speech-to-text conversion.
7. Medicine matching.
8. Adding medicines to a prescription.
9. Prescription management.
10. Frontend-backend communication.

## 📌 API Documentation

When the backend is running, FastAPI automatically provides interactive API documentation:

```text
http://127.0.0.1:8000/docs
```

This documentation can be used to test available API endpoints.

## 🎯 Project Objectives

The main objectives of the Voice-Based Medicine Prescription Entry System are:

* Reduce manual prescription entry.
* Provide faster medicine searching.
* Support voice-based prescription input.
* Improve medicine identification through fuzzy matching.
* Provide an organized prescription management workflow.
* Integrate frontend and backend healthcare functionality.

## 🔮 Future Improvements

Possible future enhancements include:

* Improved multilingual voice recognition.
* Support for additional medicine attributes.
* Patient profile integration.
* Doctor authentication and role-based access.
* Prescription history.
* PDF prescription generation.
* Digital prescription sharing.
* Advanced medicine recommendations.
* Improved speech recognition in noisy environments.
* Integration with electronic health record systems.

## 👨‍💻 Development

This project was developed as part of an internship/software development project focused on applying **AI, speech recognition, web development, and healthcare information systems**.

## 📄 License

This project currently does not specify a license.

If a license is required for public distribution, an appropriate open-source license can be added later.
****
