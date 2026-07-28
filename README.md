# 📅 AI-Powered Event Management System

An intelligent CLI-based event management system powered by OpenAI and MongoDB. This application simplifies event creation for organizers through conversational AI and provides attendees with a clear, instant Q&A assistant to get accurate event details without confusion.

---

## 💡 Key Problem Solved

Communication between event organizers and attendees is often fragmented or unclear, leading to repeated questions and confusion. 

This application solves that problem by allowing attendees to query event details in **natural language**. Instead of digging through long documents or confusing emails, attendees interact with an AI assistant that provides fast, precise, and contextual answers about the event.

---

## ✨ Features

### 🛠️ For Organizers (`organizer.py`)
* **Interactive Account System:** Secure authentication via username and password, with support for new account registration.
* **Conversational Event Creation:** The organizer answers ~10 natural language prompts from an AI chatbot to automatically compile and structure event details.
* **Smart Event Editing:** Modify existing event details using natural language commands processed via the OpenAI API.
* **Simple Event Deletion:** Quick event removal via indexed numerical selection.
* **Attendee Management:** Easily invite attendees to specific events using their usernames.

### 👥 For Attendees (`attendee.py`)
* **Natural Language Q&A:** Ask questions about registered events in plain English (e.g., *"What time does the keynote start?"* or *"Is lunch provided?"*).
* **Instant Clarification:** Powered by OpenAI to convert complex MongoDB event records into clear, human-friendly responses.

---

## 🏗️ Architecture & Tech Stack

* **Language:** Python 3.x
* **AI/LLM Processing:** OpenAI API (GPT models for natural language parsing and Q&A)
* **Database:** MongoDB (Stores user credentials, event metadata, and attendee lists)
* **Interface:** Terminal / CLI

---

## 🚀 Getting Started

### 🛠️ Prerequisites

Make sure you have the following installed on your machine:
* **Python 3.8+**
* **Git**
* An active **OpenAI API Key**

---

### 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/your-repo-name.git](https://github.com/yourusername/your-repo-name.git)
   cd your-repo-name
   ```

2. **Create and activate a virtual environment:**

      **macOS / Linux:**
      ```bash
      python3 -m venv venv
      source venv/bin/activate
      ```

      **Windows:**
      ```bash
      python -m venv venv
      .\venv\Scripts\activate
      ```

4. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Configure Environment Variables:**
   Copy the example environment file to create your own local `.env` file:

   **macOS / Linux:**
     ```bash
     cp .env.example .env
     ```
   **Windows:**
     ```cmd
     copy .env.example .env
     ```

7. **Add your API Key:**
   Open the newly created `.env` file in your editor and insert your actual OpenAI API key:
   ```text
   API_KEY=your_actual_openai_api_key_here
   ```

---

### 💻 Running the Application

Once the virtual environment is active and your `.env` file is configured, you can run either script:

* **For Attendees:**
  ```bash
  python attendee.py
  ```

* **For Organizers:**
  ```bash
  python organizer.py
  ```

---

### 📦 Project Structure

```text
.
├── attendee.py         # Main CLI application for event attendees
├── organizer.py        # Main CLI application for event organizers
├── requirements.txt    # Python package dependencies
├── .env.example        # Environment variable template
└── .gitignore          # Files ignored by Git
```
