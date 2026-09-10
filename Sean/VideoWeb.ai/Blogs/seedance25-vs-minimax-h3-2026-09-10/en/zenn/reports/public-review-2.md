verdict: PUBLIC_REVIEW_CHANGES

# EN-09 public reader review 2 (R-P)

## Scope and fresh evidence

- Article/platform: `EN-09` / Zenn / public `videowebai` reader page only.
- Public URL: <https://zenn.dev/videowebai/articles/cf88a1bb43802d>
- Frozen canonical SHA-256: `1458b6dfa2d24ebc4b5ff1a8339985383ca839c19f5d4f5c561323075ebe54b7`; release-fingerprint SHA-256: `705a8f3fc64539ce47c5c9aebb64958a96bda5ccb83eca79a19e685fe87156b9`.
- Fresh anonymous evidence: [`../evidence/public-reader-observation-2.json`](../evidence/public-reader-observation-2.json), SHA-256 `e0b4e8fecafbab1dd2f3723fa91f788aa44baea0a783b362545d3d9c6b776f8d`. It is a full parsed reader-body snapshot plus direct anonymous reads of all three public image URLs, not an HTTP-status-only check.
- No editor, account, login, upload, save, publication, repost, deletion, visibility, or other external write was used. This R-P does not make a G-P decision.

## Field comparison

| Reader field | Frozen expectation | Fresh anonymous public observation | Result |
| --- | --- | --- | --- |
| Route | Zenn public reader route returned by the user | `200 text/html`; canonical URL is exactly the supplied article URL and full reader content was parsed | PASS |
| Native title | Exact plain text: `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing` | Document title, Open Graph title, and sole native H1 are all `AI Video Prompt Iteration Workflow: One Attempt, One Thing.` | **FAIL — PUBLIC-RENDER-001 remains OPEN** |
| Literal Markdown title control | No literal `#` in the title field | No literal `#` appears in the native title, document title, or Open Graph title | PASS; partial repair verified |
| H1 transport | `SEPARATE_TITLE_FIELD`: one native H1 and zero reader-body H1 elements | Exactly one document H1, the native title; `body_h1_count: 0` | PASS; the former duplicate body H1 is gone |
| Reader body/order | Canonical reader text, excluding the separate title and image transport | 51 expected and 51 observed normalized text units; zero differences after Markdown-link normalization; body begins with the exact founder disclosure | PASS |
| H2/H3 | Frozen eight-H2/three-H3 ordered map | All eleven expected H2/H3 headings and their order remain intact | PASS |
| Provider links | Two exact descriptive anchor/href pairs | Both anchors and hrefs exactly match `links.md` and the fingerprint | PASS |
| Disclosure and fact boundaries | Opening founder disclosure; provider-attributed, non-benchmark/non-winner framing | Disclosure is the first body element and the approved boundary text remains in the body | PASS |
| Images 1–3 | Public platform URLs, exact ALT/caption, lead/middle/closing locations | Three public Zenn PNG resources return `200 image/png`; exact ALT/caption pairs and order remain. Image 2 remains after the optional-note section and before the provider-description H2 | PASS |
| Reader-copy contamination | No Chinese cards, filenames, local paths, HTML comments, or operator text | None of those artifacts occurs in the parsed reader body | PASS |

## Stable public finding status

### PUBLIC-RENDER-001 — OPEN (partially repaired)

This is the same finding opened in `public-review-1.md`; no new public finding is created. Its two previously observed subparts are now resolved by fresh public evidence: the literal leading `#` is gone, and the frozen title no longer reappears as a reader-body H1. However, the sole public native title/H1 is still the shortened `AI Video Prompt Iteration Workflow: One Attempt, One Thing.`, not the exact frozen platform title `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing`.

The remaining title mismatch keeps `PUBLIC-RENDER-001` OPEN and prevents `PUBLIC_REVIEW_APPROVED`. The anonymous reader evidence establishes only the current output; it does **not** establish a title-length limit, an unavailable native title control, or any other platform limitation.

### Minimal human repair gate

`HUMAN_NEEDS_FIX`: a human must either make the native title exactly match the frozen plain-text platform title and return the page for another anonymous R-P, or provide an observed native-control limitation for G to assess. Do not alter the already-matching reader body, headings, links, disclosure, images, captions, ALT, tags, or fact-boundary text. No local W revision is indicated because the canonical/release package already contains the expected title and the reader body now matches it.

## UNVERIFIED and non-promotions

- `HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. The same returned URL, a partial title repair, and this reader comparison do not create human acceptance or complete public QA.
- Native-editor field capabilities—including any title length or control limitation—are `UNVERIFIED`. This report makes no claim that the remaining mismatch is editable or non-editable.
- Public image delivery produces platform PNG variants rather than source-byte identity with local 1664×936 originals. Their live URLs, PNG responses, ALT, captions, and positions are verified; source-byte equality after platform transformation is not asserted.

## Integrity and exact read-only actions

- Public document SHA-256: `4333184d4dd785fc7b7803ebba99de09bb11357f5b7377b14161107d90e35253`; parsed body HTML SHA-256: `77dcbffd7f21b827f5b0de9cfee1e8c9ceb3d6da2e9cb6c8aab0633625030ad9`; normalized reader-text SHA-256: `1ffeccf8e79a86d75edbe460ac9052d8f0c13db6222811527f455578cc28b408`.
- Exact external actions are recorded in the evidence file: one anonymous public GET of the reader page and one anonymous public GET of each of its three inline image URLs. All four were read-only.
