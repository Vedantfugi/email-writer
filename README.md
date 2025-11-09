# ✉️ Email Writer Assistant

An **AI-powered Email Reply Generator** that helps you instantly craft professional responses — either through a **Chrome Extension inside Gmail** or a **standalone web app** built with React (Vite).  
Powered by **Google Gemini API** and a **Spring Boot backend**.

---

## 🧩 Overview

**Email Writer Assistant** is a full-stack AI project with three connected parts:

| Module | Description |
|--------|--------------|
| 🧠 **Backend (Spring Boot)** | Connects to the Gemini API, processes prompts, and returns AI-generated replies. |
| 🌐 **Frontend (React + Vite)** | A simple UI to paste an email, select tone, and generate a reply instantly. |
| 🧩 **Chrome Extension** | Adds an **AI Reply** button inside Gmail that fetches the response and inserts it automatically. |

---

## 🛠️ Tech Stack

### 🧱 Backend
- **Java 17+ / Spring Boot**
- **Spring WebFlux (WebClient)** for async Gemini API calls
- **Jackson** for JSON parsing
- **Google Gemini API (Generative Language model)**

### 🌐 Frontend
- **React (Vite)**
- **Material UI (MUI)** components
- **Axios** for API calls
- **Clipboard API** for copying replies

### 🧩 Chrome Extension
- **JavaScript (ES6)** content script
- **Chrome Extensions API (Manifest V3)**
- **Gmail DOM integration**

---

## ⚙️ How It Works

1️⃣ **Frontend or Extension** sends the email text + tone → to backend  
2️⃣ **Backend** creates a structured prompt and requests Gemini API  
3️⃣ **Gemini API** returns a context-aware reply  
4️⃣ **Extension** inserts it directly into Gmail, or **Frontend** displays it on the page  

How to setup locally:

🧩 1. Prerequisites

Make sure you have these installed:

Java 17+ (for Spring Boot backend)

Maven (or use the included mvnw wrapper)

Node.js 16+ & npm (for frontend)

Google Gemini API key → get it free from Google AI Studio

Google Chrome (for the extension)

⚙️ 2. Run the Backend (Spring Boot)

Open the backend/ folder in your IDE (like IntelliJ or VS Code).

In src/main/resources/application.properties, add your Gemini API details:
server.port=8080
gemini.api.key=YOUR_GEMINI_API_KEY
gemini.api.url=https://generativelanguage.googleapis.com

Run the application using Maven or your IDE:./mvnw spring-boot:run


The backend should now be running at:👉 http://localhost:8080

💻 3. Run the Frontend (React + Vite)

Open a new terminal and navigate to the frontend/ folder.

Install dependencies:npm install

Start the development server:npm run dev
Open the local URL shown in the terminal (usually http://localhost:5173/).

Enter an email in the text box, select a tone (optional), and click Generate Reply.
The app will connect to your local backend to generate a response.

📬 4. Load the Chrome Extension

Open Google Chrome and go to:chrome://extensions/

Turn Developer mode ON (top-right corner).

Click Load unpacked and select the extension/ folder from this project.

Open Gmail and click Compose — you’ll see a new AI Reply button in the toolbar.

When clicked, it sends your email content to the local backend (http://localhost:8080) and pastes the AI-generated reply automatically. 💬

🧠 5. Quick Test (Optional)

You can also test the backend directly with a curl command:

curl -X POST http://localhost:8080/api/email/generate \
-H "Content-Type: application/json" \
-d '{"emailContent":"Hey, can you send the report by Friday?","tone":"professional"}'


✅ You should receive a JSON response with the generated reply from Gemini.

⚡ 6. Coming Soon

🌐 Hosted live version (no local setup needed)

🧠 Response Quality Scoring (AI-powered evaluation)

📝 Detailed video tutorial setup
