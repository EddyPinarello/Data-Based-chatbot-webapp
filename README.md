# README 📝

🎥 Video preview of the MVP

[![Guarda il video](https://img.youtube.com/vi/Dq2FcwWGRtU/maxresdefault.jpg)](https://youtu.be/Dq2FcwWGRtU)

## 📊 Code Coverage

![Coverage](coverage.svg)

🔍 [View Full Coverage Report](https://code7crusaders.github.io/MVP/)

## 🏗 Project Overview

This project is a **React Flask-based web application** that provides API endpoints for handling chat-related functionalities. It is designed to be **lightweight**, **easy to set up**, and **extendable**.

## 🗂 Project Structure

```
MVP/
├── .pytest_cache/
├── .vscode/
├── docs/
├── htmlcov/
├── react-app/
├── SQL/
├── src/
│   └── app/
│       ├── __pycache__/
│       ├── adapters/
│       ├── config/
│       ├── controllers/
│       ├── dependencies/
│       ├── dto/
│       ├── entities/
│       ├── models/
│       ├── ports/
│       ├── repositories/
│       ├── services/
│       ├── uploads/
│       ├── usecases/
│       ├── utils/
│       ├── __init__.py
│       ├── main.py
│       └── __init__.py
│       └── README.md  # 🚀 README for the src/app directory
├── tests/
│   └── README.md  # 🧪 Tests directory (unit and integration)
├── UML/ # Directory for UML diagrams (e.g., using StarUML) 📐
├── venv/
├── .coverage
├── .env
├── .gitignore
├── coverage.svg
├── coverage.xml
├── docker-compose.yml
├── Dockerfile 🐳 # Dockerfile for containerization
├── pytest.ini # Configuration file for pytest
├── README.md      # 📌 Main README for the project
└── requirements.txt # Python dependencies 📦
```


## 🚀 Running the Project Locally

To get the application running on your local machine, follow these steps:

### **Frontend Setup (React)**
1. **Navigate to the React project folder:**  
   ```bash
   cd react-app
   ```
2. **Install dependencies:**  
   ```bash
   npm install
   ```
3. **Start the development server:**  
   ```bash
   npm run dev
   ```
   🖥 The React app will be available at [http://localhost:3000](http://localhost:3000).

### **Backend Setup (Flask)**
1. **Activate the virtual environment:**  
   On macOS/Linux:
   ```bash
   source venv/bin/activate
   ```
   On Windows:
   ```bash
   venv\Scripts\activate
   ```
2. **Install required dependencies:**  
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Flask application:**  
   ```bash
   python main.py
   ```
   🔗 The backend will be accessible at [http://127.0.0.1:5001](http://127.0.0.1:5001).

## 🐳 Running with Docker

If you prefer to use Docker, you can easily spin up the application with:

```bash
docker-compose up --build
```

This command will build the Docker images and start the containers as defined in the `docker-compose.yml` file.

## 🧪 Tests and Code Coverage

To run the tests from the project root path:

```bash
pytest ./tests/
```
To generate an HTML report for code coverage:

```bash
pytest --cov=src/app --cov-report=html
```
Open the htmlcov/index.html file in your browser to view the full report.

📂 This will create an `htmlcov` directory containing a visual report of the test coverage, which you can open in your browser.

## 🔑 Environment Variables

Make sure to configure your `.env` file properly. Add the following variables (remember to replace the placeholder values with your actual secrets and **do not commit the file** to version control):

```
LANGSMITH_TRACING=true
LANGSMITH_ENDPOINT="https://api.smith.langchain.com"
LANGSMITH_PROJECT="Ergon-Assistente-Virtuale-MVP"

OPENAI_API_KEY="your_openai_api_key"

DB_NAME="postgres"
DB_USER="postgres"
DB_PASSWORD="your_database_password"
DB_HOST="localhost"
DB_PORT="5432"

JWT_SECRET_KEY="your_secret_key"
```

