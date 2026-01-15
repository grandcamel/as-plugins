# Grandcamel Plugins

A Claude Code marketplace providing plugins for P2P development, enterprise integrations, and developer productivity.

## Installation

### From GitHub

```bash
# In Claude Code:
# "Install grandcamel-plugins from github:grandcamel/grandcamel-plugins"
```

### Manual Installation

```bash
git clone https://github.com/grandcamel/grandcamel-plugins.git
claude --plugin-dir ./grandcamel-plugins
```

## Plugins

### P2P Development

| Plugin | Description |
|--------|-------------|
| **holepunch** | Build zero-infrastructure P2P applications with Holepunch ecosystem (Pear, Hypercore, Hyperswarm) |
| **apds-dev** | APDS Personal Data Server development support |
| **anproto** | ANProto ed25519 keypair management and message signing |
| **pearpass** | PearPass password manager development support |
| **wiredove** | Wiredove decentralized social networking development |

### Enterprise Integrations

| Plugin | Description |
|--------|-------------|
| **jira-assistant-skills** | 18 specialized skills for JIRA automation |
| **confluence-assistant-skills** | 14 skills for Confluence Cloud automation |
| **splunk-assistant-skills** | 17 skills for Splunk search and administration |

### Developer Productivity

| Plugin | Description |
|--------|-------------|
| **assistant-skills** | Complete toolkit for building Claude Code skills |
| **best-practices** | Development best practices for git, Docker, and Claude Code |
| **notebooklm** | Query Google NotebookLM for source-grounded answers |

## Project Structure

```
grandcamel-plugins/
├── .claude-plugin/
│   └── marketplace.json
├── plugins/
│   ├── holepunch/
│   ├── jira-assistant-skills/
│   ├── confluence-assistant-skills/
│   ├── splunk-assistant-skills/
│   ├── assistant-skills/
│   ├── best-practices/
│   ├── apds-dev/
│   ├── anproto/
│   ├── pearpass/
│   ├── wiredove/
│   └── notebooklm/
├── VERSION
├── README.md
├── CLAUDE.md
└── LICENSE
```

## Using Individual Plugins

Each plugin can be used standalone:

```bash
claude --plugin-dir ./grandcamel-plugins/plugins/holepunch
claude --plugin-dir ./grandcamel-plugins/plugins/jira-assistant-skills
```

## Python Dependencies

Some plugins require Python libraries:

```bash
# JIRA plugin
pip install jira-assistant-skills-lib

# Confluence plugin
pip install confluence-assistant-skills-lib

# Splunk plugin
pip install splunk-assistant-skills-lib
```

## License

MIT
