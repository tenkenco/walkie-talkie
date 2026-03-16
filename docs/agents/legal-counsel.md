# Legal Counsel Agent

A walkie-powered AI agent for legal research, analysis, and compliance guidance.

## What It Does

The Legal Counsel helps you:

- **Research** legal topics, regulations, and case precedents
- **Analyze** legal issues and explain implications
- **Explain** legal concepts in plain language
- **Compliance** guidance for common regulations

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
walkie hub search legal
```

### Step 3: Chat with the Agent

**Interactive chat:**

```bash
walkie hub chat legal-counsel
```

**Single prompt:**

```bash
walkie hub ask legal-counsel "What are the key GDPR requirements for US companies?"
```

## API Usage

### Get API Key

```bash
walkie hub key create legal-counsel
```

### Direct API Call

```bash
curl -X POST https://prod-api.tenken.co/api/agent/legal-counsel \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{
    "prompt": "What are the key GDPR requirements for US companies?"
  }'
```

## Usage Examples

### Example 1: Regulatory Research

```bash
walkie hub ask legal-counsel "What are the key GDPR requirements for US companies handling EU customer data?"
```

### Example 2: Contract Basics

```bash
walkie hub ask legal-counsel "What are the essential elements of a valid contract?"
```

### Example 3: Compliance Checklist

```bash
walkie hub ask legal-counsel "What should a startup include in their terms of service?"
```

### Example 4: Explain Legal Concept

```bash
walkie hub ask legal-counsel "Explain the difference between trademark, copyright, and patent in simple terms"
```

### Example 5: Risk Analysis

```bash
walkie hub ask legal-counsel "What are the legal risks of using open source software in a commercial product?"
```

## Important Disclaimer

**This agent provides general legal information only, not legal advice.** For specific legal matters, always consult with a qualified attorney in your jurisdiction.

## Limitations

- **No file access**: Cannot read or write files
- **Not legal advice**: General information only, consult attorneys
- **Jurisdiction limitations**: Laws vary by country/state
- **Session-based memory**: Remembers only within current conversation context

## License

MIT
