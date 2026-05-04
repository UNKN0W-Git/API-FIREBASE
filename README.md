Mika Chatbot
A chatbot application built with Streamlit (frontend) and FastAPI (backend), using Firebase for authentication, Firestore for data storage, and Ollama for AI model.

## 🚀 Features
* Lightweight chat UI
* **User authorization before chatting** (Google OAuth + Firebase)
* **Save and load chat data** (Firestore)
* Stores chat history in session state
* Powered by local AI model via Ollama

## 🧰 Requirements
* Python 3.10+
* Ollama (with llama3.2:1b model)
* Firebase project (Authentication + Firestore)
* Google OAuth credentials

## 🎥 Video Demo
[Link video demo]([(https://drive.google.com/drive/u/0/folders/1jZ98gEsScT6e2BU7ukLzAqhMOVVuEUd2)])

## ⚙️ Installation
### 1. Clone repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO

### 2. Create virtual environment
python -m venv venv
venv\Scripts\activate

### 3. Install dependencies
pip install -r requirements.txt

### 4. Configure secrets
Create file .streamlit/secrets.toml (see secrets.example.toml for structure)

### 5. Install and run Ollama
Download Ollama from https://ollama.com/download
ollama pull llama3.2:1b

## 🖥️ Run Backend

cd chatbot-page-main
venv\Scripts\activate
python -m uvicorn backend.app.main:app --reload --port 8000

Check: http://localhost:8000/health

## 🌐 Run Frontend

Open a new terminal:
cd chatbot-page-main
venv\Scripts\activate
python -m streamlit run frontend/app.py

Open: http://localhost:8501

## 🛠️ Project Structure
chatbot-page-main/
├── .streamlit/
│   └── secrets.toml
├── backend/
│   └── app/
│       ├── core/
│       ├── routers/
│       ├── schemas/
│       ├── services/
│       └── main.py
├── frontend/
│   └── app.py
└── requirements.txt
