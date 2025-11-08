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

