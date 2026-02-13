# swyx's Claude Plugins

A marketplace of [Claude Cowork](https://claude.com) / [Claude Code](https://claude.com/claude-code) plugins for content creation and publishing workflows.

## Plugins

| Plugin | Description |
|---|---|
| **[latent-space-youtube](./plugins/latent-space-youtube)** | Zoom recordings → YouTube pipeline with auto titles, timestamps, playlists, and Gemini-generated thumbnails |

## Installation

### Add this marketplace

In Claude Code CLI:
```
/plugin marketplace add swyxio/claude-plugins
```

In Claude Cowork: use the plugin browser to add `swyxio/claude-plugins` as a marketplace.

### Install a plugin

```
/plugin install latent-space-youtube@swyx-plugins
```

## Creating new plugins

This repo is structured as a marketplace. To add a new plugin:

1. Create a new directory under `plugins/`
2. Add `.claude-plugin/plugin.json` manifest
3. Add skills, commands, agents as needed
4. Update `.claude-plugin/marketplace.json` with the new plugin entry

## License

MIT
