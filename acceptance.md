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

## Business-management native-host acceptance (pending)

Run these in a dedicated demo workspace after deployment. Test each host separately.

| Case | Required evidence |
| --- | --- |
| Legacy vs fresh consent | Old grant has no new tools; fresh catalog follows its scopes and operations enforce current authority |
| Bookings | Today matches Medal; creation appears once; move preserves history; occupied slot and stale price refuse |
| Workspace | Rename reflected in Medal; approved demo invite has expected effect; role change persists; owners/self remain protected |
| Traffic | Answer matches provider, window and freshness; disconnected source is not reported as zero |
| Google hours | Approved test location only; exact field mask; an edit detected during the fresh pre-write read refuses (Google offers no atomic revision precondition); pending review distinguished from public visibility |
| Site copy | Supported deployed schema; draft opens in Studio; layout preserved; custom validators produce review-only drafts; connector publication and existing drafts refuse |
| Publication | Separate approval; both revisions enforced; CMS result and live-site freshness reported separately |
| Replay/revocation | No duplicate effects; revoked permissions denied; interrupted external write is not repeated blindly |

Do not alter a live customer listing, send a real customer notification, or publish a real customer page just to complete this checklist. Choose an authorized test target and record any remaining limitation.


## Email experience update (1.2.0-rc.2)

Backend implementation is in the coordinated monorepo release; this package remains a release candidate until staging and native-host acceptance are recorded.

| Case | Required evidence |
| --- | --- |
| MCP Apps | Desktop/mobile preview and editor link in each supporting host; plain results and editor fallback in others |
| Preview isolation | Scripts, forms, remote frames and unsafe editor links blocked; existing public images render |
| Private attachment | Default import has no public copy; workspace isolation and revocation reject; bytes never echoed |
| Public email attachment | Explicit user approval; exact request confirmation; public URL readback and idempotent replay |
| Legacy logo | Resolve only existing public derivatives in the same workspace; never publish private originals |
| QA | Warnings from exact rendered HTML; browser/static checks not misrepresented as inbox or link tests |
| Performance | Correct delivered/open/click counters; missing/legacy values remain null; no recipient details; attribution unavailable |

Monorepo implementation #5209 is merged; staging transaction 35919250470 succeeded on 2026-09-23. Live backend acceptance verified private originals are not publicly readable (404), explicitly public images load (200), repeated imports reuse the same asset, outsiders are rejected, existing approved logo derivatives resolve, and an unsent campaign returns correct draft/zero-send/null-tracking metrics. The new draft was rendered locally with both images and a 375px mobile view.

Demo: https://medalsocial.dev/ws/medal-email-connector-staging/emails/templates/p175rx9gvg1mzs7a5v8kfmprkh8ezdqe

The staging MCP health/discovery checks pass, advertise email.campaign.read, and reject unauthenticated initialize requests. All nine local preview checks pass across Chromium, Firefox and WebKit, including Norwegian/Arabic host locales. PR #5210 corrects a corrupt synthetic PNG discovered by the full Firefox gate; it does not change application code.

These staging results are backend/protocol/browser-harness evidence. Native email acceptance was subsequently performed on 24 September 2026 as recorded below. Expanded business-scope acceptance and directory updates remain pending. This package remains a release candidate.

## Production release verification

The coordinated server update is deployed. Final source 39f4281aeb5fea5efb5cc477fa96e99a32016ebf passed full post-merge CI 35921759852 and staging release 35921760958. Production release 35923692729 succeeded, merging release PR #5211 at ad03ad1c95965cf796babd62d209feef306b04fe. Production health and protected-resource discovery return 200, discovery includes email.campaign.read, and anonymous initialize returns 401 with an OAuth challenge. Existing grants need reconnection to authorize the new analytics scope.

Release evidence: https://github.com/Medal-Social/medal-monorepo/actions/runs/35923692729

Production deployment does not complete native-host acceptance or marketplace review. The package remains 1.2.0-rc.2 pending those checks.


## Native host verification — 24 September 2026

Both native ChatGPT and Claude successfully read demo Brand Center, rendered an MCP Apps preview, created an unsent campaign draft, edited body copy, and imported a synthetic private PNG. An identical attachment retry returned the same asset ID in each host; no public URL was returned. No campaign was sent and no transactional trigger was activated.

- Claude conversation: https://claude.ai/chat/507a0c6a-df59-4154-aa71-223b8896c79b
- Claude saved draft: https://app.medalsocial.com/ws/chatgpt-plugin-review-wo/emails/templates/p170jfmcp6ap7ewj2ctvt42ykx8ey65z
- ChatGPT conversation: https://chatgpt.com/c/6ab452c1-92c8-83eb-b656-74c5e2c47b38
- ChatGPT corrected draft, visually verified in Medal's builder: https://app.medalsocial.com/ws/chatgpt-plugin-review-wo/emails/templates/p170akw3eyqfnz42a012ajp8eh8ezbqd

ChatGPT initially omitted the product_launch recipe when saving, although its separate preview used it. The diagnostic draft was retained; a second draft with the recipe passed explicitly to creation restored the large headline. The shared skill now requires exact preview/create composition reuse and saved-block readback. A content-only patch cannot restore omitted typography styles. The corrected run verifies the remedy; it does not establish that every future model run will follow the skill.

The template-level is_active flag is not the campaign send status. Native campaign-performance reads subsequently passed after the expanded grant, as recorded below. Existing email grants exposed 23 tools; fresh expanded consent was subsequently completed for both hosts, as recorded below. Business operations have not yet been accepted in these native sessions, and Google hours still lacks an approved connected test location.

Claude's existing listing is Published at https://claude.ai/directory/medal-social; its listing update was subsequently submitted, as recorded below. OpenAI's version 1.0.0 remains Review and read-only in the publisher portal; no new version action was available. It was not withdrawn. The full update is not claimed approved or publicly available on ChatGPT. Skill package changes require the relevant host's package update/review process.


## Expanded native grants and directory update — 24 September 2026

Reauthorized Claude and ChatGPT Full Demo with the expanded scopes, restricted to ChatGPT Plugin Review Workspace. Both hosts successfully read campaign performance (draft, zero sends and recipients, null unavailable tracking), workspace members, site inventory and Google Business location inventory. The demo has no connected sites or Google locations, so traffic and hours were not tested. Both booking-today reads returned 403. The booking API enforces the workspace bookings-module feature gate independently of OAuth scopes; the specific production workspace configuration has not yet been inspected. No business mutation, notification or public update was performed.

ChatGPT read-only evidence: https://chatgpt.com/c/6ab45757-870c-83ed-aaf8-4123662b4c1d

Claude directory update submitted: the publisher explicitly confirms 'Your latest edit is in review; the live listing stays until it is approved.' The update synchronizes all 53 tools, declares MCP App support, explains expanded permissions and documents the incomplete live cases. The all-tools self-tested checkbox was cleared to avoid claiming unperformed acceptance. Existing published listing remains available.

OpenAI 1.0.0 remains in Review and locked; no update version was submitted or existing review withdrawn. The full developer connector works. A publisher warning revealed missing dedicated widget-domain metadata; PR #5213 adds standard ui.domain and passed all 25 focused plugin-server tests. It is merged into dev; production deployment is tracked separately and is not implied by merge.

PR: https://github.com/Medal-Social/medal-monorepo/pull/5213
