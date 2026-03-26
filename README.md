# Welcome Email Skill

A skill for Claude that guides you through a structured conversation and generates a high-converting welcome email for your business, newsletter, or product.

## What it does

The skill acts as an email strategist. It runs a 9-question discovery interview (one question at a time, always with examples), then produces an annotated welcome email under 200 words.

**Discovery phases:**

1. **Context** - What they signed up for, what your business does
2. **Audience** - Who your subscribers are, what they expect
3. **Voice** - Your brand's tone, optional writing sample to match
4. **Content** - What to expect going forward, immediate win, personal touch

**Output:**

- Subject line
- Greeting + acknowledgment
- Expectation setting
- Immediate win (with link placeholder)
- Human touch
- Single call-to-action
- Sign-off with reply question
- Inline annotations explaining why each section works

The email adapts based on signup type: newsletter, product purchase, free trial, course enrollment, waitlist, or community.

## Installation

### Claude Code (CLI, IDE extensions, or web)

From your project directory:

```bash
claude mcp add welcome-email -- npx -y @anthropic-ai/claude-code-mcp-skill --skill-path /path/to/welcome-email/Skill.md
```

Replace `/path/to/welcome-email/Skill.md` with the actual path where you cloned this repo.

### Claude Desktop

1. Download `Claude Desktop/welcome-email.zip` from this repo
2. Drag and drop the zip file onto the Claude Desktop window

That's it. The skill is now available in your conversations.

## Usage

Once installed, just ask Claude to help you write a welcome email:

> "I need a welcome email for my newsletter"

> "Help me write a welcome email for new signups"

Claude will walk you through the discovery questions, show you a summary for confirmation, then generate the annotated draft. You can iterate on any section before getting the final copy-ready version.

## How it works

The skill file (`welcome-email/Skill.md`) is a structured prompt that teaches Claude a specific workflow. It defines:

- The exact questions to ask and in what order
- Rules for adapting to different signup types
- Writing constraints (no em dashes, no generic filler, under 200 words)
- A two-stage output: annotated draft for review, then clean copy for pasting

You can read the full skill in [`welcome-email/Skill.md`](welcome-email/Skill.md) and modify it to suit your needs.

## License

MIT License. See [LICENSE](LICENSE) for details.
