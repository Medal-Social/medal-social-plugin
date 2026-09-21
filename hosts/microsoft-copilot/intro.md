# Medal Social

Turn a campaign brief, content idea or sketch visible to your assistant into an on-brand email draft. Medal Brand Center supplies voice, colors, typography, logo and company footer. Native text, image, button and layout modules remain editable in the Medal visual email builder; custom HTML is available where necessary.

## Prerequisites

A Medal Social account, workspace membership, completed Brand Center email settings and permission to create email drafts. Copilot Studio access and an environment whose data policies permit this connector are also required.

## Authentication

Connect using OAuth 2.0 and select the intended Medal workspace. Tools are restricted by the user's granted scopes and workspace permissions. Never share credentials in chat. Inspect the actual consent screen: the shared connector also supports authorized social and customer-context capabilities.

## Email tools

- `get_email_brand_context`: current branding, email settings and approved assets.
- `import_email_image`: import a user-approved public image into public email assets.
- `preview_email`: compile and validate before saving.
- `create_email_draft`: save an unsent campaign or inactive transactional template.
- `get_email_draft`: read editable modules and their document revision.
- `update_email_draft`: apply targeted, revision-checked edits.

## Example

Create an unsent email announcing our mobile app. Use Brand Center, an approved hero image, one verified CTA and our standard footer. Keep the modules editable and return the Medal builder link.

## Limits and troubleshooting

Draft tools do not send email, add recipients or activate transactional triggers. If permissions are missing, reconnect with the required scopes. If Brand Center is incomplete, finish its email setup. On an edit conflict, read the latest draft and reconcile changes. Public image imports must not contain confidential material. Browser previews do not establish rendering in every inbox client.

## Support

https://medalsocial.com — hello@medalsocial.com

This document accompanies the connector preparation package; it does not assert Microsoft certification.
