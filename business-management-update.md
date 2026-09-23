# Business management update — release candidate

This package prepares the business-management expansion of the shared Medal MCP. It is not a claim that the expansion is deployed, host-tested or approved by a marketplace. Release the coordinated backend/MCP changes and complete the acceptance ledger before publishing this package as 1.2.0.

The shared endpoint stays `https://mcp.medalsocial.com/plugins/marketing/mcp`. No separate Claude, ChatGPT or Grok business backend is introduced.

| Addition | Behavior |
| --- | --- |
| Bookings | Today, search, detail, services, resources and availability; previewed creation for an existing contact and rescheduling |
| Workspace | Member reads; previewed rename/invite; owner-authorized member role changes |
| Traffic | Connected sites and source-specific traffic/search summaries with freshness |
| Google Business | Locations and live hours; previewed regular/special-hour submission |
| Sanity | Document/schema discovery; bounded existing-copy edits, drafts and separately approved publication |

The server declares up to 51 tools including the original 22. The catalog is filtered by granted scopes; each operation also checks current workspace authority. Existing grants retain their old permissions. Reconnect and review the expanded consent to enable new tools; some hosts may also require refreshing their tool catalog or OAuth client registration.

Sanity edits require a deployed schema. Custom validators can produce a clearly marked review draft requiring Studio validation; the connector cannot publish those drafts. Unsupported schema versions, structural edits and existing editorial drafts are refused. CMS publication does not prove that a website cache refreshed. Google submission does not prove that a public listing updated. Online booking payment is not part of the new staff-booking tools.

## Release and directory updates

1. Merge and deploy the shared server changes through Medal's coordinated staging/production workflow.
2. Test a fresh grant and a legacy grant; legacy grants must not acquire new powers silently.
3. Run the business cases in `acceptance.md` in each supported host using dedicated demo records.
4. Change release-candidate versions to 1.2.0 and publish the package update with the existing logo and identity.
5. Update the existing ChatGPT/Claude review entries with expanded tools, permissions, limitations and fresh recordings. Follow the current publisher portal's update/re-review process; do not create duplicate listings or claim approval.
6. Update the existing Cursor/Grok package submission according to its publisher workflow. Server changes and marketplace approval are separate milestones.

This repository contains no reviewer credentials. Supply any required reviewer access only through the publisher's private fields.

## Staging evidence, 23 September 2026

Live backend checks passed for member reads, rename/restore, booking catalogue/availability/create/reschedule/idempotent replay, traffic reads and workspace isolation. A Sanity review draft saved and replayed without changing the published document; custom-rule publication was refused. Studio browser handoff fixes Medal-Social/medal-monorepo#5207 and Medal-Social/medal-customers#960 are merged and deployed to staging. Browser acceptance passed: the Downloads review draft opens in the embedded Studio and visual website preview, retains its module and leaves published content unchanged. The old Coffee Chat fixture has legacy schema warnings and is not a clean validation fixture. Native-host acceptance with the expanded grant, a controlled live member invitation and an approved Google test location remain pending. These backend checks do not certify each host.

Production repair promotion completed successfully in Medal-Social/medal-monorepo run 35878629469 (release PR #5208). Both MCP endpoints passed health and unauthenticated-access checks. Desktop/mobile staging previews passed; Studio retains a pre-existing SEO title-length warning. Expanded marketplace publication remains pending the host/provider checks above.
