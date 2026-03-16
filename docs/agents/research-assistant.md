# Research Assistant Agent

A walkie-powered AI agent for research, web search, and synthesizing information from multiple sources.

## What It Does

The Research Assistant helps you:

- **Search the web** for current information on any topic
- **Synthesize findings** from multiple sources into coherent summaries
- **Recall past research** from your session history
- **Cross-validate claims** by checking multiple sources

## Quick Start

### Step 1: Install & Sign Up

```bash
npm i -g @tenken/walkie-cli
walkie auth signup
walkie auth login
```

### Step 2: Find the Agent

```bash
walkie hub browse
# or search for it
walkie hub search research
```

### Step 3: Chat with the Agent

**Interactive chat:**

```bash
walkie hub chat research-assistant
```

**Single prompt:**

```bash
walkie hub ask research-assistant "What are the latest developments in AI agents in 2026?"
```

## API Usage

### Get API Key

```bash
walkie hub key create research-assistant
```

### Direct API Call

```bash
curl -X POST https://prod-api.tenken.co/api/agent/research-assistant \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{
    "prompt": "What are the latest developments in AI agents in 2026?"
  }'
```

## Usage Examples

### Example 1: Current Events Research

```bash
walkie hub ask research-assistant "What is the current state of quantum computing in 2026?"
```

### Example 2: Synthesize Topic

```bash
walkie hub ask research-assistant "Give me a summary of the best practices for building RAG systems in 2026"
```

### Example 3: Compare Options

```bash
walkie hub ask research-assistant "Compare Claude vs Gemini vs GPT for enterprise use cases"
```

### Example 4: Interactive Chat

```bash
walkie hub chat research-assistant
# Then type your questions interactively
```

## Limitations

- **No file access**: Cannot read or write files
- **No code execution**: Cannot run code or commands
- **Session-based memory**: Remembers only within current conversation context
- **Web search limited**: Uses search API with rate limits

## License

MIT
