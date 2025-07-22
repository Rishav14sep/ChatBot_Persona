 🧠 AI Assistant Agent with Tool Use (OpenAI + Function Calling)

 This project is a simple command-line chatbot powered by OpenAI's GPT-4 model that can reason through multi-step tasks and use external tools like weather lookup and system command execution to fulfill user queries.
It follows the Start, Plan, Action, Observe methodology, using structured reasoning before taking actions.

🚀 Features
✅ Uses OpenAI GPT-4 (Function Calling) with JSON structured output

✅ Supports tool invocation through structured planning

✅ Tools included:

get_weather(city: str): Fetches weather data from wttr.in

run_command(cmd: str): Executes shell commands

✅ Follows a clear reasoning framework:

Plan → Select tool → Act → Observe → Respond

🛠️ Tech Stack
Python 3.10+

OpenAI GPT-4.1

LangChain-style planning logic (manually implemented)

Function Calling with response_format={"type": "json_object"}

External tools:

requests (weather API)

os.system (command runner)

📁 Project Structure
text
Copy
Edit
📦 AI_Assistant
 ┣ 📜 main.py         # Main chatbot script
 ┣ 📜 .env            # Contains your OpenAI API key
⚙️ Setup Instructions
Clone the repository (if applicable):

bash
Copy
Edit
git clone https://github.com/yourname/ai-assistant-agent.git
cd ai-assistant-agent
Create a .env file:

Save your OpenAI API key:

ini
Copy
Edit
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Note: For security, avoid hardcoding your API key in the script.

Install dependencies:

bash
Copy
Edit
pip install openai python-dotenv requests
Run the script:

bash
Copy
Edit
python main.py
🧠 Example Usage
pgsql
Copy
Edit
> What is the weather in New York?

🧠: The user is interested in weather data of New York
🧠: From the available tools I should call get_weather
🛠️: Calling Tool: get_weather with input new york
🤖: The weather in New York is Partly cloudy +27°C.
📌 Notes
The code uses response_format={"type": "json_object"} for function-style structured responses.

Make sure your OpenAI API plan supports GPT-4 with function calling.

The weather tool is a free endpoint (wttr.in) and may throttle or fail under heavy usage.

🧩 To Do / Improvements
Add error handling for API failures

Add more tools like:

Web scraping

Wikipedia search

File read/write

Convert to web app or add GUI

Use subprocess instead of os.system for safer command execution

🔒 Security Warning
Never hardcode your API key in code, especially when sharing or publishing. Always load it from environment variables or a secure vault.

📜 License
This project is for educational/demo purposes. Customize and expand based on your use case.

Let me know if you'd like this turned into a Markdown file (README.md), or want to turn it into a proper open-source GitHub repo with MIT License and contribution guidelines.









Ask ChatGPT

