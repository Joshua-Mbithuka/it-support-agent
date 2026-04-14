# 🤖 IT Support AI Agent

An autonomous AI-powered IT support agent built with **n8n** that handles customer support requests, searches for solutions on the web, and automatically creates support tickets in **Freshservice** when escalation is needed.

---

## 🧠 How It Works

The agent receives messages through the n8n chat interface, intelligently searches Google for solutions, and either resolves the issue or escalates it to a human agent by creating a Freshservice ticket — all without any manual intervention.

```
Customer Message (n8n Chat)
          ↓
     AI Agent (Claude)
     ├── 🔍 search_web tool → Google (SerpAPI)
     └── 🎫 create_ticket tool → Freshservice
          ↓
    Response to Customer
```

---

## ✨ Key Features

- **Conversational AI** — Understands natural language support requests
- **Web Search** — Searches Google in real time for IT solutions via SerpAPI
- **Smart Escalation** — Asks the customer before raising a ticket
- **Auto Ticket Creation** — Creates a fully detailed Freshservice ticket with AI-written description
- **Memory** — Remembers conversation context across multiple messages
- **Professional Responses** — Claude writes polished, human-like replies

---

## 🛠️ Built With

| Tool | Role |
|------|------|
| [n8n](https://n8n.io) | Workflow automation engine |
| [Claude (Anthropic)](https://anthropic.com) | AI conversation & decision making |
| [SerpAPI](https://serpapi.com) | Real-time Google search |
| [Freshservice](https://freshservice.com) | IT service desk & ticket management |
| [Railway](https://railway.app) | Cloud hosting (24/7) |

---

## ⚙️ Setup & Installation

### Prerequisites
- n8n instance (local or hosted on Railway)
- Anthropic API key
- SerpAPI key (free tier: 100 searches/month)
- Freshservice account with API key

### Steps

**1. Clone this repo**
```bash
git clone https://github.com/YOUR_USERNAME/it-support-agent.git
```

**2. Import the workflow into n8n**
- Open your n8n instance
- Click **"New Workflow"** → **"..."** → **"Import from file"**
- Upload `it-support-agent.json`

**3. Add your credentials**

| Credential | Where to get it |
|---|---|
| Anthropic API key | [console.anthropic.com](https://console.anthropic.com) |
| SerpAPI key | [serpapi.com](https://serpapi.com) |
| Freshservice API key | Freshservice Profile Settings |

**4. Update placeholders in the workflow**

| Placeholder | Replace with |
|---|---|
| `{Add Your company}` | Your company name |
| `[YourDomain]` | Your Freshservice domain |
| `{Your Group ID}` | Your Freshservice group ID |

**5. Activate the workflow**
- Toggle **Activate** in the top right corner ✅
