# Claude

## Connect in Claude web

In Customize > Connectors, choose Add custom connector. Name it **Medal Social** and enter:

`https://mcp.medalsocial.com/plugins/marketing/mcp`

Choose sign-in before use. Medal supports OAuth discovery and dynamic client registration. Complete Medal sign-in, choose the intended workspace and review the actual consent permissions. Then use the starter prompts in the main README.

## Claude Code and Cowork plugin

This repository includes `.claude-plugin/plugin.json`, `.mcp.json` and the shared `skills/medal-branded-email/SKILL.md`. The plugin combines the remote connector with the email design workflow. For a local Claude Code check after cloning, run `claude --plugin-dir ./medal-social-plugin`, then authenticate the Medal connection through `/mcp`.

A remote connector listing and a Cowork/Claude Code plugin listing have separate submission forms. Package availability is not directory approval. See [connector submissions](https://claude.com/docs/connectors/building/submission) and [plugin submissions](https://claude.com/docs/plugins/submit).

Use an unsent campaign and an inactive transactional draft for acceptance. Confirm the actual builder result and manual-edit preservation before claiming host support. Shared protocol or package validation alone is insufficient.
