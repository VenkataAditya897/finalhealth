
# Healthcare Assistant Flask App

A Flask-based healthcare assistant application featuring user authentication, health data tracking, AI-powered symptom analysis chatbot, voice input support, and reminder management. The app uses MongoDB for data storage and integrates LangChain + ChatGroq for medical advice generation.

## Features

- User sign-up and sign-in with password hashing.
- Dashboard displaying health data and averages.
- Add health reports via OCR and manual health data entry.
- AI chatbot for symptom analysis using LangChain and ChatGroq.
- Voice input to convert speech to text.
- Reminders with repeat options and alarm sounds.
- Conversation history storage and management.
- Responsive web UI with Flask templates.
- Background scheduler for reminder checking.
- Docker-friendly setup.

---

## Prerequisites

- Python 3.10
- MongoDB running locally or accessible remotely
- `pip` package manager

---

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/yourrepo.git
   cd yourrepo/doctorproj
   ```

2. **Create and activate a virtual environment (recommended):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Ensure MongoDB is running locally or update the MongoDB URI in `app.py` if using remote DB.**

---

## Configuration

- Update `app.secret_key` in `app.py` with a secure random key for session security.
- Configure your Groq API key in `app.py` (replace the placeholder key with your own).
- Ensure the vectorstore index file `vectorstore_med_part2.index` is present or create it according to your data.

---

## Running the Application

```bash
python app.py
```

By default, Flask runs on [http://127.0.0.1:5000](http://127.0.0.1:5000).

Open this URL in your browser to access the app.

---

## Usage

- Sign up for a new user account.
- Sign in to access your dashboard.
- Add health data manually or upload reports.
- Use the AI chatbot for symptom analysis.
- Set reminders with optional repeat frequencies.
- Manage your reminders and clear chat history.

---

## Notes

- Alarm sounds use `pygame` for playback. Make sure your environment supports audio playback.
- Background scheduler runs every minute to check and trigger reminders.
- Voice input uses Google Speech Recognition API; requires internet access.
- Chatbot uses LangChain with Groq API — usage limits may apply.

---

## Contact

For questions or support, please contact venkataaditya897@gmail.com
