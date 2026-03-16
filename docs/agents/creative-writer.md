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

### Example 1: Embodying Feeling Through Objects

```bash
walkie hub ask creative-writer --prompt "How do I anchor grief in physical objects the way Ocean Vuong does, without it feeling decorative?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/creative-writer \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "How do I anchor grief in physical objects the way Ocean Vuong does, without it feeling decorative?"}'
```

### Example 2: Dialogue and Subtext

```bash
walkie hub ask creative-writer --prompt "My dialogue explains too much. How do I build Hemingway-style subtext where the real tension stays beneath the surface?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/creative-writer \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "My dialogue explains too much. How do I build Hemingway-style subtext where the real tension stays beneath the surface?"}'
```

### Example 3: Fix Overwritten Metaphors

```bash
walkie hub ask creative-writer --prompt "My metaphors are overwritten and tangled — how do I fix chains of imagery that compete with each other?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/creative-writer \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "My metaphors are overwritten and tangled — how do I fix chains of imagery that compete with each other?"}'
```

### Example 4: Fragmentation and Lyric Structure

```bash
walkie hub ask creative-writer --prompt "I'm writing a lyric essay and losing control of the associative logic. How do I use fragmentation without losing coherence?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/creative-writer \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "I'\''m writing a lyric essay and losing control of the associative logic. How do I use fragmentation without losing coherence?"}'
```

### Example 5: Endings That Resonate

```bash
walkie hub ask creative-writer --prompt "How do I write an ending that actually resonates instead of just stopping?"
```

```bash
curl -X POST https://prod-api.tenken.co/api/agent/creative-writer \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_CONSUMER_TOKEN" \
  -d '{"prompt": "How do I write an ending that actually resonates instead of just stopping?"}'
```

### Example 6: Interactive Craft Session

```bash
walkie hub chat creative-writer
# Paste your draft and work through revision together
```

## Limitations

- **No file access**: Cannot read or write files
- **No code execution**: Cannot run code or commands
- **Session-based memory**: Remembers only within current conversation context

## License

MIT
