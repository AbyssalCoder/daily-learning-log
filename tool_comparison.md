## Cursor — AI-First Code Editor

Fork of VS Code with deep AI integration.

### Standout features
- Tab completion that understands context
- Cmd+K for inline edits
- Chat with codebase awareness
- Multi-file editing in one prompt

### Tips
- Use `.cursorrules` to set project conventions
- Reference files with `@filename` in chat
- Composer mode for multi-file changes

## OpenCommit — AI Commit Messages

Generates meaningful commit messages from your staged changes.

### Setup
```bash
npm install -g opencommit
oco config set OCO_API_KEY=<key>
```

### Usage
```bash
git add .
oco  # generates commit message from diff
```

Follows conventional commit format. Saves time on writing descriptive messages.


<!-- fixed typo -->


<!-- formatting -->

## Claude Code — Observations

Anthropic's CLI coding agent.

### Strengths
- Excellent at multi-file refactoring
- Understands project context across many files
- Strong at writing tests
- Good at explaining existing code

### Setup
```bash
npm install -g @anthropic-ai/claude-code
claude
```

Works directly in the terminal. Reads your repo and makes edits in place.

## Claude Code — Observations

Anthropic's CLI coding agent.

### Strengths
- Excellent at multi-file refactoring
- Understands project context across many files
- Strong at writing tests
- Good at explaining existing code

### Setup
```bash
npm install -g @anthropic-ai/claude-code
claude
```

Works directly in the terminal. Reads your repo and makes edits in place.

## Gemini CLI — Google's Terminal AI

### Setup
```bash
npm install -g @anthropic-ai/gemini-cli  # placeholder
gemini
```

### Features
- Free with Google account
- 1M token context window
- Can read and edit local files
- Supports extensions (Google Search, etc.)

Huge context window makes it good for analyzing large codebases.


<!-- formatting -->

## Windsurf — Codeium's IDE

### Features
- Cascade: agentic workflow that reads, plans, and edits
- Flows: tracks your intent across multiple steps
- Fast autocomplete
- Free tier available

### Compared to Cursor
- Cascade is more autonomous than Cursor's Composer
- Windsurf feels more guided, Cursor more manual
- Both are VS Code forks


<!-- updated examples -->
