# Claude

## Connect in Claude web

In Customize > Connectors, choose Add custom connector. Name it **Medal Social** and enter:

`https://mcp.medalsocial.com/plugins/marketing/mcp`

Choose sign-in before use. Medal supports OAuth discovery and dynamic client registration. Complete Medal sign-in, choose the intended workspace and review the actual consent permissions. Then use the starter prompts in the main README.

## Claude Code and Cowork plugin

This repository includes `.claude-plugin/plugin.json`, `.mcp.json` and the shared `skills/medal-branded-email/SKILL.md`. The 1.2 release candidate also includes `skills/medal-business-management/SKILL.md`; its new capabilities remain subject to deployment and acceptance. For a local Claude Code check after cloning, run `claude --plugin-dir ./medal-social-plugin`, then authenticate the Medal connection through `/mcp`.

A remote connector listing and a Cowork/Claude Code plugin listing have separate submission forms. Package availability is not directory approval. See [connector submissions](https://claude.com/docs/connectors/building/submission) and [plugin submissions](https://claude.com/docs/plugins/submit).

Use an unsent campaign and an inactive transactional draft for acceptance. Confirm the actual builder result and manual-edit preservation before claiming host support. Shared protocol or package validation alone is insufficient.

For the business expansion, update the existing connector submission rather than creating another listing. The existing email connector was observed as Published on September 22, 2026 at [Medal's publisher page](https://claude.ai/directory/manage/medal-social); that page says edits go through review before replacing the live listing. Complete the business scenarios in `acceptance.md`, reconnect for the added scopes, and use the proposed update copy in `listing.md` only after those checks pass.
