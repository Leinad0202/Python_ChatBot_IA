# Python_ChatBot_IA
Python_ChatBot_IA is a simple and functional chatbot built with Python and Streamlit. It connects to the OpenAI API to handle real-time natural language conversations. The app is lightweight and requires only two Python libraries: streamlit and openai.

⚠️ Security Note: The API key is not hardcoded in the source code. It is loaded from an environment variable named OPENAI_API_KEY, following OpenAI's best practices for key management.

# Features
Interactive Chat Interface: Built with Streamlit for a clean and easy-to-use web UI.

OpenAI-Powered Responses: Uses OpenAI’s models (e.g., GPT-3.5, GPT-4) to respond to user input.

Secure API Key Handling: The key is loaded from an environment variable, not stored in the code.

Minimal Dependencies: Only requires streamlit and openai, making setup fast and simple.

Lightweight and Extensible: The code is clean and easy to modify — ideal for adding new features like model selection, temperature control, or streaming outputs.

# Prerequisites
Python 3.8 or higher

pip (Python package manager)

OpenAI API Key — Get it from your OpenAI dashboard

(Optional) python-dotenv — Useful for loading environment variables from a .env file.

# Installation
Clone the repository:

bash
Copiar
Editar
git clone https://github.com/your-username/Python_ChatBot_IA.git
cd Python_ChatBot_IA
Install required packages:

bash
Copiar
Editar
pip install streamlit openai
(Optional) Install python-dotenv if you want to use a .env file for your API key:

bash
Copiar
Editar
pip install python-dotenv
🔐 API Key Configuration
Create a .env file in the root directory:

ini
Copiar
Editar
OPENAI_API_KEY=sk-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Make sure to add .env to your .gitignore file:

txt
Copiar
Editar
.env
Load the key in your code (in main.py):

python
Copiar
Editar
import os
from dotenv import load_dotenv

load_dotenv()
openai.api_key = os.getenv("OPENAI_API_KEY")
This setup ensures your API key is safe and not exposed in version control.

# Running the Chatbot
Run the app with Streamlit:

bash
Copiar
Editar
streamlit run main.py
Then open your browser and go to http://localhost:8501.

You’ll see a chat interface where you can type messages and receive AI-powered responses.
