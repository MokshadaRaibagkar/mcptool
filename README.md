# 🌦️ MCP Weather Alert Agent

A lightweight AI agent powered by [MCP (Modular Connector Protocol)](https://github.com/modelcontextprotocol/specification) that fetches **real-time weather alerts** for any U.S. state using the [National Weather Service API](https://www.weather.gov/documentation/services-web-api).


---

## ✨ Features

- 🤖 **AI Chat Interface** - Interactive conversation with memory
- 🌪️ **Real-time Weather Alerts** - Live data from National Weather Service
- ⚡ **Fast Inference** - Powered by Groq LLM via LangChain
- 🔧 **MCP Integration** - Built with `mcp`, `mcp-use`, and `FastMCP`
- 🛠️ **Tool-based Architecture** - Structured function calling

---

## 🎯 Quick Example

```bash
💬 User: "Provide me weather alerts for California"
🤖 Agent: Calling get_alerts("CA")...
🌦️ Result: "FLOOD WARNING for Central Valley until 6 PM PST..."
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Groq API key ([Get one here](https://console.groq.com/))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/MokshadaRaibagkar/mcp-weather-alert-agent.git
   cd mcp-weather-alert-agent
   ```

2. **Create virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env
   # Edit .env and add your GROQ_API_KEY
   ```

---

## 🛠️ Usage

### Option 1: Interactive Chat Agent
```bash
uv run server/client.py
```

### Option 2: MCP Dev Server (for testing)
```bash
uv run mcp dev server/weather.py
```
Opens MCP Inspector for tool testing and debugging.

### Option 3: MCP Inspector (Visual Interface)
```bash
uv run mcp dev server/weather.py
```

---

## 🔧 API Reference

### `get_alerts(state: str) -> str`

Fetches active weather alerts for a U.S. state.

**Parameters:**
- `state` (str): Two-letter state code (e.g., "CA", "TX", "NY")

**Returns:**
- Formatted string with current weather alerts or "No active alerts"

**Example:**
```python
result = get_alerts("FL")
# Returns: "HURRICANE WARNING for Miami-Dade County..."
```

---


## 🧪 Example Interactions

```
Weather Alert Agent initialized! Ask me about weather alerts.

💬 You: What are the current weather alerts for Texas?
🛠️ Calling get_alerts with state: TX
🌦️ Current alerts for Texas:
- TORNADO WATCH for East Texas until 10 PM CDT
- FLASH FLOOD WARNING for Austin area until midnight

💬 You: Any alerts in California?
🛠️ Calling get_alerts with state: CA
✅ No active weather alerts for California at this time.
```

---

## 🌐 Tech Stack

| Component | Technology |
|-----------|------------|
| **MCP Framework** | [MCP Protocol](https://github.com/modelcontextprotocol/specification) |
| **LLM** | [Groq](https://groq.com/) |
| **Agent Framework** | [LangChain](https://langchain.com/) |
| **Weather API** | [National Weather Service](https://www.weather.gov/documentation/services-web-api) |
| **Development** | [FastMCP](https://github.com/jlowin/fastmcp) |

---

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---


## 👩‍💻 Author

**Mokshada Raibagkar**

- [Github](https://github.com/MokshadaRaibagkar)
- [LinkedIn](https://linkedin.com/in/mokshada-raibagkar)

---

<div align="center">

**⭐ Star this repo if it helped you!**

Made with ❤️ and ☕

</div>