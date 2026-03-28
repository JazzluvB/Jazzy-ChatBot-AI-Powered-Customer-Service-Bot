# Jazzy ChatBot-AI-Powered Customer Service Bot

Conversational AI chatbot built for a digital content editing agency. The bot helps potential clients explore services, get package recommendations, and connect with a human advisor when needed — all through a custom web interface.

---

## About the Project

This project was built as a complete client-facing chatbot for **Jazzy Creative Studio**, an agency specializing in video and photo editing for creators and brands.

The main goal was to automate the first point of contact with potential clients — answering questions, recommending the right service package, and escalating to a human agent on Discord when the conversation required it.

---

## Features

- Understands and responds to questions about video and photo editing services
- Recommends packages (Basic, Intermediate, Professional) based on client needs
- Detects when a client wants to speak with a human and shares the Discord contact
- Responds in the same language the user writes in (Spanish or English)
- Retains conversation context within each session using memory
- Displays a rating screen at the end of each conversation
- Clean, custom web UI built from scratch based on a Figma design

---

## Tech Stack

- **n8n** — workflow automation and conversation flow logic
- **OpenAI GPT** — language model powering the AI responses
- **HTML / CSS / JavaScript** — custom frontend interface
- **Discord** — human escalation channel
- **Google Docs** — knowledge base connected to the AI agent
- **Figma** — UI design reference
- **Vercel** — deployment

---

## How It Works

The conversation flow runs entirely on n8n. When a user sends a message through the web interface, it hits a webhook that triggers the AI Agent node. The agent uses OpenAI GPT with a custom system prompt, has access to a Google Docs knowledge base, and can escalate to Discord when the client requests a human.

The frontend is a single HTML file with three screens: an initial screen with an idle robot, an active chat screen, and a post-conversation rating screen.

---

## Project Structure

```
jozzy-chatbot/
├── index.html       Main web interface
└── README.md        Project documentation
```

---

## Getting Started

Clone the repository and open `index.html` in your browser, or deploy it directly to Vercel.

Before running, update the webhook URL inside `index.html`:

```js
const WEBHOOK = 'https://your-instance.app.n8n.cloud/webhook/your-id/chat';
```

Make sure your n8n workflow is active (Published) before testing.

---

## Deployment

The frontend is a single static file and can be deployed to any static hosting platform. Vercel is recommended for its simplicity — just drag and drop the file and you get a live public URL instantly.

---

## What I Learned

This was my first end-to-end AI automation project. I learned how to design and configure multi-node workflows in n8n, write effective system prompts for AI agents, connect external tools like Google Docs and Discord to a live workflow, and build a custom chat UI from scratch without relying on pre-built components.

---

## Contact

Built by a freelance developer for Jozzy Creative Studio.

For service inquiries or collaboration: [discord.gg/7d25e2nS](https://discord.gg/7d25e2nS)
