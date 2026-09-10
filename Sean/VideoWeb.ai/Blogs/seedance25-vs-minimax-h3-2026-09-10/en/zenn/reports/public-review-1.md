verdict: PUBLIC_REVIEW_CHANGES

# EN-09 public reader review 1 (R-P)

## Scope and evidence boundary

- Article: `EN-09`; platform/account reader route: Zenn / `videowebai`.
- Public URL reviewed: <https://zenn.dev/videowebai/articles/cf88a1bb43802d>
- Canonical release fingerprint: `HUMAN_RELEASE_FINGERPRINT@1`; canonical `article.md` SHA-256 `1458b6dfa2d24ebc4b5ff1a8339985383ca839c19f5d4f5c561323075ebe54b7`; expected platform title: `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing`.
- Reader evidence: [`../evidence/public-reader-observation-1.json`](../evidence/public-reader-observation-1.json). It records the anonymized public document/body hashes, exact reader observations, and the four anonymous HTTPS GETs. No editor, account, upload, save, publication, visibility, or retry action was taken.
- The reader content itself was obtained and parsed. This is therefore not an HTTP-status-only finding. Earlier local R2 and G1 approval established only local package/release readiness; this R-P concerns the actual public reader render.

## Field comparison

| Reader field | Frozen local expectation | Public observation | Result |
| --- | --- | --- | --- |
| Canonical/public route | The user-supplied Zenn article URL | Canonical link and `og:url` are exactly `https://zenn.dev/videowebai/articles/cf88a1bb43802d`; anonymous reader body is present | PASS |
| Native title and semantic H1 | One separate-title-field H1: `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing`; body H1 count `0` | Document title, `og:title`, and native article-header H1 read `# AI Video Prompt Iteration Workflow: One Attempt, One Thing.`; the expected title appears again as a body H1 | **FAIL — PUBLIC-RENDER-001** |
| Reader body and order | Same reader text as `content.md` / canonical, excluding platform image transport | 52 expected and 52 observed text units; zero differences after normalizing Markdown link syntax. The disclosure, restrained provider attribution, and no-winner/no-price/no-benchmark boundaries remain present | PASS |
| H2/H3 map | Eight H2 and three H3 entries in the release fingerprint, in order | All eleven expected H2/H3 headings and their order are present | PASS |
| Required VideoWeb links | Two exact href/anchor pairs | Both exact anchors and hrefs are present: `its Seedance 2.5 workflow page` → `https://videoweb.ai/model/seedance-2-5/`; `its MiniMax H3 workflow page` → `https://videoweb.ai/model/minimax-h3/` | PASS |
| Disclosure | Founder disclosure at the opening | Exact disclosure is present before the introductory body text | PASS |
| Three reader images | Three 16:9 editorial images, public delivery URLs, exact ALT/caption, lead/middle/closing placement | Three `static.zenn.studio/user-upload` PNGs load anonymously as `200 image/png`; their ALT text/captions and insertion order match the manifest. Image 2 is after the optional-note section and directly before the provider-description section | PASS |
| Clean reader body | No Chinese release cards, filenames, ALT/control text, local Markdown paths, or image-placeholder comments | The parsed reader body has no Chinese characters, HTML comments, source filenames, or `./` local paths. Images use public platform URLs. The literal `#` remains only in the malformed native title identified above | PASS except PUBLIC-RENDER-001 |
| Observable metadata | Public title, author/date, canonical route, native topic normalization | Author `VideoWeb AI` / `videowebai`, published `2026-09-10T08:19:59+00:00`, type `idea`, `should_noindex: false`, and five normalized topic slugs are observable. Zenn exposes a generic `zenn:description`, not the local raw SEO description; the package had already marked that native field mapping unverified | PASS for observable fields; SEO-description field is UNVERIFIED, not silently asserted |

## Stable public finding

### PUBLIC-RENDER-001 — OPEN — native title/H1 transport is not the frozen public title

The anonymous reader exposes a literal Markdown `#` and the shortened native title `AI Video Prompt Iteration Workflow: One Attempt, One Thing.` in the document title, Open Graph title, and article-header H1. The frozen separate title field instead requires `AI Video Prompt Iteration Workflow: Review One Attempt, Then Change One Thing`. The latter is present as an additional body H1, even though the release fingerprint requires the pasted body to contain zero H1 headings.

This is a reader-visible title/H1 parity failure, not a change to the otherwise matching article body. Required repair: in the authorized native editor, set the separate title field to the exact frozen platform title without a `#`, and remove only the Markdown H1 from the reader body so that the body begins with the disclosure. Preserve the verified body text/order, two CTA pairs, three image URLs/ALT/captions/positions, disclosure, tags, and fact-boundary language. A fresh anonymous R-P read is required after that human repair.

Writer gate: **CHANGES_REQUIRED** (PUBLIC-RENDER-001 must be closed by a fresh public reader check).

## UNVERIFIED and non-promotions

- `HUMAN_ACCEPTED` remains **NOT_YET_PROVIDED** in `evidence/EN-09-user-publication-url.json`. The supplied public URL proves neither human acceptance nor complete public QA.
- No native-editor metadata field was entered or inferred. The local raw SEO title/description mapping remains UNVERIFIED where Zenn does not expose it on the reader page.
- The three public Zenn image delivery variants have different bytes/dimensions from the original 1664×936 local files, so source-byte identity after platform delivery transformation is not claimed. Their actual reader URLs, `200 image/png` responses, ALT, captions, and placement are verified in the evidence file.
- This is an R-P result only; it makes no G-P decision.

## Integrity and external read-only actions

- Reader snapshot SHA-256: `c565bf49914cc3c4ed2cce54a625b1764b40410cd87cd864e7c5ee167e1da10f`; parsed public body HTML SHA-256: `21f7c5553b4906cd5735b2fdccda5e3a1663382dac651f8d95bc71173d01acbb`; normalized reader-text comparison SHA-256: `6e3016106a8726fd6289c4735fb5ab3d48ca8fdd59963524b56c82f58187ce93`.
- Exact external actions are listed in the evidence file: one anonymous public reader GET and one anonymous public GET for each of the three inline image URLs. All were read-only. The preliminary Web-reader open was blocked by its URL-safety layer and supplied no content; it was not used as page evidence.
