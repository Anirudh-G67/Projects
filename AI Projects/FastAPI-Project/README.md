# FastAPI Project

This project demonstrates API development using FastAPI and Python.

## Technologies
- Python
- FastAPI
- Pydantic
- Uvicorn

## Setup and Usage

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd <project-folder>
```

### 2. Create and Activate a Virtual Environment
```bash
python -m venv venv
```

**Windows:**
```bash
venv\Scripts\activate
```

**Linux/macOS:**
```bash
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install fastapi uvicorn[standard]
```

### 4. Run the Application
Start the FastAPI development server using:
```bash
uvicorn main:app --reload
```

Replace `main` with the name of the Python file containing your FastAPI application, excluding `.py`.

### 5. Access the API
Once the server is running, open these URLs in your browser:

- Root endpoint: `http://127.0.0.1:8000/`
- Get all menu items: `http://127.0.0.1:8000/menu`
- Get a menu item by ID: `http://127.0.0.1:8000/menu/1`
- Filter menu by category: `http://127.0.0.1:8000/menu?category=Masala%20Chai`
- Interactive API documentation (Swagger UI): `http://127.0.0.1:8000/docs`
- Alternative API documentation (ReDoc): `http://127.0.0.1:8000/redoc`

### 6. Example Response
A successful request to `/menu/1` returns:
```json
{
  "id": 1,
  "category": "Masala Chai",
  "price": 20,
  "description": "Classic Indian spiced tea",
  "available": true
}
```

The API returns a `404 Not Found` error when a requested menu item or category does not exist.
