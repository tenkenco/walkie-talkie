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

### Example 1: Systematic Literature Review

```bash
walkie hub ask research-assistant --prompt "Walk me through how to conduct a literature review that's actually systematic, not just a collection of papers I found."
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/research-assistant \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Walk me through how to conduct a literature review that'\''s actually systematic, not just a collection of papers I found."}'
```

### Example 2: Interpreting P-Values

```bash
walkie hub ask research-assistant --prompt "What does a p-value tell me and what does it absolutely not tell me?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/research-assistant \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "What does a p-value tell me and what does it absolutely not tell me?"}'
```

### Example 3: Causal vs Correlational Claims

```bash
walkie hub ask research-assistant --prompt "How do researchers distinguish between causal claims and strong correlations? How do I evaluate that in a paper I'm reading?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/research-assistant \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "How do researchers distinguish between causal claims and strong correlations? How do I evaluate that in a paper I'\''m reading?"}'
```

### Example 4: Difference-in-Differences Validity

```bash
walkie hub ask research-assistant --prompt "Our study uses a difference-in-differences design. What makes that credible or weak?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/research-assistant \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Our study uses a difference-in-differences design. What makes that credible or weak?"}'
```

### Example 5: Reading Research Critically

```bash
walkie hub ask research-assistant --prompt "What did the replication crisis actually reveal about how to read published research?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/research-assistant \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "What did the replication crisis actually reveal about how to read published research?"}'
```

### Example 6: Interactive Research Session

```bash
walkie hub chat research-assistant
# Work through a paper or methodology question together
```

## Limitations

- **No file access**: Cannot read or write files
- **No code execution**: Cannot run code or commands
- **Session-based memory**: Remembers only within current conversation context
- **Web search limited**: Uses search API with rate limits

## License

MIT
