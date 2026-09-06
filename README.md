# Sommont Luca Plugin

This repository contains public Codex plugin distribution metadata for Sommont
Luca. It does not contain Sommont application source code.

## Packages

- `sommont-luca`: production plugin wrapper for `https://mcp.sommont.com/mcp`
- `sommont-luca-dev`: development plugin wrapper for `https://mcp-dev.sommont.com/mcp`

## Copy-Paste Install Prompts

Use one of these prompts with ChatGPT, Claude, Codex, or another coding
assistant that can run terminal commands on your machine.

### Install PROD

```text
Install the Sommont Luca Codex plugin from GitHub.

Use this public marketplace repo:
https://github.com/wisewoodholdings-eng/sommont-luca-plugin

Install the production plugin, not the DEV plugin.

Run:
codex plugin marketplace add wisewoodholdings-eng/sommont-luca-plugin --ref main
codex plugin add sommont-luca@sommont

Then verify `codex plugin list` shows:
sommont-luca@sommont installed, enabled

After install, tell me to start a new Codex task/thread so the plugin tools are loaded.
```

### Install DEV

```text
Install the Sommont Luca DEV Codex plugin from GitHub.

Use this public marketplace repo:
https://github.com/wisewoodholdings-eng/sommont-luca-plugin

Install the DEV plugin for pre-production testing, not the production plugin.

Run:
codex plugin marketplace add wisewoodholdings-eng/sommont-luca-plugin --ref main
codex plugin add sommont-luca-dev@sommont

Then verify `codex plugin list` shows:
sommont-luca-dev@sommont installed, enabled

After install, tell me to start a new Codex task/thread so the plugin tools are loaded.
```

## OAuth

Sommont Luca uses OAuth account linking through Clerk.

Production:

```text
MCP endpoint: https://mcp.sommont.com/mcp
Protected resource metadata: https://mcp.sommont.com/.well-known/oauth-protected-resource
OAuth mode: Pre-defined client credentials
Client ID: 3AO2lHQkWaGfvXbY
Scopes: openid profile email
```

Development:

```text
MCP endpoint: https://mcp-dev.sommont.com/mcp
Protected resource metadata: https://mcp-dev.sommont.com/.well-known/oauth-protected-resource
Scopes: openid profile email
```

## Install From GitHub

Add this repo as a Codex Git marketplace:

```bash
codex plugin marketplace add wisewoodholdings-eng/sommont-luca-plugin --ref main
```

Install the production plugin:

```bash
codex plugin add sommont-luca@sommont
```

Optional development plugin:

```bash
codex plugin add sommont-luca-dev@sommont
```

Start a new Codex thread after installing so the plugin and MCP tools are loaded.

## Local Codex Marketplace

This repo is structured as a marketplace root:

```text
.agents/plugins/marketplace.json
plugins/sommont-luca/.codex-plugin/plugin.json
plugins/sommont-luca/.mcp.json
plugins/sommont-luca-dev/.codex-plugin/plugin.json
plugins/sommont-luca-dev/.mcp.json
```

Install the marketplace from a local clone when testing in Codex:

```bash
codex plugin marketplace add /path/to/sommont-luca-plugin
codex plugin add sommont-luca@sommont
```

The same package files are self-hosted by Sommont:

```text
https://sommont.com/plugins/marketplace.json
https://sommont.com/plugins/sommont-luca/.codex-plugin/plugin.json
https://sommont.com/plugins/sommont-luca/.mcp.json
```
