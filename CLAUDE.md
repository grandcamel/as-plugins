# AS-Plugins (Assistant Skills) Marketplace

Claude Code marketplace for Assistant Skills plugins using GitHub sources.

## Project Structure

```
as-plugins/
├── .claude-plugin/
│   └── marketplace.json      # Marketplace manifest
├── VERSION
├── README.md
└── CLAUDE.md
```

## Key Concept: GitHub Sources

Plugins are referenced via GitHub sources in marketplace.json (no local submodules):

```json
{
  "name": "jira-assistant-skills",
  "source": {
    "source": "github",
    "repo": "grandcamel/JIRA-Assistant-Skills"
  }
}
```

Users install plugins directly from GitHub without needing to clone this repo.

## Plugin Repositories

| Plugin | Repository |
|--------|------------|
| jira-assistant-skills | grandcamel/JIRA-Assistant-Skills |
| confluence-assistant-skills | grandcamel/Confluence-Assistant-Skills |
| splunk-assistant-skills | grandcamel/Splunk-Assistant-Skills |
| assistant-skills | grandcamel/Assistant-Skills |

## Development Guidelines

### Adding a Plugin

Add entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "new-plugin",
  "source": {
    "source": "github",
    "repo": "grandcamel/New-Plugin"
  },
  "description": "Plugin description",
  "version": "1.0.0",
  "category": "productivity",
  "keywords": ["keyword1", "keyword2"]
}
```

### Updating Versions

When a plugin has a new release, update its version in marketplace.json.

### Commit Messages

Use conventional commits:
- `chore(<plugin>): bump version to X.Y.Z`
- `feat: add <plugin> plugin`
- `docs:` - Documentation changes

## Testing

```bash
# Test marketplace locally
claude --plugin-dir ./

# Add marketplace
/plugin marketplace add grandcamel/as-plugins
```
