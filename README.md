# 📰 AI-Powered Fake News Detector

An end-to-end AI-powered solution designed to combat online misinformation by classifying news articles as REAL or FAKE.
This system leverages a fine-tuned MobileBERT transformer model for lightweight yet accurate text classification.  

---
👉 **Live Demo**: https://hackathon-frontend1-qhwz.onrender.com/
---

<img src="https://github.com/VishalRaj20/Inspira-Hackathon/blob/0eeb772b1d123ae5f86d8f1d3d01a98a20f7932f/icons/Screenshot%202025-08-23%20140521.png" alt="Frontend App Ui Preview" />

---
## ⚡ Features
- Fake News Detection using MobileBERT (fine-tuned model).
- REST API served via **FastAPI** with CORS enabled.
- Frontend powered by **Vite + Vanilla JS**.
- Chrome Extension support (calls backend API).
- Fake → Corrected factual rewrite using **Google Gemini API**.
- Deployable on **Render.com** or any cloud service.

---

## 📂 Project Structure

project/
│
├── backend/
│ ├── server.py # FastAPI backend
│ ├── requirements.txt # Python dependencies
│ ├── fake_news_detector_mobilebert/ # Fine-tuned model folder
│ │ ├── config.json
│ │ ├── vocab.txt
│ │ ├── special_tokens_map.json
│ │ ├── tokenizer_config.json
│ │ ├── pytorch_model.bin
│
├── frontend/
│ ├── index.html
│ ├── main.js # Frontend logic (calls backend + Gemini API)
│ ├── style.css
│ ├── vite.config.js
│ ├── package.json
│
├── extension/ # Chrome Extension build
│ ├── manifest.json
│ ├── index.html
│ ├── main.js
│ ├── style.css
│
└── README.md

---

## 🔧 Backend Setup (FastAPI)
```bash
### 1️⃣ Create virtual environment

cd backend
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
2️⃣ Install dependencies

pip install -r requirements.txt
3️⃣ Run backend

uvicorn server:app --host 0.0.0.0 --port 8000
Your API is now live at:
👉 http://127.0.0.1:8000

```

🎨 Frontend Setup (Vite + JS)
1️⃣ Install dependencies

cd frontend
npm install
2️⃣ Run locally
npm run dev
Open 👉 http://localhost:5173
```
🧩 Chrome Extension Setup
Go to chrome://extensions/.

Enable Developer Mode.
Click Load unpacked.
Select the extension/ folder.
Extension will appear in your browser.

```
☁️ Deployment on Render

----
Backend
Push your backend code to GitHub.
On Render, create a Web Service.

Build command:
pip install -r requirements.txt

start command:
uvicorn server:app --reload

---
Frontend
Push frontend repo to GitHub.
On Render, create a Static Site.

Build command:
npm install

Run command:
npm run dev
