# hospitle_api
# Hospital Patient Management API

A REST API built with **Flask** and **SQLite** to manage hospital patients.

---
##  Architecture

```
hospital-api/
│
├── hospitle.py        # Main Flask application (routes & logic)
├── hospital.db        # SQLite database (auto-created on first run)
└── README.md          # Project documentation
```

### Tech Stack
| Layer    | Technology        |
|----------|-------------------|
| Backend  | Python + Flask    |
| Database | SQLite3           |
| API Type | REST API          |

### How It Works
```
Client (Postman / Browser)
        ↓  HTTP Request
    Flask App (hospitle.py)
        ↓  SQL Query
    SQLite Database (hospital.db)
        ↓  JSON Response
Client receives data
```

---

## 🚀 How To Run This Project

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/hospital-api.git
cd hospital-api
```

### 2. Create Virtual Environment
```bash
python -m venv venv

# On Windows:
venv\Scripts\activate

# On Mac/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install flask
```

### 4. Run the App
```bash
python hospitle.py
```

### 5. Open in Browser or Postman
```
http://127.0.0.1:5000
```

---

## API Endpoints

| Method | Endpoint        | Description         |
|--------|-----------------|---------------------|
| GET    | `/`             | Check API is running |
| POST   | `/add_patient`  | Add a new patient   |
| GET    | `/patients`     | Get all patients    |

### POST `/add_patient` — Example Request Body
```json
{
  "id": 1,
  "name": "Maheen",
  "age": 20,
  "disease": "Fever"
}
```

### GET `/patients` — Example Response
```json
[
  {
    "id": 1,
    "name": "Maheen",
    "age": 20,
    "disease": "Fever"
  }
]
```

---

## Database

- Database: **SQLite** (no setup needed, auto-created)
- File: `hospital.db`
- Table: `patients`

| Column  | Type    |
|---------|---------|
| id      | INTEGER (Primary Key) |
| name    | TEXT    |
| age     | INTEGER |
| disease | TEXT    |

---

##  Author
- **Maheen**
- GitHub: m9544998@gmail.com
