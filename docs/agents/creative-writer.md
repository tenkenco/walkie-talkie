# Creative Writing Agent

A walkie-powered AI agent for brainstorming, drafting, and editing creative content.

## What It Does

The Creative Writer helps you:

- **Brainstorm** ideas, outlines, and concepts
- **Draft** blog posts, emails, stories, and marketing copy
- **Edit** existing content for clarity, tone, and style
- **Adapt** writing for different audiences and formats

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
walkie hub search creative
```

### Step 3: Chat with the Agent

**Interactive chat:**

```bash
walkie hub chat creative-writer
```

**Single prompt:**

```bash
walkie hub ask creative-writer "Help me brainstorm 5 blog post ideas about AI in 2026"
```

## API Usage

### Get API Key

```bash
walkie hub key create creative-writer
```

### Direct API Call

```bash
curl -X POST https://prod-api.tenken.co/api/agent/creative-writer \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{
    "prompt": "Help me brainstorm 5 blog post ideas about AI in 2026"
  }'
```

## Usage Examples

### Example 1: Brainstorm Ideas

```bash
walkie hub ask creative-writer "Give me 10 creative campaign ideas for a sustainable fashion brand"
```

### Example 2: Draft Content

```bash
walkie hub ask creative-writer "Write a professional cold email to a potential client in the fintech space"
```

### Example 3: Edit/Improve

```bash
walkie hub ask creative-writer "Improve this paragraph: We offer the best solutions for businesses. Our team is experienced and can help you succeed."
```

### Example 4: Adapt Tone

```bash
walkie hub ask creative-writer "Rewrite this for LinkedIn: Check out our new product! It is awesome and you should buy it!"
```

### Example 5: Interactive Chat

```bash
walkie hub chat creative-writer
# Then collaborate on writing projects
```

## Limitations

- **No file access**: Cannot read or write files
- **No code execution**: Cannot run code or commands
- **Session-based memory**: Remembers only within current conversation context

## License

MIT
