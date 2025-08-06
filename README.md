# ✉️ EMAIL REPLY GENERATOR & EXTENSION

An intelligent email reply generator that offers instant responses to emails in **three tones**: **Professional**, **Casual**, and **Friendly**. It’s designed to enhance productivity by integrating seamlessly into your email workflow with a **Chrome Extension**, **React Frontend**, and a **Spring Boot Backend**.

---

## 📁 Project Structure

### 1. `email-writer-react` – Frontend
- Built using **React.js**.
- Communicates with the backend to fetch generated email replies.
- Provides a user-friendly dialog interface for selecting tone and previewing responses.

### 2. `email-writer-sb` – Backend
- Built using **Spring Boot**.
- Handles the email content processing and generates contextual replies using AI (e.g., OpenAI or other APIs).
- Exposes REST APIs to interact with the frontend and Chrome extension.

### 3. `email-writer-ext` – Chrome Extension
- **Manifest V3** based extension.
- Injects a custom reply interface into the Gmail compose window.
- Includes:
  - `manifest.json`: Defines permissions, content scripts, and extension metadata.
  - `content.js`: Injects UI and handles interaction with the Gmail DOM.
  - Connects with the backend to retrieve replies based on email content.

---

## 💡 Features

- Auto-detects the email body and suggests replies.
- Generates 3 different tone-based responses:
  - 🎩 Professional
  - 🙂 Friendly
  - 😎 Casual
- Easy-to-use popup inside Gmail.
- Fast and efficient with API-backed response generation.

---

## 🖼️ Project Screenshots

### 🕶️ Before Generating Reply

![Without Reply](./assets/screenshot-no-reply.png)

---

### 💬 After Generating Replies (Different Tones)

**Professional**
![Professional Reply](./assets/screenshot-professional.png)

**Casual**
![Casual Reply](./assets/screenshot-casual.png)

**Friendly**
![Friendly Reply](./assets/screenshot-friendly.png)

---

## 🚀 Installation Guide

Clone the Repository

```bash

git clone https://github.com/your-username/email-reply-generator.git
cd email-reply-generator
```
Set Up Frontend (email-writer-react)

```bash

cd email-writer-react
npm install
npm start
```
✅ Make sure the backend is running and the API URL is correctly set in the frontend.

Set Up Backend (email-writer-sb)

```bash

cd ../email-writer-sb
./mvnw spring-boot:run   # For Mac/Linux
# OR
mvn spring-boot:run      # For Windows
Load Chrome Extension (email-writer-ext)
```

Open Chrome and go to chrome://extensions/

Enable Developer Mode

Click Load Unpacked

Select the email-writer-ext folder

Reload Gmail to see the extension in action

🛠️ Tech Stack
React.js – Frontend

Spring Boot – Backend

Chrome Extension (Manifest V3) – Browser Integration

REST APIs – Communication between frontend, backend, and extension

HTML / CSS / JavaScript – Extension logic and interface
