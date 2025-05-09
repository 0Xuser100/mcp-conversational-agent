# 🌟 MCP-Driven Conversational Agent: The Ultimate AI Tool-Using Chatbot 🌟

Welcome to the **MCP-Driven Conversational Agent** project! This repository demonstrates how to build a powerful, memory-enabled AI assistant that can interact with real-world tools and services using the [MCP-Use](https://github.com/mcp-use/mcp-use) framework, [LangChain](https://python.langchain.com/), and modern LLMs.

> **Note:** This project requires both **Python** and **Node.js** (for running MCP tool servers like Playwright, Airbnb, DuckDuckGo, etc.).

---

## 🚀 Project Overview

This project showcases an end-to-end example of a conversational AI agent that:
- Uses **MCP-Use** to connect to multiple tool servers (web browsing, Airbnb, DuckDuckGo, and more)
- Leverages **LangChain** for LLM integration (e.g., Groq, OpenAI, Anthropic)
- Maintains **conversation memory** for contextual, multi-turn interactions
- Can be easily extended to new tools and LLMs

---

## ✨ Features
- **Conversational Memory:** Remembers previous messages for smarter, more natural conversations
- **Multi-Tool Access:** Search the web, browse Airbnb, and more via MCP servers
- **Configurable:** Easily switch or add new MCP servers via a JSON config
- **Modern LLM Support:** Works with Groq, OpenAI, Anthropic, and any LangChain-compatible model
- **Interactive CLI:** Chat with your agent in the terminal

---

## 🗂️ Project Structure

```
├── Main.py                # Main script: interactive chat agent
├── browser_mcp.json     # MCP server configuration file
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation (this file)
```

---

## ⚡ Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/0Xuser100/mcp-conversational-agent.git
cd mcp-conversational-agent
```

### 2. Install Node.js (Required for MCP Servers)
Download and install Node.js (LTS version) from [nodejs.org](https://nodejs.org/).
After installation, verify:
```bash
node -v
npm -v
```

### 3. Install Python Dependencies
```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables
Create a `.env` file in the project root and add your LLM API keys (e.g., for Groq, OpenAI, Anthropic):
```
GROQ_API_KEY=your_groq_api_key
```

### 5. Configure MCP Servers
Edit `browser_mcp.json` to specify which MCP servers you want to use (Playwright for web, Airbnb, DuckDuckGo, etc.). Example:
```
{
  "mcpServers": {
    "airbnb": {
      "command": "npx",
      "args": ["-y", "@openbnb/mcp-server-airbnb", "--ignore-robots-txt"]
    },
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    },
    "duckduckgo-search": {
      "command": "npx",
      "args": ["-y", "duckduckgo-mcp-server"]
    }
  }
}
```

### 6. Run the Chat Agent
```bash
python Main.py
```

---

## 🧑‍💻 Usage
- Type your message and press Enter to chat with the agent
- Type `clear` to reset the conversation memory
- Type `exit` or `quit` to end the session

## 🧪 Testing the Search Tools

You can test the agent's ability to use different search tools (web, Airbnb, DuckDuckGo, etc.) by entering natural language queries in the chat. Here are some example queries to try:

### 1. Web Search (Playwright/Google)
- `Search for the latest news about AI.`
- `Find the official website for the Eiffel Tower.`

### 2. Airbnb Search
- `Show me hotel listings in Egypt.`
- `Find a place to stay in Barcelona for 2 adults in August.`

### 3. DuckDuckGo Search
- `Search DuckDuckGo for Python tutorials.`
- `Find privacy-focused search engines.`

### How to Test
1. Start the agent with `python Main.py`.
2. Type any of the example queries above (or your own) and press Enter.
3. The agent will use the appropriate tool/server to answer your query.

> **Tip:** You can mix and match queries, and the agent will remember context if you ask follow-up questions!

---

## 🛠️ How It Works
- The agent loads your MCP server config and API keys
- It connects to the specified MCP servers (web, Airbnb, etc.)
- It uses a modern LLM (via LangChain) to interpret your queries and decide which tools to use
- Conversation memory is maintained for context-aware responses

---

## 🔌 Extending the Project
- Add new MCP servers by editing `browser_mcp.json`
- Swap LLMs by changing the model in `Main.py`
- Integrate new tools or APIs supported by MCP-Use and LangChain

---

## 🤝 Contributing
Pull requests and issues are welcome! To contribute:
1. Fork the repo
2. Create a new branch
3. Make your changes
4. Submit a pull request

---

## 📄 License
This project is licensed under the MIT License.

---

## 🙏 Acknowledgments
- [MCP-Use](https://github.com/mcp-use/mcp-use) for the unified agent/server framework
- [LangChain](https://python.langchain.com/) for LLM integration
- [Playwright MCP](https://github.com/microsoft/playwright-mcp) and [OpenBNB MCP](https://github.com/openbnb/mcp-server-airbnb) for tool servers

---

## 🌐 Learn More
- [MCP-Use Documentation](https://mcp-use.io/)
- [LangChain Documentation](https://python.langchain.com/)
- [Playwright MCP](https://github.com/microsoft/playwright-mcp)
- [OpenBNB MCP](https://github.com/openbnb/mcp-server-airbnb)

---

> **Build your own AI agent that can use real-world tools, search the web, and more — all with just a few lines of code!** 
