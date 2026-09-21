<img src="assets/logo.svg" width="96" height="96" alt="Medal Social" />

# Medal Social

**An idea in chat. An on-brand email you can edit.**

Connect your Medal Social workspace and turn a launch brief, content idea or sketch your assistant can view into a campaign draft or inactive transactional template. Your Brand Center supplies the voice, logo, colors, typography and footer. Images and native email modules stay editable in Medal's visual builder.

## Try it

> Create an unsent email announcing our mobile app. Use our Brand Center, an approved hero image, one download CTA and our standard footer. Open the draft in the Medal email builder.

> Create an inactive welcome email using our brand. Keep the text, image and CTA editable, and give me the builder link.

> Read this Medal email draft and shorten the second paragraph. Preserve the caption and styling I edited in the builder.

## Connect

1. Install **Medal Social** from the marketplace once the listing is approved, or import this public plugin repository using your host's supported local/team-plugin workflow.
2. Authenticate with Medal Social in the browser and select the intended workspace on the consent screen.
3. Complete Brand Center's email setup in Medal, including the logo, visual style and company footer.
4. Ask for a draft. Review and edit it through the returned Medal builder link.

A Medal Social account, workspace membership and appropriate permissions are required. Existing grants that predate email support may require reconnection. The plugin package is free; use of Medal's hosted service is subject to your Medal account and plan.

### One shared MCP

`https://mcp.medalsocial.com/plugins/marketing/mcp`

The same endpoint supplies the tool catalog, authentication, brand context, email compiler and saved drafts to compatible hosts. This package adds host metadata, the logo and a reusable email-design skill. It contains no separate email backend.

For Grok web, add this URL as a Custom connector at [grok.com/connectors](https://grok.com/connectors). Grok web custom connectors and the Grok Bot marketplace have separate installation/review flows.

## Included capabilities

| Email tool | Purpose |
| --- | --- |
| `get_email_brand_context` | Read current Brand Center guidance, email settings and available assets |
| `import_email_image` | Import an approved public image into the workspace |
| `preview_email` | Compile and validate a branded composition before saving |
| `create_email_draft` | Create an unsent campaign draft or inactive transactional template |
| `get_email_draft` | Read the live editable document and revision |
| `update_email_draft` | Apply targeted edits with protection against stale writes |

Native text, images, buttons, dividers, spacers, columns and OTP modules are supported; sanitized custom HTML is available when needed. The `product_launch` recipe provides a consistent heading, spacing and CTA hierarchy while preserving the workspace's brand.

The shared connector also includes authorized searches for posts, analytics, channels, contacts, deals and helpdesk context, plus post drafting, previewing, scheduling and publishing. Availability depends on the scopes granted at consent. **The email skill only uses draft email actions.** Inspect the actual consent screen before granting access.

## Authentication and data

- OAuth runs through Medal's browser sign-in and workspace consent. No API key, password or token is included in this repository or requested in chat.
- Network destinations: `mcp.medalsocial.com` for MCP, `app.medalsocial.com` for Medal sign-in/consent and the builder, and `assets.medalsocial.com` for public email imagery. An explicitly requested image import also fetches its approved public source URL through Medal.
- Imported email images are public assets so recipients can load them. Do not import confidential imagery.
- The connected host receives tool results containing the workspace data needed for the requested operation. Its own data policies apply alongside Medal's.
- This package has no executable hooks, install scripts, background tasks, telemetry collectors or bundled server credentials. The hosted Medal service remains separately operated.
- Revoke access through your connected-app settings. Reconnection requires normal consent.

## Validation and limits

The shared backend was exercised in an authenticated Grok web staging session: campaign and inactive transactional creation, image import, live reads/edits, preservation of manual caption/style changes, stale-write rejection and desktop/mobile builder previews. This evidence does not establish Grok Bot, Cursor, ChatGPT or Claude host acceptance, nor inbox-client certification.

Saved MCP HTML uses the shared renderer's strict table/inline-style mode. Embedded dark styles are optional in builder-preview/export modes. Review delivered test messages in your target email clients before a campaign launch.

Email sends, audience setup, scheduling and transactional trigger activation remain separate from these draft tools. A generic builder quality warning about marketing unsubscribe may appear on a transactional template; review according to the intended email type.

## Support

[Medal Social](https://medalsocial.com) · [Contact support](mailto:hello@medalsocial.com)

For a reproducible plugin issue, open a repository issue without credentials or private customer data. Report security concerns privately to the support address.

## License

The integration configuration, skill and documentation are MIT licensed. Medal Social's name and logo remain its trademarks; the license does not grant trademark rights or license the hosted service or its proprietary implementation.
