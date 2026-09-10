verdict: PUBLIC_QA_CHANGES
scope: FRESH_INDEPENDENT_PUBLIC_GATE
article_id: EN-09
platform: Zenn
public_url: https://zenn.dev/videowebai/articles/cf88a1bb43802d
date: 2026-09-10

# EN-09 fresh public gate report 1

## Decision

`PUBLIC_QA_PASSED` is not available. The original article-scoped R-P has independently obtained and compared the anonymous public reader body, but it reports one OPEN, reader-visible transport mismatch: `PUBLIC-RENDER-001`. Separately, the user-returned URL record still says `human_acceptance: NOT_YET_PROVIDED`. The public URL, local G1 `PASS`, and successful reader surfaces below therefore cannot be promoted to `HUMAN_ACCEPTED`, completed, harvested, or public-QA-passed.

This fresh G-P issues `PUBLIC_QA_CHANGES`. This report makes no claim about why Zenn rendered the title/body boundary this way and does not access or change the editor, account, post, visibility, images, or campaign/root state.

## Inputs independently consumed

| Input | SHA-256 | Gate use |
| --- | --- | --- |
| `r3/public-review-1.md` | `69fb31f309dc6a991fe9842dd6363fcc9782013248744611f2c19af66f0b3652` | Authoritative original R-P result and stable public finding. |
| `evidence/public-reader-observation-1.json` | `771e8f5eb74c218dd915377931c3a024fe6261b2911c6f9c50edc58c363f83e9` | Anonymous HTTPS reader/image observations, document/body hashes, and field facts. |
| `human-release/Zenn/fingerprint.json` | `705a8f3fc64539ce47c5c9aebb64958a96bda5ccb83eca79a19e685fe87156b9` | Frozen title/H1 transport and expected reader payload. |
| `../../evidence/EN-09-user-publication-url.json` | `08c3f1622ac2141d8bf30642238bb0e4356ddb23b492add9c4064b123490bd1d` | Returned URL provenance and absence of human acceptance. |
| `r3/full-review-2.md` | `a9bf3b661e3c1852df9fd6843940cbe0a940cbb59b2f7ff7642eab12f6385fe1` | Local R2 closure context only; it is not public-QA evidence. |
| `r3/gate-report-1.md` | `37becdb43624b9e97ac6b0eb3f8f18ec235ebc97c30c7284f4012e44f3e2a769` | Local `HUMAN_RELEASE_READY` boundary only; it is not a publication or public-QA result. |

## R-P finding disposition

| Finding | Status | Evidence-grounded disposition |
| --- | --- | --- |
| `PUBLIC-RENDER-001` | OPEN | The frozen `SEPARATE_TITLE_FIELD` contract requires native semantic H1/title `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing` and zero body H1s. The anonymous reader instead exposes `# AI Video Prompt Iteration Workflow: One Attempt, One Thing.` in document title, Open Graph title, and native header H1; it exposes the frozen title as an additional body H1. This is the original R-P's stable finding and remains open unchanged. |

No new public finding is created. The local findings `PAYLOAD-ANNOTATION-001`, `VISUAL-NARRATIVE-001`, and `SEO-LONGTAIL-RESEARCH-001` remain locally resolved as recorded in the prior reviews; that does not close `PUBLIC-RENDER-001`.

## Public reader surfaces preserved by the evidence

- Anonymous reader evidence is substantive, not status-only: the reader document was `200 text/html`, its full reader body was parsed, and 52 expected versus 52 observed text units had zero normalized differences.
- The ordered eight H2 and three H3 headings, founder disclosure, provider-attribution/fact-boundary wording, and both exact VideoWeb href/anchor pairs match the frozen public-reader expectation.
- Three anonymous public Zenn PNG deliveries returned `200 image/png`; their ALT text, captions, and lead/middle/closing positions match the manifest. Their delivered bytes/dimensions differ from local 1664×936 originals, so source-byte equality after platform transformation is not asserted.
- No Chinese cards, HTML comments, source filenames, or local Markdown paths were observed in the reader body. The literal `#` is confined to the title defect above.
- Zenn's generic reader description/native metadata mapping remains `UNVERIFIED`; it is not treated as a repairable local assertion.

## Human-only minimal repair card

`HUMAN_NEEDS_FIX` is required for the open reader mismatch. In the authorized native Zenn editor, a human should:

1. Put exactly `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing` in the separate title field as plain text, with no literal `#`.
2. Remove only the duplicate Markdown H1 from the reader body so the body begins with the already-verified founder disclosure.
3. Preserve the verified body order/text, H2/H3 sequence, two URL/anchor pairs, founder disclosure, three public image URLs with their ALT/captions/positions, topic fields, and the fact-boundary language.
4. Return the repaired public URL plus an explicit human result (`HUMAN_ACCEPTED` only if the complete acceptance checklist now passes; otherwise `HUMAN_NEEDS_FIX` with failed rows).

After a human repair, resume the original EN-09 R for a fresh anonymous R-P against new reader evidence, then create another fresh G-P. No final public-QA pass may be inferred before both steps and explicit `HUMAN_ACCEPTED`.

## Acceptance and execution boundary

- `HUMAN_ACCEPTED`: `NOT_YET_PROVIDED`.
- This report is a fresh independent G-P decision only. It does not create a human acceptance, change a public post, authorize an editor action, update campaign/root state, or harvest Zenn platform learnings.
- No external action was taken by this G-P. All public observations consumed are the recorded anonymous read-only evidence listed above.
