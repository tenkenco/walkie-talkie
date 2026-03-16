# Finance Advisor Agent

A walkie-powered AI agent for financial research, analysis, and planning guidance.

## What It Does

The Finance Advisor helps you:

- **Research** current market conditions and investment options
- **Analyze** financial situations and recommend strategies
- **Plan** budgets, savings, and investment approaches
- **Explain** financial concepts in plain language

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
walkie hub search finance
```

### Step 3: Chat with the Agent

**Interactive chat:**

```bash
walkie hub chat finance-advisor
```

**Single prompt:**

```bash
walkie hub ask finance-advisor "What are the current trends in bond yields in 2026?"
```

## API Usage

### Get API Key

```bash
walkie hub key create finance-advisor
```

### Direct API Call

```bash
curl -X POST https://prod-api.tenken.co/api/agent/finance-advisor \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{
    "prompt": "What are the current trends in bond yields in 2026?"
  }'
```

## Usage Examples

### Example 1: Diversification Theory

```bash
walkie hub ask finance-advisor --prompt "Why does diversification actually reduce risk — isn't it just averaging down returns?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/finance-advisor \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Why does diversification actually reduce risk — isn'\''t it just averaging down returns?"}'
```

### Example 2: Sequence-of-Returns Risk

```bash
walkie hub ask finance-advisor --prompt "How does sequence-of-returns risk work and why does it matter so much in the early years of retirement?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/finance-advisor \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "How does sequence-of-returns risk work and why does it matter so much in the early years of retirement?"}'
```

### Example 3: Understanding Duration

```bash
walkie hub ask finance-advisor --prompt "Explain what bond duration means for a portfolio without the jargon overload."
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/finance-advisor \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Explain what bond duration means for a portfolio without the jargon overload."}'
```

### Example 4: Reading Startup Unit Economics

```bash
walkie hub ask finance-advisor --prompt "Walk me through how to read a startup's unit economics critically — what should I be skeptical of?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/finance-advisor \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Walk me through how to read a startup'\''s unit economics critically — what should I be skeptical of?"}'
```

### Example 5: Venture Power Law

```bash
walkie hub ask finance-advisor --prompt "Why do venture returns follow a power law, and what does that mean for how VCs think about portfolio construction?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/finance-advisor \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Why do venture returns follow a power law, and what does that mean for how VCs think about portfolio construction?"}'
```

## Important Disclaimer

**This agent provides general financial information only, not personalized financial advice.** Always consult with a qualified financial advisor for investment decisions.

## Limitations

- **No file access**: Cannot read or write files
- **No real-time data**: Provides research-based information, not live market data
- **Session-based memory**: Remembers only within current conversation context
- **Not financial advice**: General information only, consult professionals

## License

MIT
