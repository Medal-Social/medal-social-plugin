# Host acceptance checklist

Run independently in Claude, Gemini Apps and Microsoft Copilot Studio. Use only a designated demo workspace and unsent drafts. Record actual results separately from expected behavior; never mark a scenario passed from a package validator or protocol probe.

| Scenario | Expected result |
| --- | --- |
| Workspace OAuth | Correct workspace is displayed at consent and retained in tool calls |
| Brand-first launch brief | Read current Brand Center before composing; use product_launch recipe, real brand styling, verified copy and CTA |
| Image | Reuse approved assets or import an authorized public image; correct alt text and native image module |
| Campaign | Preview then create exactly one unsent campaign with no recipients; return working editor URL |
| Transactional | Create inactive template with declared variables; no activation or invented values |
| Visual review | Inspect desktop/mobile, light/dark, logo, hero, CTA contrast, footer and unsubscribe for campaigns |
| Human edit | Edit caption/style in Medal, persist, then request a different text edit through the assistant; preserve manual changes |
| Stale revision | Reject a stale expected_revision; reread before a reconciled patch |
| Retry | Same exact creation/idempotency key does not duplicate the draft |
| Missing brand or permission | Explain the missing setup or permission without claiming successful creation |
| Unsafe image or unsupported sketch | Reject disallowed import; disclose inability to view sketch; no fabricated inspection |
| Workspace isolation | Refuse access outside the authorized workspace |

Directory reviewers may require additional testing for every social/customer tool exposed by the grant. The email checklist is not a claim that those additional tools have been tested in every host.

## Business-management acceptance (pending live verification)

Run these in a dedicated demo workspace after deployment. Test each host separately.

| Case | Required evidence |
| --- | --- |
| Legacy vs fresh consent | Old grant has no new tools; fresh grant exposes only its scopes and current role |
| Bookings | Today matches Medal; creation appears once; move preserves history; occupied slot and stale price refuse |
| Workspace | Rename reflected in Medal; approved demo invite has expected effect; role change persists; owners/self remain protected |
| Traffic | Answer matches provider, window and freshness; disconnected source is not reported as zero |
| Google hours | Approved test location only; exact field mask; concurrent edit refuses; pending review distinguished from public visibility |
| Site copy | Supported deployed schema; draft opens in Studio; layout preserved; unsupported rules and existing draft refuse |
| Publication | Separate approval; both revisions enforced; CMS result and live-site freshness reported separately |
| Replay/revocation | No duplicate effects; revoked permissions denied; interrupted external write is not repeated blindly |

Do not alter a live customer listing, send a real customer notification, or publish a real customer page just to complete this checklist. Choose an authorized test target and record any remaining limitation.
