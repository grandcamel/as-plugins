# Grandcamel Plugins Marketplace

Claude Code marketplace consolidating plugins for P2P development, enterprise integrations, and developer productivity.

## Project Structure

```
grandcamel-plugins/
├── .claude-plugin/
│   └── marketplace.json         # Marketplace manifest
├── plugins/
│   └── <plugin-name>/           # Individual plugins
│       ├── plugin.json          # Plugin metadata
│       ├── skills/              # Plugin skills
│       ├── commands/            # Slash commands
│       ├── agents/              # Autonomous agents
│       └── hooks/               # Event handlers
├── VERSION
├── README.md
├── CLAUDE.md
└── LICENSE
```

## Development Guidelines

### Versioning

- **Marketplace version**: In `VERSION` and `.claude-plugin/marketplace.json` → `metadata.version`
- **Plugin versions**: In each `plugins/<name>/plugin.json` → `version` and marketplace `plugins[].version`
- **Format**: Semantic versioning (MAJOR.MINOR.PATCH)

### Adding a New Plugin

1. Create `plugins/<plugin-name>/` directory
2. Add `plugin.json` with required fields:
   ```json
   {
     "name": "plugin-name",
     "version": "1.0.0",
     "description": "What the plugin does"
   }
   ```
3. Add components (skills/, commands/, agents/)
4. Register in `.claude-plugin/marketplace.json` → `plugins[]`
5. Update README.md

### Commit Messages

Use conventional commits:
- `feat(<plugin>):` - New features
- `fix(<plugin>):` - Bug fixes
- `docs(<plugin>):` - Documentation
- `refactor(<plugin>):` - Code restructuring
- `chore:` - Maintenance tasks

### Testing

```bash
# Test entire marketplace
claude --plugin-dir ./

# Test individual plugin
claude --plugin-dir ./plugins/<plugin-name>
```

### Python Plugins

Plugins with Python dependencies:
- jira-assistant-skills → jira-assistant-skills-lib (PyPI)
- confluence-assistant-skills → confluence-assistant-skills-lib (PyPI)
- splunk-assistant-skills → splunk-assistant-skills-lib (PyPI)
- notebooklm → patchright (browser automation)

Each plugin maintains its own `requirements.txt`.

## Plugin Categories

| Category | Plugins |
|----------|---------|
| development | holepunch, assistant-skills, best-practices, apds-dev, wiredove |
| productivity | jira-assistant-skills, confluence-assistant-skills, splunk-assistant-skills, notebooklm |
| developer-tools | anproto, pearpass |
