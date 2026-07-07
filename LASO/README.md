# LASO - Service Locator Application

This is the unified codebase for **LASO** (Sri Lanka's Service Locator Application). The project has been restructured to cleanly separate backend logic, the SQLite database layer, and the mobile-first frontend.

---

## Directory Structure

```
LASO/
├── backend/
│   ├── app.py                      # Flask Integration Server
│   ├── test_integration.py         # Integration test suite
│   ├── requirements.txt            # Unified Python dependencies
│   ├── location_service/           # GPS, maps, proximity and search functions
│   ├── rating_system/              # Rating models and calculations
│   └── user_communication/         # User validation & chat messaging logic
│
├── database/
│   ├── database.py                 # SQLite database schema & operations
│   ├── laso_app.db                 # SQLite database file
│   └── view_database.py            # SQLite database inspector tool
│
└── frontend/
    ├── index.html                  # Main application landing page
    ├── assets/                     # Graphical assets
    ├── js/                         # Frontend business logic & API clients
    ├── pages/                      # Client-side views (auth, chat, search, profiles)
    ├── styles/                     # CSS stylesheets
    └── README.md                   # Frontend-specific documentation
```

---

## Getting Started

### 1. Setup Backend Dependencies
Navigate to the `backend/` directory and install the required dependencies:
```bash
pip install -r backend/requirements.txt
```

### 2. Run the Backend Server
Start the Flask web server:
```bash
python backend/app.py
```
The server will start running at `http://localhost:8000`.

### 3. Inspect the Database
You can inspect the database tables and review sample data using the inspector utility:
```bash
python database/view_database.py
```

### 4. Run the Integration Tests
To run the automated suite verifying the database, location search, and user registration/communication:
```bash
python backend/test_integration.py
```

### 5. Launch the Frontend
The frontend can be loaded directly from the `frontend/` directory. Since it uses ES modules, it should be served via an HTTP server. See [frontend/README.md](file:///C:/Users/Azaam/.gemini/antigravity/scratch/LASO/frontend/README.md) for detailed serving options (e.g. Live Server or Python `http.server`).