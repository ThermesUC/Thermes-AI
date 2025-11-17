# 💻 Thermes: Terminal-Style AI Chatbot

<img width="1760" height="985" alt="ThermesAI" src="https://github.com/user-attachments/assets/0c1f6ea2-f128-4e9e-82b3-04d842a4af00" />
<div align="center">

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-%23412991.svg?style=for-the-badge&logo=openai&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

**A specialized conversational AI agent wrapped in a nostalgic Command Line Interface (CLI).**
**Developed for the Accenture UC 2024 Hackathon.**

</div>

---

## 📖 Overview

**Thermes** represents a fusion of retro aesthetics and modern artificial intelligence. Created by a team of freshman Computer Science students in a 3-day Hackathon sprint, this project challenges the traditional chatbot interface.

Instead of a standard chat bubble UI, Thermes simulates a functioning **Operating System Terminal**, offering an immersive environment where users can query complex information regarding **AI Regulations (Chile & EU)**. The system leverages a curated knowledge base to provide accurate, context-aware responses.

## Key Features

* **Specialized Knowledge Base:** Trained specifically on Chilean AI strategic plans and European Union AI regulations using RAG (Retrieval-Augmented Generation) principles.
* **Immersive Terminal UI:**
    * Custom CSS styling mimicking a dark-mode OS shell.
    * Typewriter-style prompt interactions (`>>>`).
    * Hidden visual easter eggs (Dropdown menu in the header).
* **Dynamic Backend:** Powered by **Flask**, enabling real-time communication between the retro frontend and the OpenAI API.
* **Robust Context Handling:** Utilizes multiple data sources (`data.txt` files) to ground answers in reality and reduce hallucinations.

## Technical Implementation

The project follows a client-server architecture designed for speed and simplicity.

### The Stack
* **Frontend:** Native **HTML5** and **CSS3** for the visual shell. **Vanilla JavaScript** manages the DOM, event listeners for keypresses, and asynchronous `fetch` requests to the API.
* **Backend:** A **Python Flask** server acts as the controller. It receives user input, processes context from the local text corpus (`data.txt`, `data1.txt`, etc.), and queries the LLM.
* **AI Engine:** Integration with **OpenAI**, customized with specific system prompts to maintain the persona and accuracy of the bot.

### How it Works
1.  **Input:** User types a command/question into the styled `<input>` field.
2.  **Request:** JS captures the `Enter` event and sends a POST request to `/chat`.
3.  **Processing:** The Python server retrieves relevant context from the text files.
4.  **Response:** The generated answer is sent back as JSON and appended to the DOM with a typewriter styling (`> Response`).

## 📂 Project Structure

```text
/
├── app.py              # Flask application entry point & route logic
├── data.txt            # Knowledge base corpus
├── README.md           # Project documentation
├── templates/
│   └── index.html      # Main HTML structure for the terminal interface
└── static/
    ├── css/
    │   └── style.css   # Custom styling, themes, and animations
    ├── js/
    │   └── script.js   # Frontend logic and API communication
    └── images/         # Assets (Wallpapers, icons)
````

## 👥 The Team

Built with 💻 and ☕ by:

  * **Diego Anton** - [GitHub](https://github.com/dianAnton)
  * **Jose Pedro Barraza** - [GitHub](https://github.com/ElZapallo432)
  * **Sebastian Besoaín**
  * **Vicente Cuitiño**
  * **Julian Murguia**
  * **Farid Seminario**
