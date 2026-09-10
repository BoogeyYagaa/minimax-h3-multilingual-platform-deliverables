verdict: PUBLIC_QA_CHANGES
role: ARTICLE_PUBLIC_GATE
gate: fresh independent public G-P; on-disk evidence only
article_id: EN-04
platform: Tumblr
public_url: https://www.tumblr.com/videowebai/827355403965890560/a-travel-photo-to-video-prompt-plan-three-motion?source=share
reviewed_at: 2026-09-10
human_accepted: NOT_YET_PROVIDED

# EN-04 Tumblr public gate 1

## Decision

`PUBLIC_QA_CHANGES`. The public evidence supports a real, anonymously readable Tumblr reader document rather than an HTTP-status shell, and it supports the R-P's passed comparisons for the approved body, title/H1, disclosure, both fixed provider links, and the three in-body image/ALT/caption placements. It also reproducibly shows one material public difference: Tumblr renders the three canonical subordinate motion headings as H2 rather than H3. That difference leaves prose and ordering intact but breaks the required public heading hierarchy.

This gate preserves R-P's stable finding `PUBLIC-HEADING-HIERARCHY-001` as `OPEN — P1`. No additional G-specific finding ID is needed: the existing ID precisely identifies the public reader difference and remains the repair/verification key.

`HUMAN_ACCEPTED` is still `NOT_YET_PROVIDED`, so this report cannot be `PUBLIC_QA_PASSED`, does not complete the article, and does not authorize harvest. The missing human acceptance did not block this technical assessment.

## Inputs read and SHA-256

| Input | SHA-256 |
| --- | --- |
| `campaign.config.json` | `5054902516e61fcd8c3a437362d693052411ef6c08b91c368c998863e5eecfc9` |
| `confirmation.md` | `cb50f6732a93277ba61922c91a5e61e7d1e1824aa9416bbfd0dc6663dd15ca1d` |
| `requirements-contract.md` | `df2e0be107baf2decd8acabac88c6371ab6014ba49aaf5fa65755d323710adbb` |
| `r3/state.json` (read-only scope/status input) | `39e234b62c26f7f1e984591f3027e7818d84f0cb6c86dc182a84068821ffb8f6` |
| `articles/EN-04/article.md` | `f964429defc48401a2a7ef37cefcd35570169ed6ffd1524ab8d892ded505a732` |
| `articles/EN-04/article.html` | `86af2774ea15cb6fc20641dd02e6ebac8e54eb694cfc32b8c9a1a86cd64db083` |
| `articles/EN-04/human-release/Tumblr/fingerprint.json` | `36d31aae752372395df92377518d674d7eee17c76d51e250a5b9a6d887db7770` |
| `articles/EN-04/human-release/Tumblr/release-package-metadata.json` | `57f0fbe9c76acbbeb921ee0080a633c28cecb59ccea5f9bf25438e9b045601b3` |
| `articles/EN-04/human-release/Tumblr/transport-check.md` | `58dc57b8782a0f2c1f61df68e82d93621c90a9a8ad624bda2fdd0633eb3470fa` |
| `articles/EN-04/human-release/Tumblr/image-manifest.md` | `a07f35ac199955d20b61e1f9b5421e1424d27785be8d4bb8b782bb0503df5fc6` |
| `articles/EN-04/r3/full-review-2.md` | `0da6b1ff47c2a259b328380a09dbb844dce487820f5b81d81c06fdf6aa9b9137` |
| `articles/EN-04/r3/gate-report-1.md` | `e20f18c72d069adaf3e0fe624681db8cdf61aa15e051ed911c8b4b0a70c5d6e5` |
| `articles/EN-04/r3/rich-image-instruction-delta-review-2.md` | `4953b8c32df510fa7cbff0912d297773f71c240a73ee4aeeff45ecda5c04745f` |
| `articles/EN-04/r3/rich-image-handoff-gate-2.md` | `cdb9137fb8344c688cc3cdffda2d994c2b2076c21b6fd6605ff69ce0c5ff27b2` |
| `evidence/EN-04-user-publication-url.json` | `d90a7bc6e87b76550d3a35ba198257dfe93d13b0a96181374598a53e01e5bf12` |
| `articles/EN-04/r3/public-review-1.md` | `995d5dcbae77182cc8f6ad3472553bb0eab3da5fa6959ba71c57e182778165ab` |
| `articles/EN-04/evidence/public-reader-observation-1.md` | `ce2ed3d871424e6ec67c11082ca958c4e0cbc35ddde61735525f88d3e8a98844` |

All earlier EN-04 research, Full R1/R2, resolution, local gate, rich-image delta, rich-image instruction resolution, and local gate-2 records were read as local baseline only. No historical local PASS is relabelled as public proof.

## Evidence separation

### Local package baseline — not public proof

The local package fixes EN-04 to the confirmed Tumblr/account alias and declares `SEPARATE_TITLE_FIELD`: one title H1 plus a body map of six H2 and three H3 headings. Full R2 approved the canonical/release reader surfaces, and the bounded local gate-2 closed only the rich-image handoff instruction conflict. Those local records establish the intended structure, exact two links, disclosure, and LEAD/MIDDLE/CLOSING image contract. They cannot establish how Tumblr rendered the live document.

### Public reader proof — the required G-P evidence surface

The R-P's anonymous read-only observation captured `HTTP/2 200` with an actual Tumblr post container at `Thu, 10 Sep 2026 08:15:55 GMT`, response-envelope SHA-256 `6c1c546336be951f2bdfea9fe0e2758d148fa835dd18a8f837bf7606478e91d1` (141,785 bytes). It records 8,563 bytes of normalized reader text equal to canonical HTML and verifies the following public surfaces:

| Public surface | G-P disposition from R-P evidence |
| --- | --- |
| Full prose, paragraph order, and four-item list | PASS |
| Public title / H1 | PASS — one canonical-title H1 |
| Founder disclosure | PASS — exact disclosure once near the opening |
| Required provider link 1 | PASS — `Seedance 2.5 page` → `https://videoweb.ai/model/seedance-2-5/`, once |
| Required provider link 2 | PASS — `MiniMax H3 page` → `https://videoweb.ai/model/minimax-h3/`, once |
| Images / ALT / captions / placement | PASS — three public images with the manifest ALT and one matching caption at the LEAD, MIDDLE, and CLOSING boundaries |
| Operator-placeholder removal | PASS — no Chinese placeholder, filename marker, or yellow instruction text in reader text |
| Observable metadata | PASS / observed — description starts with the canonical opening; `og:title` reports three images; `og:type` is `article`; `og:url` removes only the sharing query |
| Heading semantics | CHANGES — see the open finding below |

## Open public finding

### PUBLIC-HEADING-HIERARCHY-001 — OPEN — P1

- **Canonical requirement:** one H1, six H2 headings, and three H3 motion directions subordinate to `Three controlled motion directions for a travel image`.
- **Public observation:** one H1, nine H2 headings, and zero H3 headings. The three numbered motion labels retain their text and order but are public H2 elements.
- **Impact:** the reader-visible prose is not lost or reordered, but the public semantic hierarchy differs from the approved canonical/release hierarchy.
- **Disposition:** `PUBLIC_QA_CHANGES`; this is a repairable reader-page difference, not a basis to infer a Tumblr cause, a deletion, account state, or a need to alter approved content.

## Minimal human-only repair and recheck

1. A human, using the existing native Tumblr post, restores only the three numbered motion-direction labels to subordinate H3 semantics beneath their existing parent H2.
2. Preserve the approved text, title, body order, exact two anchors/hrefs, founder disclosure, all three images, ALT values, captions, positions, metadata values, author/account identity, visibility, and public URL. Do not repost or create a replacement post.
3. After that human correction, resume the original EN-04 R for a new read-only R-P of the corrected public reader page, then dispatch a **new fresh G-P**. Neither this report nor the R-P authorizes an automated editor action, edit, upload, publication, republish, share, deletion, account change, or visibility change.

If the native editor does not expose a way to restore those subordinate semantics, record that observed limitation rather than inventing a cause or using an alternative publication/account route. It remains a human decision whether to pursue any platform-side correction.

## Remaining UNVERIFIED boundaries

- `HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`; final human acceptance is separate from this technical G-P and is still required for completion.
- The public `@videowebai` label and reader metadata do not prove account ownership, current login state, or authorization to edit.
- The specific native control/path capable of restoring H3 semantics has not been inspected and is not assumed.
- The corrected public reader page does not yet exist in evidence; its title/body/link/image/metadata parity and its heading semantics must be freshly re-read after a human correction.
- Remote image asset bytes and post-repair painted rendering were not separately retrieved as byte-identical local assets. The current public evidence does, however, verify the three actual reader-image elements, their ALT values, captions, and specified positions.
- No `PUBLIC_QA_PASSED`, completion, harvest, or root-state transition is made by this report.

## Guardrails and status ownership

No browser, CDP, login, editor, upload, publish, repost, delete, share, visibility, account, or MusicMaker action was performed. This report is the only file written by this fresh G-P. `r3/state.json` is read-only here; campaign-controller state updates, if any, remain the root controller's responsibility.
