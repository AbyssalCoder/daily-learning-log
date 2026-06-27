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
