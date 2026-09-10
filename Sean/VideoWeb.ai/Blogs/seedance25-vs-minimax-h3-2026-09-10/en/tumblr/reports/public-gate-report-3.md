verdict: PUBLIC_QA_CHANGES
role: ARTICLE_PUBLIC_GATE
gate: fresh independent public G-P; on-disk evidence only
article_id: EN-04
platform: Tumblr
public_url: https://www.tumblr.com/videowebai/827355403965890560/a-travel-photo-to-video-prompt-plan-three-motion?source=share
reviewed_at: 2026-09-10
human_accepted: NOT_YET_PROVIDED

# EN-04 Tumblr public gate 3

## Decision

`PUBLIC_QA_CHANGES` remains the only supported verdict. Current R-P3 is `PUBLIC_REVIEW_CHANGES`, and its fresh anonymous reader observation records an actual Tumblr post whose normalized reader text still exactly matches the canonical HTML. The public semantic map is now **1 H1 / 6 H2 / 0 H3**, while the frozen canonical/release map is **1 H1 / 6 H2 / 3 H3**. Therefore the stable public finding `PUBLIC-HEADING-HIERARCHY-001` remains **OPEN — P1**.

There is a real but incomplete structural recovery from R-P2: the sole title H1 and all six major-section H2 elements are again semantically correct. The unresolved part is exact and limited: `Atmospheric drift`, `Surface pulse`, and `Light transition` remain present in the correct reader-text order but are not semantic H3 elements. This does not close the whole 1/6/3 requirement.

The user returning the same public URL for the round-3 recheck is not proof of repair and is not `HUMAN_ACCEPTED`. The URL receipt and both recheck requests expressly retain `HUMAN_ACCEPTED: NOT_YET_PROVIDED`. Consequently this report does not complete EN-04, authorize harvest, or make a campaign/root-state transition.

## Current evidence and input integrity

| Input | SHA-256 |
| --- | --- |
| `campaign.config.json` | `5054902516e61fcd8c3a437362d693052411ef6c08b91c368c998863e5eecfc9` |
| `confirmation.md` | `cb50f6732a93277ba61922c91a5e61e7d1e1824aa9416bbfd0dc6663dd15ca1d` |
| `requirements-contract.md` | `df2e0be107baf2decd8acabac88c6371ab6014ba49aaf5fa65755d323710adbb` |
| `r3/state.json` (read-only status input) | `3503d533b9415878e73b1e117d70c60d8b8cb9b36da61e02cedec94009e4a13a` |
| `articles/EN-04/article.md` | `f964429defc48401a2a7ef37cefcd35570169ed6ffd1524ab8d892ded505a732` |
| `articles/EN-04/article.html` | `86af2774ea15cb6fc20641dd02e6ebac8e54eb694cfc32b8c9a1a86cd64db083` |
| `articles/EN-04/human-release/Tumblr/content.md` | `d3f7b26caf0b312204ded94695aa00142a26e5535176fc21614242e229377ac2` |
| `articles/EN-04/human-release/Tumblr/fingerprint.json` | `36d31aae752372395df92377518d674d7eee17c76d51e250a5b9a6d887db7770` |
| `articles/EN-04/human-release/Tumblr/visual-payload.html` | `514350c322f8cb461763723ced753e871dbd8a3063e540dc27df9de129b14454` |
| `articles/EN-04/r3/full-review-2.md` | `0da6b1ff47c2a259b328380a09dbb844dce487820f5b81d81c06fdf6aa9b9137` |
| `articles/EN-04/r3/gate-report-1.md` | `e20f18c72d069adaf3e0fe624681db8cdf61aa15e051ed911c8b4b0a70c5d6e5` |
| `articles/EN-04/r3/public-review-1.md` | `995d5dcbae77182cc8f6ad3472553bb0eab3da5fa6959ba71c57e182778165ab` |
| `articles/EN-04/r3/public-gate-report-1.md` | `22c73046344dabfdd1fcc702904cec5c49803e7746bc32879c40fbedadbb0396` |
| `articles/EN-04/r3/public-review-2.md` | `affa7fbe471542a48f47ad752b2d7b42f8f703460ff6df1ad7d2267aa6ec998b` |
| `articles/EN-04/r3/public-gate-report-2.md` | `79c7b7b7b0669b2f08c139d5ad26a67abf0eefcbe283fb9292b54a1f7626c8f1` |
| `articles/EN-04/r3/public-review-3.md` | `845fb6e86c81c24407dbc5bdb5b2f5aaa0b4ff3e5fde789a31aee3596af819a3` |
| `articles/EN-04/evidence/public-reader-observation-1.md` | `ce2ed3d871424e6ec67c11082ca958c4e0cbc35ddde61735525f88d3e8a98844` |
| `articles/EN-04/evidence/public-reader-observation-2.md` | `3deaaaa21d1c7f8dea12e51dbd96ca76044fb8aad00247b6589ad5a4c78d07c4` |
| `articles/EN-04/evidence/public-reader-observation-3.md` | `d0b1f719a550d45447f1f766ead513e4025e737f2b6706195ff539223d2e4c46` |

The current package fingerprint declares `SEPARATE_TITLE_FIELD`: title semantic level 1, no body H1, six H2 sections, and the three named motion directions as H3. Independent local checks confirm the current canonical/release hashes match that fingerprint. Full R2, local G1, and the bounded rich-image instruction R/G lineage were read as local baseline only; none is relabelled as public-reader proof.

R-P3's no-cache anonymous observation was collected at `Thu, 10 Sep 2026 09:27:29 GMT`: HTTP/2 200 with an actual post container, response-envelope SHA-256 `5fe5134ad3dd7a021b1b0596473b1d83b7689f265e7e8083337e14b0fcef8643`, and 8,563 bytes of normalized reader text equal to canonical HTML.

## Finding continuity and partial resolution

### PUBLIC-HEADING-HIERARCHY-001 — OPEN — P1

| Evidence round | Public semantic map | Disposition |
| --- | --- | --- |
| R-P1 | 1 H1 / 9 H2 / 0 H3 | OPEN |
| R-P2 | 7 H1 / 3 H2 / 0 H3 | OPEN |
| R-P3 | 1 H1 / 6 H2 / 0 H3 | H1 and all six major H2 elements restored; all three required motion-direction H3 elements remain missing. OPEN. |
| Frozen canonical/release target | 1 H1 / 6 H2 / 3 H3 | Required for resolution. |

The required missing H3 map is:

- `1. Atmospheric drift: let the mood move, not the location`
- `2. Surface pulse: focus attention on one abstract rhythm`
- `3. Light transition: interpret a memory without rewriting its time`

The unchanged stable ID covers this remaining semantic mismatch. No additional G-specific finding and no inferred platform-cause finding is created.

## Passed public-reader surfaces retained from R-P3 evidence

| Surface | Disposition |
| --- | --- |
| Actual reader document | PASS — actual post container, not an HTTP-status shell. |
| Full body, paragraph order, and four-item list | PASS — normalized reader text exactly equals canonical HTML. |
| Title and major sections | PASS — one canonical title H1 and all six frozen H2 labels in the frozen order. |
| Founder disclosure | PASS — exact disclosure occurs once near the opening. |
| Required provider links | PASS — each exact anchor/href pair occurs once: `Seedance 2.5 page` → `https://videoweb.ai/model/seedance-2-5/`; `MiniMax H3 page` → `https://videoweb.ai/model/minimax-h3/`. |
| Images | PASS — three images retain manifest ALT, one matching English caption each, and the intended LEAD/MIDDLE/CLOSING positions. |
| Placeholder removal | PASS — no Chinese placeholder label, release filename marker, or yellow instruction remains in public reader text. |
| Observable metadata | PASS / observed — description begins with the canonical opening; public metadata reports three images and article type. |

## Minimal human-only repair

1. If the existing native Tumblr post can be corrected, a human restores only the three named motion-direction labels above to semantic H3 beneath `Three controlled motion directions for a travel image`.
2. Preserve the current sole H1, six H2 elements, title text, body/list order, exact two anchor/href pairs, founder disclosure, three image files, ALT, captions, positions, metadata values, visibility, author/account identity, and this public URL. Do not repost, replace, delete, or create a new post.
3. If the human cannot make that limited semantic correction, record the observed limitation and failed checklist item. Do not infer a cause, control, or workaround from this report.
4. After a human correction, obtain a fresh anonymous read-only R-P for the existing URL and then a new fresh G-P. No editor or public-site action is authorized by this report.

## Acceptance and authority boundary

`HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. Even a future technical 1/6/3 match cannot produce `PUBLIC_QA_PASSED` without explicit human acceptance of the reader page. Conversely, a returned URL, HTTP 200, screenshot, local release readiness, or a public-reader comparison is not acceptance.

No browser, public-site, editor, login, account, CDP, upload, edit, save, publish, repost, delete, visibility, sharing, MusicMaker, or root-state action was performed. This report is the only file written by this fresh G-P; campaign-controller state ownership remains outside this task.
