# 🤖 Groq Llama Streamlit Chatbot

A simple and fast **Generative AI chatbot** built using **Streamlit**, **Groq API**, and **Llama 3.3 70B Versatile**.

The application allows users to enter a prompt and generate an AI response using Groq's high-speed inference platform.

## 🚀 Features

* 🤖 AI chatbot powered by Llama 3.3 70B
* ⚡ Fast LLM inference using Groq
* 🎨 Simple and interactive Streamlit UI
* 🔐 API key securely managed using Streamlit Secrets
* 💬 Custom user prompts
* 🌡️ Configurable temperature
* 🔢 Configurable maximum output tokens
* ❌ Basic error handling

## 🛠️ Tech Stack

* **Python**
* **Streamlit**
* **Groq API**
* **Llama 3.3 70B Versatile**

## 📁 Project Structure

```text
groq-llama-streamlit-chatbot/
│
├── app.py
├── requirements.txt
├── README.md
└── .gitignore
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/groq-llama-streamlit-chatbot.git
```

```bash
cd groq-llama-streamlit-chatbot
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows:**

```bash
venv\Scripts\activate
```

**Linux/macOS:**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## 🔑 API Key Configuration

Create the following file:

```text
.streamlit/secrets.toml
```

Add your Groq API key:

```toml
GROQ_API_KEY = "your_groq_api_key"
```

> ⚠️ Never upload your API key or `.streamlit/secrets.toml` to GitHub.

Add this to `.gitignore`:

```text
.streamlit/secrets.toml
venv/
__pycache__/
.env
```

## ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

The application will open in your browser.

## 🧠 How It Works

The application follows a simple LLM pipeline:

```text
User
  │
  ▼
Streamlit UI
  │
  ▼
User Prompt
  │
  ▼
Groq API
  │
  ▼
Llama 3.3 70B
  │
  ▼
Generated Response
  │
  ▼
Streamlit UI
```

### Model Configuration

The chatbot uses:

```python
model="llama-3.3-70b-versatile"
```

The model receives two messages:

* **System message** → Defines the assistant's behavior
* **User message** → Contains the user's prompt

The generated response is then extracted from the API response and displayed in the Streamlit application.

## 📦 requirements.txt

```text
streamlit
groq
```

## 🌐 Deployment

This application can be deployed using **Streamlit Community Cloud**.

Basic deployment steps:

1. Push the project to GitHub.
2. Open Streamlit Community Cloud.
3. Connect your GitHub repository.
4. Select `app.py` as the main file.
5. Add `GROQ_API_KEY` under Streamlit Secrets.
6. Deploy the application.

## 🔐 Security

API keys should **never** be hardcoded in your Python source code.

Instead of:

```python
api_key = "gsk_xxxxxxxxx"
```

use:

```python
api_key = st.secrets["GROQ_API_KEY"]
```

This keeps your API credentials separate from your source code.

## 🔮 Future Improvements

Possible improvements for this project:

* 💬 Chat history
* 🧠 Conversation memory
* 📡 Streaming responses
* ⚡ Response latency measurement
* 💰 Token/cost tracking
* 🗂️ Conversation management
* 🎛️ Model and temperature selection
* 🔄 Retry mechanism for API failures
* 🚀 Production deployment
* 📊 LLM observability and monitoring
* 💾 Redis-based response caching

## 🎯 Learning Objectives

This project demonstrates the fundamentals of building an LLM application:

* Calling an LLM through an API
* Working with system and user prompts
* Using Groq for fast inference
* Building a UI with Streamlit
* Managing API secrets
* Handling API exceptions
* Deploying a GenAI application

## 👨‍💻 Author

**Shreeshail Goura**

Generative AI Engineer | AI/ML | LLMs | RAG | Agentic AI

---

⭐ If you found this project useful, consider giving the repository a star!
