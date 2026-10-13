# AI Project Manager — n8n Automation

An AI-powered Project Management Assistant built with **n8n** that integrates AI agents with productivity tools to streamline project-related tasks through natural-language interactions.

The system connects email, calendar, structured data, and web search capabilities through a unified Telegram interface.

## Overview

The AI Project Manager interprets user requests, selects relevant tools, and executes actions across connected services. It is designed to be extensible, allowing additional integrations and capabilities to be introduced as the project evolves.

## Features

- **AI-Powered Assistance:** Uses AI models to understand requests and determine appropriate actions.
- **Email Management:** Retrieves emails and sends messages through Gmail.
- **Calendar Management:** Retrieves calendar events and creates new events.
- **Data Management:** Searches, retrieves, creates, and updates Airtable records.
- **Web Search:** Retrieves relevant information using SerpAPI.
- **Telegram Interface:** Enables users to interact with the assistant through conversational messages.
- **Conversational Memory:** Maintains context across interactions using n8n Simple Memory.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow orchestration and automation |
| Google Gemini | AI language model integration |
| Groq | Alternative AI model integration |
| Telegram Bot API | Conversational user interface |
| Gmail | Email operations |
| Google Calendar | Calendar and event management |
| Airtable | Structured data and record management |
| SerpAPI | Web search |
| Simple Memory | Conversational context |

## Workflow Architecture

The system follows an AI-agent-based architecture:

1. **Input:** The user sends a message through Telegram.
2. **Request Processing:** The AI Agent interprets the request and identifies the required action.
3. **Tool Selection:** The agent selects an appropriate connected tool based on the request.
4. **Execution:** The selected integration performs the relevant operation.
5. **Response:** The result is returned to the user through Telegram.

```text
User
  |
  v
Telegram Trigger
  |
  v
AI Agent <----> AI Models
  |             Simple Memory
  |
  +---- Gmail
  +---- Google Calendar
  +---- Airtable
  +---- SerpAPI
  |
  v
Telegram Response
```

## Integrations

### Gmail
- Retrieve email messages.
- Send email messages.

### Google Calendar
- Retrieve calendar events.
- Create new calendar events.

### Airtable
- Search for records.
- Retrieve individual records.
- Create new records.
- Update existing records.

### SerpAPI
- Perform web searches to retrieve relevant information.

### Telegram
- Receive user requests.
- Deliver the assistant's responses.

## Setup

### Prerequisites

- An installed n8n instance.
- A Telegram bot created through BotFather.
- Credentials for the AI model provider you intend to use.
- Connected Gmail and Google Calendar accounts.
- An Airtable account and configured API credentials.
- A SerpAPI API key.

### Configuration

1. Create a new workflow in n8n.
2. Add a Telegram Trigger node to receive incoming messages.
3. Configure an AI Agent node with an appropriate system prompt.
4. Connect an AI model, such as Google Gemini or Groq.
5. Add Simple Memory to support conversational context.
6. Configure the Gmail, Google Calendar, Airtable, and SerpAPI tools.
7. Connect the AI Agent output to a Telegram message node.
8. Configure credentials and test each integration.
9. Activate or publish the workflow according to your n8n setup.

**Security note:** Store API keys and service credentials in n8n credentials. Never commit secrets, access tokens, or private configuration files to GitHub.

## Potential Improvements

- Add task creation, assignment, and status tracking.
- Introduce project deadlines and priority management.
- Add confirmation steps before sensitive actions.
- Improve error handling and tool execution validation.
- Integrate additional productivity platforms.
- Implement persistent conversation storage for long-term context.

## Project Goals

This project explores practical applications of AI agents and workflow automation by connecting multiple services into a unified assistant. It also provides hands-on experience with API integrations, tool calling, conversational AI, and workflow orchestration.

## Acknowledgments

Developed as part of my learning journey with the **Digital Egypt Pioneers Initiative (DEPI)**.

Special thanks to [Alaa El-Dewer](https://www.linkedin.com/in/alaa-eldewer/) for his guidance.

## Author

**Abdelrahman Mohamed Attia**

- LinkedIn: [abdelrhman-mohamed-attia](https://www.linkedin.com/in/abdelrhman-mohamed-attia-47059822b/)
- GitHub: [Alpha2005elhagary](https://github.com/Alpha2005elhagary)

---

*Built with n8n, AI agents, and workflow automation.*
