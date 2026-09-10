verdict: PUBLIC_QA_DEFERRED
scope: FRESH_INDEPENDENT_PUBLIC_GATE
article_id: EN-09
platform: Zenn
public_url: https://zenn.dev/videowebai/articles/cf88a1bb43802d
date: 2026-09-10

# EN-09 fresh public gate report 3

## Scope and independent boundary

This is a fresh, on-disk public-gate decision for the frozen `EN-09` /
English / Global English readers / Zenn /
`VIDEOWEB_OWNER_ACCOUNT_PRIORITY` mapping. That exact pair is in the frozen
allowed scope. The applicable frozen requirements remain `REQ-SCOPE-001`,
`REQ-BRAND-001`, `REQ-CONTENT-001`, `REQ-LINK-001`, `REQ-PAYLOAD-001`,
`REQ-WORKFLOW-001`, and `REQ-PUBLICATION-001`.

This G-P used only the local records listed below. It did not fetch a page,
open a browser, editor, or account, or upload, edit, save, publish, repost,
delete, roll back, change visibility, harvest, or change campaign/root state.
This report is the only file written for this decision.

## Evidence consumed

| Local record | SHA-256 | Gate use |
| --- | --- | --- |
| `r3/public-review-2.md` | `9939d8c0e285c7ddb04ef5bdad750e33d5a1efddc636220249bf35fe64b15fbb` | Latest R-P verdict and the saved round-2 reader comparison. |
| `evidence/public-reader-observation-2.json` | `e0b4e8fecafbab1dd2f3723fa91f788aa44baea0a783b362545d3d9c6b776f8d` | Saved anonymous reader/body/image observations; no new capture is claimed. |
| `r3/public-gate-report-2.md` | `7c91aea67379f5461b90ccebaeed013e45170d5682810bf6a6b8383f51273142` | Prior fresh G-P decision and the original title-repair boundary. |
| `r3/public-finding-disposition-1.md` | `0c80fd8f06667edb9b8552b4a52abb2d5782df1bbf2871f27de05d3571803183` | Narrow local disposition for the remaining title-text subpart only. |
| `../../evidence/EN-09-user-confirmed-title-length-limitation.json` | `911356d62e00fc027b41c795f30141a1d376d379ab5f31283b35ed02d8235212` | Explicit user limitation statement, its exact scope, and the absence of a stated character cap or whole-article acceptance. |
| `../../evidence/EN-09-user-publication-url.json` | `08c3f1622ac2141d8bf30642238bb0e4356ddb23b492add9c4064b123490bd1d` | Returned URL provenance and `human_acceptance: NOT_YET_PROVIDED`. |
| `../../evidence/EN-09-user-recheck-requests.json` | `f1d51be1b5151b04efeacf692c6ab3a57e667d7eb8824e16c17e25ee2c89116a` | Round-2 same-URL recheck provenance and its retained absence of human acceptance. |
| `human-release/Zenn/fingerprint.json` | `705a8f3fc64539ce47c5c9aebb64958a96bda5ccb83eca79a19e685fe87156b9` | Frozen title, `SEPARATE_TITLE_FIELD` transport, body, heading, link, image, disclosure, and metadata controls. |
| `title-strategy.md` | `13e332a1580e9707249371f8c897cc61fb352000ea9270f9d57d0f2e2df4700e` | Frozen canonical/platform title mapping. |
| `r3/full-review-2.md` and `r3/gate-report-1.md` | `a9bf3b661e3c1852df9fd6843940cbe0a940cbb59b2f7ff7642eab12f6385fe1`; `37becdb43624b9e97ac6b0eb3f8f18ec235ebc97c30c7284f4012e44f3e2a769` | Local package approval and `HUMAN_RELEASE_READY` context only; neither is public acceptance or public-QA proof. |

## Exact title-limitation mapping

| Stable finding and subpart | Frozen control | Saved public fact | Disposition and gate treatment |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` — remaining native-title shortening only | Canonical H1 and platform title remain `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing`. | The sole native/document/Open Graph title remains `AI Video Prompt Iteration Workflow: One Attempt, One Thing.` (including the recorded final period). It does not equal the frozen full title. | `USER_CONFIRMED_TITLE_LENGTH_LIMIT_NO_REPAIR_REQUIRED`. The user statement is limited to `Zenn 标题有长度限制`; the exact native character cap is `NOT_PROVIDED`. This closes the remaining title-length subpart as a no-repair-required platform limitation. It does not alter the frozen title, establish a cap, native-control behavior, cause, workaround, or title parity. |
| `PUBLIC-RENDER-001` — literal Markdown title marker | No literal `#` in the native title. | The saved round-2 observation records `literal_hash_in_native_title: false`. | Already verified corrected; preserved and not reopened. |
| `PUBLIC-RENDER-001` — duplicate reader-body H1 | `SEPARATE_TITLE_FIELD` requires zero reader-body H1 elements. | The saved round-2 observation records exactly one native H1 and `body_h1_count: 0`. | Already verified corrected; preserved and not reopened. |

The accepted limitation is only the remaining shortened native-title mismatch.
It does not relabel the frozen title as changed or as a native-title match, and
it does not turn the underlying observed non-parity into a repaired transfer.
No title retry, native-control confirmation, editor inspection, or fresh
public-title retry is requested for that scoped limitation.

## Public reader surfaces retained from round 2

The saved anonymous reader evidence remains substantive reader evidence, not
an HTTP-status-only record: the document was `200 text/html`, 51 expected and
51 observed normalized reader-text units had zero differences, and the body
began with the frozen founder disclosure. The ordered eight H2 / three H3
map, both exact VideoWeb anchor/href pairs, provider-attribution and
fact-boundary text, and three public PNG image positions with exact ALT and
captions remain verified by that saved observation. It also records no Chinese
cards, HTML comments, source filenames, or local paths in the reader body. No
source-byte equality is claimed for platform-transformed images.

## Public-gate decision mapping

| Verdict | Mapping to the on-disk record |
| --- | --- |
| `PUBLIC_QA_PASSED` | Not available. `HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED` / `NOT_EXPLICITLY_PROVIDED`. The title-limitation statement is expressly not full-article acceptance. The latest R-P on disk remains `PUBLIC_REVIEW_CHANGES`; the narrow disposition does not itself create `PUBLIC_REVIEW_APPROVED` or a public-QA pass. |
| `PUBLIC_QA_CHANGES` | Not selected. The former request to repair the remaining title text is superseded only as a repair obligation by the explicit no-repair-required limitation. No other reproducible public reader mismatch is recorded, and this G-P must not manufacture a title repair card, retry, or control check. |
| `PUBLIC_QA_ROLLBACK` | Not selected. The saved reader evidence records no severe body, disclosure, link, heading, or image failure, and no rollback decision or action is authorized by these records. |
| `PUBLIC_QA_DEFERRED` | **Selected.** The remaining title non-parity has a scoped no-repair disposition, but the separate acceptance and current-review prerequisites for a pass are absent. A public URL, local package gates, saved reader evidence, and the limitation statement cannot supply whole-article `HUMAN_ACCEPTED`, an R-P approval that accounts for the disposition, or a public-QA pass. |

## Boundary before a later public pass

No editor, title, or public-page repair is requested by this report. Before a
later fresh G-P may consider `PUBLIC_QA_PASSED`, the record needs (1) an
explicit full-article `HUMAN_ACCEPTED` result, separate from the title-length
limitation statement, and (2) an EN-09 R-P decision that accounts for this
retained scoped disposition and is `PUBLIC_REVIEW_APPROVED`. If a material
public change occurs, that R-P also needs fresh reader evidence; this G-P does
not assert a new capture or require one for the accepted title limitation.

Until then, EN-09 is `PUBLIC_QA_DEFERRED`: the frozen/public title difference
remains documented as accepted non-parity, not repaired or fully matching;
the article is not whole-article accepted, not public-QA passed, and not
eligible for completion or harvest.
