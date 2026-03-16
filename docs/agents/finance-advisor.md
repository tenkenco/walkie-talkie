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

### Example 1: Market Research

```bash
walkie hub ask finance-advisor "What is the current state of cryptocurrency markets in 2026?"
```

### Example 2: Investment Analysis

```bash
walkie hub ask finance-advisor "What are the pros and cons of investing in index funds vs ETFs?"
```

### Example 3: Retirement Planning

```bash
walkie hub ask finance-advisor "I am 30 years old making $100k/year. How much should I save for retirement?"
```

### Example 4: Budget Planning

```bash
walkie hub ask finance-advisor "What is the 50/30/20 budgeting rule and how do I apply it?"
```

### Example 5: Concept Explanation

```bash
walkie hub ask finance-advisor "Explain compound interest in simple terms"
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
