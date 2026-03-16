# Software Development Partner Agent

A walkie-powered AI agent for debugging, code review, and software architecture advice.

## What It Does

The Software Developer helps you:

- **Debug** issues by analyzing error messages and code patterns
- **Review** code for security, performance, and style issues
- **Architect** solutions for complex technical challenges
- **Explain** code, patterns, and concepts

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
walkie hub search dev
```

### Step 3: Chat with the Agent

**Interactive chat:**

```bash
walkie hub chat dev-partner
```

**Single prompt:**

```bash
walkie hub ask dev-partner "Why am getting a TypeError in my JavaScript function?"
```

## API Usage

### Get API Key

```bash
walkie hub key create dev-partner
```

### Direct API Call

```bash
curl -X POST https://prod-api.tenken.co/api/agent/dev-partner \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{
    "prompt": "Why am getting a TypeError: Cannot read property of undefined?"
  }'
```

## Usage Examples

### Example 1: Monolith vs Microservices

```bash
walkie hub ask dev-partner --prompt "We're considering splitting our monolith into microservices. Walk me through when that's the wrong choice."
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/dev-partner \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "We'\''re considering splitting our monolith into microservices. Walk me through when that'\''s the wrong choice."}'
```

### Example 2: Debugging Under Load

```bash
walkie hub ask dev-partner --prompt "My app has latency spikes under load but not in testing. How should I investigate what's actually causing it?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/dev-partner \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "My app has latency spikes under load but not in testing. How should I investigate what'\''s actually causing it?"}'
```

### Example 3: RAG Failure Modes

```bash
walkie hub ask dev-partner --prompt "Our RAG pipeline returns technically relevant documents but the LLM responses are still poor. What failure modes should I look for?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/dev-partner \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Our RAG pipeline returns technically relevant documents but the LLM responses are still poor. What failure modes should I look for?"}'
```

### Example 4: Zero-Downtime Migrations

```bash
walkie hub ask dev-partner --prompt "We need zero-downtime database migrations on a system that's always being written to. What's the safest approach?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/dev-partner \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "We need zero-downtime database migrations on a system that'\''s always being written to. What'\''s the safest approach?"}'
```

### Example 5: Feature Flag Complexity

```bash
walkie hub ask dev-partner --prompt "We use feature flags everywhere and the codebase is getting messy. How do I avoid creating hidden complexity?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/dev-partner \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "We use feature flags everywhere and the codebase is getting messy. How do I avoid creating hidden complexity?"}'
```

## Limitations

- **No file access**: Cannot read or write files
- **No code execution**: Cannot run or test code
- **Session-based memory**: Remembers only within current conversation context

## License

MIT
