# 🗣️ Language Learning Chatbot using Gemini and MongoDB

This project is a terminal-based language learning chatbot powered by Google's Gemini API. It allows users to practice a target language while tracking their mistakes to improve over time. Mistakes and corrections are stored in MongoDB, enabling personalized learning and feedback.

---

## 📌 Features

- 🔤 Learn a new language by chatting with a Gemini-powered AI tutor.
- 🧠 Logs and stores mistakes with corrections in a MongoDB collection.
- ⚙️ Supports dynamic model selection from available Gemini models.
- 📊 Summarizes past mistakes for user review and learning.
- 💬 Terminal-based interactive chatbot experience.

---

## 🧱 System Architecture

```
[User Terminal]
     ↓
[Python App] 
     ↙            ↘
[Google Gemini]    [MongoDB]
     ↓                  ↑
[AI Responses] ← [Stores mistakes]
```

---

## 🛠️ Technologies Used

- **Python**
- **Google Generative AI (Gemini API)**
- **MongoDB (via PyMongo)**
- **dotenv (to load environment variables)**

---

## 🚀 How to Run

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/language-chatbot.git
cd language-chatbot
```

2. **Install dependencies**

```bash
pip install google-generativeai pymongo python-dotenv
```

3. **Set environment variables**

Create a `.env` file in the root directory and add:

```
GOOGLE_API_KEY=your_gemini_api_key
MONGO_URI=your_mongodb_uri
```

4. **Run the chatbot**

```bash
python chatbot.py
```

---

## 📋 Example Flow

```bash
What language do you know? python
What language do you want to learn? java
What is your proficiency level (beginner/intermediate/advanced)? beginner

Using model: gemini-1.5-flash

[java] You: what is java
Bot: Java is a high-level, class-based, object-oriented programming language...

[java] You: how to declare variable in java
Bot: You might have meant: int x = 5; instead of "declare variable in java".

[java] You: exit

Summary of mistakes:
You said: how to declare variable in java, Correction: You might have meant: int x = 5;
```

---

## 📦 Database Structure

- **Database Name**: `mistakes`
- **Collection**: `mistakes`
- **Sample Document**:
```json
{
  "user_input": "how to declare variable in java",
  "correction": "You might have meant: int x = 5;"
}
```

---

## 📽️ Demo Video

A demo screen-recording is included in the submission folder, explaining:
- Project architecture
- Code structure
- Demo of chatbot interaction
- Mistake tracking logic

---

## 📄 License

This project is open-source and free to use for learning purposes.
