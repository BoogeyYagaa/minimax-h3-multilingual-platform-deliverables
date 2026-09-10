verdict: PUBLIC_QA_CHANGES
scope: FRESH_INDEPENDENT_PUBLIC_GATE
article_id: EN-09
platform: Zenn
public_url: https://zenn.dev/videowebai/articles/cf88a1bb43802d
date: 2026-09-10

# EN-09 fresh public gate report 2

## Decision

`PUBLIC_QA_PASSED` is not available. The second R-P independently rechecked the same public reader URL using a fresh full reader-body snapshot and reports `PUBLIC_REVIEW_CHANGES`: stable finding `PUBLIC-RENDER-001` remains OPEN. The two repairable subparts from round 1 are now verified as corrected, but the sole native reader title/H1 remains a shortened title rather than the exact frozen plain-text platform title.

Separately, the user-returned URL and the recheck request both retain `human_acceptance: NOT_YET_PROVIDED`. A URL, a partial reader repair, local G1 `PASS`, and this read-only G-P cannot be promoted to `HUMAN_ACCEPTED`, completion, harvest, or `PUBLIC_QA_PASSED`.

## Inputs independently consumed

| Input | SHA-256 | Gate use |
| --- | --- | --- |
| `r3/public-review-2.md` | `9939d8c0e285c7ddb04ef5bdad750e33d5a1efddc636220249bf35fe64b15fbb` | Authoritative second R-P verdict and disposition of the stable public finding. |
| `evidence/public-reader-observation-2.json` | `e0b4e8fecafbab1dd2f3723fa91f788aa44baea0a783b362545d3d9c6b776f8d` | Fresh anonymous reader/body/image observations. |
| `human-release/Zenn/fingerprint.json` | `705a8f3fc64539ce47c5c9aebb64958a96bda5ccb83eca79a19e685fe87156b9` | Frozen title, `SEPARATE_TITLE_FIELD` transport, links, headings, images, disclosure, and body expectation. |
| `title-strategy.md` | `13e332a1580e9707249371f8c897cc61fb352000ea9270f9d57d0f2e2df4700e` | Frozen canonical/platform title mapping. |
| `r3/public-review-1.md` | `69fb31f309dc6a991fe9842dd6363fcc9782013248744611f2c19af66f0b3652` | Original opening of `PUBLIC-RENDER-001` and subpart baseline. |
| `r3/public-gate-report-1.md` | `8661bf2dd6e60ebbe1f30113639d139286f254997ab4b1c486de2f6257d768aa` | Prior independent G-P disposition and human-only boundary. |
| `../../evidence/EN-09-user-publication-url.json` | `08c3f1622ac2141d8bf30642238bb0e4356ddb23b492add9c4064b123490bd1d` | Initial URL provenance and missing human acceptance. |
| `../../evidence/EN-09-user-recheck-requests.json` | `f1d51be1b5151b04efeacf692c6ab3a57e667d7eb8824e16c17e25ee2c89116a` | Same-URL recheck provenance; it explicitly forbids assuming the repairs succeeded. |
| `r3/full-review-2.md` and `r3/gate-report-1.md` | `a9bf3b661e3c1852df9fd6843940cbe0a940cbb59b2f7ff7642eab12f6385fe1`; `37becdb43624b9e97ac6b0eb3f8f18ec235ebc97c30c7284f4012e44f3e2a769` | Local package/G1 context only, not public-QA or acceptance evidence. |

## Stable public-finding mapping

| Stable finding | Round-1 reader state | Fresh round-2 state | G-P disposition |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | Native title had a literal `#`, was shortened, and the frozen full title appeared again as a reader-body H1. | The literal `#` is gone; there is exactly one native H1 and `body_h1_count` is `0`. The sole native/document/OG title remains `AI Video Prompt Iteration Workflow: One Attempt, One Thing.` rather than `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing`. | **OPEN, partially repaired**. The first two subparts are corrected and must not be re-opened; the remaining exact-title mismatch keeps the same stable finding open. |

No new public finding is created. The pre-publication findings `SEO-LONGTAIL-RESEARCH-001`, `PAYLOAD-ANNOTATION-001`, and `VISUAL-NARRATIVE-001` remain resolved in their recorded local review history; their local resolution does not close `PUBLIC-RENDER-001`.

## Public reader surfaces that remain verified

- The fresh anonymous reader document was `200 text/html`; it produced 51 expected and 51 observed normalized reader-text units with zero differences.
- The reader body begins with the exact founder disclosure; the approved provider-attribution and fact-boundary wording, ordered eight H2 / three H3 map, and both fixed VideoWeb anchor/href pairs remain present.
- All three public Zenn PNG resources returned `200 image/png`; their ALT text, captions, and lead/middle/closing positions match the release manifest. Platform-delivered image bytes and dimensions are not asserted to equal the local source files.
- The parsed reader body contains no Chinese cards, HTML comments, source filenames, local paths, or operator text.

## Minimal human-only next action

Issue `HUMAN_NEEDS_FIX` for the remaining reader-visible mismatch only. In the authorized native Zenn editor, set the separate title field as plain text to exactly:

`AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing`

Preserve the now-matching reader body, H2/H3 order, two fixed links, founder disclosure, three image locations/ALT/captions, tags, and fact-boundary text. No local W revision is indicated by the current evidence. After the human rechecks the complete acceptance checklist, return the public URL with an explicit `HUMAN_ACCEPTED` only if every applicable row passes; otherwise return `HUMAN_NEEDS_FIX` and the failed rows. Then the original EN-09 R must perform a fresh anonymous R-P, followed by another fresh G-P.

The native title-control capability, including any length or control limitation, remains `UNVERIFIED`. This report does not infer a cause, limit, workaround, or exception from the shortened title.

## Acceptance and execution boundary

- `HUMAN_ACCEPTED`: `NOT_YET_PROVIDED`.
- The same returned URL is evidence neither of the title repair nor of human acceptance.
- This G-P used only the recorded on-disk evidence. It did not access an external site, browser, editor, account, root state, or platform service; it did not upload, edit, save, publish, repost, delete, change visibility, or harvest anything.
- This article remains outside `PUBLIC_QA_PASSED` until the exact title mismatch is closed by a fresh reader comparison and explicit human acceptance is provided.
