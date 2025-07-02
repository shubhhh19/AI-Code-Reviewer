# AI Code Reviewer
Checkout the Website: https://ai-code-reviewer-navy.vercel.app/

A full-stack web application for intelligent, context-aware code reviews using AI. Paste or upload your code and receive detailed feedback on bugs, optimizations, best practices, and security concerns.

---

## Features

- **AI-Powered Code Review:** Uses Anthropic Claude for deep, context-aware code analysis.
- **Multi-Language Support:** 20+ programming languages, with automatic detection.
- **Modern UI:** Minimal, responsive React interface with whitespace, large headings, and subtle animations.
- **Code History:** View and revisit past code reviews.
- **Code Explain:** Get brief, AI-generated explanations for code snippets.
- **File Upload & Editor:** Paste code or upload files; syntax highlighting included.

---

## Installation & Run Instructions

### Prerequisites
- **Python 3.11+** (for backend)
- **Node.js 18+** (for frontend)
- **Anthropic Claude API Key** (get from Anthropic)

### 1. Clone the Repository
```bash
git clone https://github.com/shubhhh19/AI-Code-Reviewer.git
cd AI-Code-Reviewer
```

### 2. Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Environment Configuration
Create a `.env` file in `backend/`:
```
CLAUDE_API_KEY=your_anthropic_api_key_here
FLASK_ENV=development
SECRET_KEY=your_secret_key_here
CORS_ORIGINS=*
```

### 4. Frontend Setup
```bash
cd ../frontend
npm install  # or pnpm install
```

### 5. Development Mode
- **Backend:**
  ```bash
  cd backend
  source venv/bin/activate
  python src/main.py
  ```
- **Frontend:**
  ```bash
  cd frontend
  npm run dev
  ```
- Visit: [http://localhost:5173](http://localhost:5173)

### 6. Production Build
```bash
cd frontend
npm run build
cp -r dist/* ../backend/src/static/
cd ../backend
source venv/bin/activate
python src/main.py
```
- Visit: [http://localhost:5001](http://localhost:5001)

---

## Interesting Parts During the Build Process

- **AI Service Integration:**
  - Started with Google Gemini, then Hugging Face (GPT-2, StarCoder, etc.), and finally Anthropic Claude for best results and reliability.
  - Handled model availability, API key management, and error handling for multiple providers.
- **Frontend-Backend Proxying:**
  - Solved CORS and 404 issues by configuring Vite to proxy `/api` requests to Flask backend.
- **UI/UX Polish:**
  - Iteratively improved the UI for whitespace, clarity, and modern feel.
  - Added history, code explain, and clear buttons for better usability.

---

## Difficulties Faced & Solutions

- **AI Model Access:**
  - *Problem:* Many Hugging Face models were unavailable or required payment.
  - *Solution:* Switched to Anthropic Claude, which provided reliable, high-quality code reviews.
- **API Proxying & CORS:**
  - *Problem:* Frontend 404 errors and CORS issues.
  - *Solution:* Configured Vite proxy and Flask CORS settings.
- **Deployment:**
  - *Problem:* Ensuring smooth deployment and environment variable management.
  - *Solution:* Documented clear instructions and tested on multiple platforms.

---

## Screenshots
<img src="https://github.com/user-attachments/assets/fce716c3-69b4-4c7c-91e5-f0321228cb4d" alt="Home Page" width="1000"/>
<img src="https://github.com/user-attachments/assets/f0b5ee0d-893d-4438-a1ae-30417737bdeb" alt="Home Page" width="1000"/>
---

**Built with ❤️ by Shubh Soni. [Portfolio](https://shubhsoni.me)**
