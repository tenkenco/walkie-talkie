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

### Example 1: Founder Agreement Terms

```bash
walkie hub ask legal-counsel --prompt "What are the key terms in a founder agreement that prevent expensive disputes down the road?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/legal-counsel \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "What are the key terms in a founder agreement that prevent expensive disputes down the road?"}'
```

### Example 2: Copyright vs Patent

```bash
walkie hub ask legal-counsel --prompt "What's the practical difference between copyright and patent protection for a software company?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/legal-counsel \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "What'\''s the practical difference between copyright and patent protection for a software company?"}'
```

### Example 3: SaaS Contract Clauses

```bash
walkie hub ask legal-counsel --prompt "Which SaaS contract clauses actually matter and which are just boilerplate to negotiate away?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/legal-counsel \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "Which SaaS contract clauses actually matter and which are just boilerplate to negotiate away?"}'
```

### Example 4: Employee vs Contractor Classification

```bash
walkie hub ask legal-counsel --prompt "How do I think about employee vs contractor classification risk as we scale our team?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/legal-counsel \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "How do I think about employee vs contractor classification risk as we scale our team?"}'
```

### Example 5: Open Source Licensing Risk

```bash
walkie hub ask legal-counsel --prompt "What open source licensing issues can create hidden commercialization risk for a startup?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/legal-counsel \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "What open source licensing issues can create hidden commercialization risk for a startup?"}'
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
