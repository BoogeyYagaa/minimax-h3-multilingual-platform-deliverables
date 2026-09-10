verdict: PUBLIC_QA_CHANGES
role: ARTICLE_PUBLIC_GATE
gate: fresh independent public G-P; on-disk evidence only
article_id: EN-04
platform: Tumblr
public_url: https://www.tumblr.com/videowebai/827355403965890560/a-travel-photo-to-video-prompt-plan-three-motion?source=share
reviewed_at: 2026-09-10
human_accepted: NOT_YET_PROVIDED

# EN-04 Tumblr public gate 2

## Decision

`PUBLIC_QA_CHANGES` remains the only supported public verdict. The new R-P2 and its fresh anonymous reader observation show an actual public Tumblr post whose normalized reader text remains equal to canonical HTML, but they do not show a repaired heading hierarchy. The frozen package requires one semantic H1, six H2 sections, and three subordinate H3 motion directions. Fresh public evidence instead records seven H1, three H2, and zero H3.

The user re-returning the same Tumblr URL is neither proof of a repair nor `HUMAN_ACCEPTED`. `HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`; therefore this report cannot be `PUBLIC_QA_PASSED`, cannot complete EN-04, and does not authorize harvest.

## Inputs read and current SHA-256

| Input | SHA-256 |
| --- | --- |
| `campaign.config.json` | `5054902516e61fcd8c3a437362d693052411ef6c08b91c368c998863e5eecfc9` |
| `confirmation.md` | `cb50f6732a93277ba61922c91a5e61e7d1e1824aa9416bbfd0dc6663dd15ca1d` |
| `requirements-contract.md` | `df2e0be107baf2decd8acabac88c6371ab6014ba49aaf5fa65755d323710adbb` |
| `articles/EN-04/article.html` | `86af2774ea15cb6fc20641dd02e6ebac8e54eb694cfc32b8c9a1a86cd64db083` |
| `articles/EN-04/human-release/Tumblr/fingerprint.json` | `36d31aae752372395df92377518d674d7eee17c76d51e250a5b9a6d887db7770` |
| `articles/EN-04/human-release/Tumblr/visual-payload.html` | `514350c322f8cb461763723ced753e871dbd8a3063e540dc27df9de129b14454` |
| `articles/EN-04/r3/full-review-2.md` | `0da6b1ff47c2a259b328380a09dbb844dce487820f5b81d81c06fdf6aa9b9137` |
| `articles/EN-04/r3/rich-image-handoff-gate-2.md` | `cdb9137fb8344c688cc3cdffda2d994c2b2076c21b6fd6605ff69ce0c5ff27b2` |
| `articles/EN-04/r3/public-gate-report-1.md` | `22c73046344dabfdd1fcc702904cec5c49803e7746bc32879c40fbedadbb0396` |
| `articles/EN-04/r3/public-review-1.md` | `995d5dcbae77182cc8f6ad3472553bb0eab3da5fa6959ba71c57e182778165ab` |
| `articles/EN-04/r3/public-review-2.md` | `affa7fbe471542a48f47ad752b2d7b42f8f703460ff6df1ad7d2267aa6ec998b` |
| `articles/EN-04/evidence/public-reader-observation-1.md` | `ce2ed3d871424e6ec67c11082ca958c4e0cbc35ddde61735525f88d3e8a98844` |
| `articles/EN-04/evidence/public-reader-observation-2.md` | `3deaaaa21d1c7f8dea12e51dbd96ca76044fb8aad00247b6589ad5a4c78d07c4` |

The local package is an intended-structure baseline, not public proof. Its current fingerprint declares `SEPARATE_TITLE_FIELD`: semantic title level 1, zero body H1, six H2 sections, and the three named motion directions as H3. Full R2 and the bounded rich-image gate closed local findings only; neither is relabelled as native Tumblr or public-QA evidence.

## Finding continuity and exact mapping

### PUBLIC-HEADING-HIERARCHY-001 — OPEN — P1

| Mapping | Evidence |
| --- | --- |
| Frozen semantic structure | `fingerprint.json` and `transport-check.md`: 1 H1, 6 H2, 3 H3; the three motion directions are H3 under `Three controlled motion directions for a travel image`. |
| R-P1 public observation | `public-review-1.md` / `public-reader-observation-1.md`: 1 H1, 9 H2, 0 H3. |
| G-P1 disposition | `public-gate-report-1.md`: the stable finding is OPEN and requires public semantic-hierarchy parity. |
| Fresh R-P2 public observation | `public-review-2.md` / `public-reader-observation-2.md`: 7 H1, 3 H2, 0 H3. The title plus all six canonical H2 labels are H1; the three motion labels remain H2, not H3. |
| G-P2 disposition | The same stable finding remains OPEN. No new G-specific or speculative platform-cause finding is created. |

Textual parity does not close an element-type mismatch. The three intended subordinate headings have not been restored as semantic H3; the broader 1/6/3 frozen hierarchy is also not present on the public reader page. No conclusion is made about Tumblr controls, editor behavior, account authority, or whether the required correction is currently possible.

## Passed public fields retained from fresh R-P2 evidence

| Public surface | Disposition |
| --- | --- |
| Normalized body text, paragraph order, and four-item list | PASS — matches canonical HTML exactly after markup normalization (8,563 bytes). |
| Title text | PASS — canonical title remains the page and reader title text. |
| Founder disclosure | PASS — exact disclosure occurs once near the opening. |
| Seedance provider link | PASS — one exact `Seedance 2.5 page` anchor to `https://videoweb.ai/model/seedance-2-5/`. |
| MiniMax provider link | PASS — one exact `MiniMax H3 page` anchor to `https://videoweb.ai/model/minimax-h3/`. |
| Images, ALT, captions, and order | PASS — three image elements retain exact manifest ALT, their English captions, and LEAD/MIDDLE/CLOSING order. |
| Placeholder removal | PASS — no Chinese placeholder label, release filename marker, or yellow-placeholder instruction appears in reader text. |
| Observable metadata | PASS / observed — description begins with the canonical opening; post metadata reports three images and article type. |

## Minimal human-only next action

1. If the existing native Tumblr post can be corrected, a human restores only the frozen semantic map: one title H1, six major H2 sections, and the three named motion directions as H3 below their existing parent H2. Do not infer or test a platform control from this report.
2. Preserve the approved title text, prose, paragraph/list order, both exact provider href/anchor pairs, founder disclosure, three images, ALT, captions, order, metadata values, visibility, author/account identity, and public URL. Do not repost, replace, delete, or create another post.
3. The human returns the existing URL with an explicit `HUMAN_ACCEPTED` only after accepting the reader page, or `HUMAN_NEEDS_FIX` with the failed item. A correction then requires a fresh anonymous read-only R-P and a new fresh G-P; the same URL alone is insufficient evidence of either correction or acceptance.

## Acceptance and authority boundary

- No `PUBLIC_QA_PASSED`, completion, harvest, or campaign/root-state transition is made here.
- `HUMAN_ACCEPTED` remains independently required even if a future R-P finds exact public parity.
- This fresh G-P performed no browser, public-site, editor, account, CDP, upload, save, publish, repost, delete, visibility, sharing, MusicMaker, or root-state action. This article-local report is its sole write.
