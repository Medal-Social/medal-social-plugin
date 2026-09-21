# Microsoft Copilot Studio

## Preferred setup: MCP onboarding wizard

1. Open a test agent in Copilot Studio and choose Tools > Add a tool > New tool > Model Context Protocol.
2. Name: **Medal Social**.
3. Description: **Create and edit branded campaign drafts and inactive transactional templates using Medal Brand Center, approved images and native email modules. Return the Medal visual builder link for review. Email tools never send messages.**
4. Server URL: `https://mcp.medalsocial.com/plugins/marketing/mcp`.
5. Authentication: OAuth 2.0 > Dynamic discovery. Use Streamable HTTP.
6. Create the connection, sign in to Medal, select the intended workspace and review the consent permissions.
7. Where tool selection is available, enable the six email tools only for the email demo. Copy the shared email skill's workflow into the agent instructions if the host does not load MCP server instructions. Keep the agent unpublished while validating drafts.

## Power Apps import alternative

`apiDefinition.swagger.json` follows Microsoft's documented MCP schema format. Import it as a custom connector, then configure OAuth in the authenticated Power Platform environment. It is an import starting point, not a complete certified connector. Never run it with authentication disabled. No client ID, secret, token or user grant is included.

Use the wizard first because it supports OAuth discovery/DCR directly. A certification export must include the environment's actual authentication configuration and supporting artifacts. Do not invent client credentials or ship a nominally authenticated configuration with blank security settings.

## Public marketplace

Microsoft's certification route requires a verified Partner Center publisher enrolled in Microsoft 365 and Copilot. Submit under **Connectors and Agents for Microsoft Copilot Studio**, with the actual connector export, logo, intro.md, review access and test evidence. A successful test-agent connection is separate from public certification and Microsoft 365 deployment.

Sources:
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/mcp-add-existing-server-to-agent
- https://learn.microsoft.com/en-us/microsoft-copilot-studio/mcp-server-certification
