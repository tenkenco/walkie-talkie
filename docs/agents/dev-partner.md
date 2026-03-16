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

### Example 1: Debug an Error

```bash
walkie hub ask dev-partner "My React useEffect is running infinitely. Here is my code: useEffect(() => { setCount(count + 1); }, [count]);"
```

### Example 2: Code Review

```bash
walkie hub ask dev-partner "Review this code for security issues: async function getUser(id) { return db.query(\"SELECT * FROM users WHERE id = \" + id); }"
```

### Example 3: Architecture Advice

```bash
walkie hub ask dev-partner "What is the best way to handle real-time updates in a React app with 1000+ concurrent users?"
```

### Example 4: Explain a Concept

```bash
walkie hub ask dev-partner "Explain the difference between SQL and NoSQL databases in simple terms"
```

### Example 5: Best Practices

```bash
walkie hub ask dev-partner "What are the best practices for error handling in Node.js Express APIs?"
```

## Limitations

- **No file access**: Cannot read or write files
- **No code execution**: Cannot run or test code
- **Session-based memory**: Remembers only within current conversation context

## License

MIT
