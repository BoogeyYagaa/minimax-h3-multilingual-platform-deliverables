verdict: PUBLIC_REVIEW_CHANGES

重置到本清单逐条核对，只依据本轮产物与冻结需求。

# EN-02 Public R1 — Paragraph anonymous reader comparison

## Scope, role, and non-writing boundary

- Role: the existing independent EN-02 `ARTICLE_LANGUAGE_REVIEWER`, acting as `public_reviewer` (R-P) for EN-02 only. This review is limited to the public reader URL and the frozen EN-02 package. It does not modify the article, root R3 state, any platform, or any other article.
- Re-read in full: `writer-review-3p/SKILL.md`; the campaign configuration, confirmation, requirements contract, current R3 publication record for EN-02, assignment, research proposal/status, approved research R1, all Full R1–R5 reports, local G report, all four W resolutions, W handoff/lane status, canonical, product-facts boundary, and the full Paragraph package (payload, fingerprint, manifest, transport/local-SEO reference, release card, checklist, raw controls, and local images). I also re-read `evidence/EN-02-user-publication-url-and-image-limitations.json`.
- The local verifier still passes, but it is explicitly W-local static evidence only. It cannot establish a Paragraph editor, publication, human acceptance, or public rendering result. Its current local source hashes are canonical `157e52c0912f40a33dc21fb2b5065dbe9ba3d8a803a42df4bb9412d0a3f21ad2`, clean body `8b689fe1f1e57cc8364585aaac9b8e362a67304e5cbdaa2ebbff993645371f0d`, and visual payload `caaa4822c4995dded19971150731615f02f2537ff2b910bf625435b0a23ede4a`.
- This is a technical, read-only public comparison. The user-returned URL is not `HUMAN_ACCEPTED`; no G-P/public-QA decision is made here.

## Public reader evidence and read-only actions

The evidence record is [`../evidence/public-reader-1.json`](../evidence/public-reader-1.json), SHA-256 `4c3dae17b42d5879c3d9366b203190ad281984ac6bc78e64dc9409be367391f9`.

1. Attempted the permitted public read through the generic web reader. It rejected the `@` path as a non-retryable safe-open error; this is recorded as a tool limitation, not an accessibility conclusion.
2. Performed anonymous HTTPS `HEAD` and `GET` only on the supplied reader URL. Both returned HTTP 200 (`text/html`); the captured public HTML SHA-256 is `be9fa15d4a0a7fc22cc17102f062a9bae5eecc3365ef9756d7bae0500ded3cae`.
3. Performed anonymous HTTPS `HEAD` and `GET` only on the page's public Markdown-reader alternative. It returned HTTP 200 (`text/markdown; charset=utf-8`); SHA-256 `b06df52113e7f5f1e90c5f96433d94cfd34f4e2fb4c78f45a808d74d8e0e3751`.
4. Read the three public original-PNG URLs exposed by the reader page and SHA-256 checked their bytes. Each is byte-identical to its retained local image asset. No account, editor, upload, save, publish, delete, repost, or login operation occurred.
5. Read the desktop computer-use surface inventory only. It exposed no browser tab target, so no editor or logged-in browser route was opened and no screenshot was captured.

## Field-by-field reader comparison

| Surface | Frozen package | Public reader evidence | Result |
| --- | --- | --- | --- |
| URL and reader availability | Supplied Paragraph URL; public proof required | HTML and Markdown reader endpoints both return HTTP 200 at the evidence-record time. | PASS, time-bounded. |
| H1 and visible title | `A Short Video Launch Storyboard Template: From Opening Hook to Requested Action` | Public H1 is exact. The HTML document title retains that string with the platform/author suffix `— VideoWeb AI`. | PASS for H1 and title base; suffix observed as platform presentation. |
| Full body and order | Canonical/body transport is the frozen English reader sequence. | Independent normalization checked all 36 non-heading canonical blocks in order against the public Markdown reader source: 36/36 matched. No Chinese operator card, filename, ALT instruction, or status text appears in the reader body. | PASS. |
| H2/H3 map | Six H2 and four H3 entries in the fingerprint map. | Public HTML heading sequence exactly matches the local ten-entry H2/H3 map, including all four numbered H3 beats. | PASS. |
| Founder disclosure | `I am a founder of VideoWeb AI.` near the opening. | Exact sentence appears once, after the opening paragraph. | PASS. |
| Fixed Seedance link | Exact href once; descriptive anchor. | `https://videoweb.ai/model/seedance-2-5/` occurs once with `Seedance 2.5’s text, image, and optional reference-media workflow`. | PASS. |
| Fixed MiniMax link | Exact href once; descriptive anchor. | `https://videoweb.ai/model/minimax-h3/` occurs once with `MiniMax H3 workflow page`. | PASS. |
| Provider/fact boundary | VideoWeb is sentence-level provider attribution only; no official-vendor, benchmark, winner, result, price, availability, or performance conclusion. | The matched public body retains the provider sentence and its express exclusions. | PASS. |
| Public tags | Five frozen raw tags. | The public Markdown/meta record exposes all five concepts; `Seedance 2.5` and `MiniMax H3` are lower-cased by the public representation. | OBSERVED normalization; not a reader-copy mismatch. |
| Canonical/author/robots | Platform-controlled metadata remains observable where exposed. | Canonical equals the supplied URL; author is `VideoWeb AI`; robots is `index, follow, max-image-preview:large`. | OBSERVED. |
| SEO description/excerpt | Frozen raw value: `Plan one short launch clip from its opening hook to its requested action with a pre-generation storyboard template and a clear decision map.` | Public `description`, `og:description`, and JSON-LD description instead read: `Plan your launch clip before writing generation prompts. Use this four-beat decision map to align the opening hook, core message, visual reveal, and requested action in one reviewable order.` | `PUBLIC-RENDER-002` OPEN. |
| Local images retained | Three original PNGs, each 1664×936, with separate ALT/caption/placement records. | All three local assets remain in the package and their hashes/dimensions match manifest and fingerprint. This does not call them merely local placeholders or claim a local file is itself public proof. | PASS locally; public relationship verified below. |
| In-body image 01 | After disclosure and before first H2; paired caption. | Matching public PNG bytes appear after disclosure/before H2 with the exact caption. | PASS. |
| In-body image 02 | After the decision-map H2 and before its first paragraph; paired caption. | Matching public PNG bytes appear at that exact anchor with the exact caption. | PASS. |
| In-body image 03 | After the review H2 and before its first paragraph; paired caption. | Matching public PNG bytes appear at that exact anchor with the exact caption. | PASS. |
| Additional visible image | The frozen visual plan has no pre-disclosure cover placement; image 01's declared reader placement is after disclosure. | The public HTML contains a second visible render of image 01 after H1 and before the disclosure, in addition to the correctly placed in-body image 01. | `PUBLIC-RENDER-001` OPEN. |
| Public in-body ALT | The package retains three intended ALT strings. | The three in-body `<img>` elements have empty `alt` attributes; only the additional pre-disclosure cover uses the first intended ALT string. Captions are present for each in-body image. | `USER_REPORTED_PLATFORM_LIMITATION`; do not claim ALT was entered or persisted. |

## Findings and required human follow-up

### PUBLIC-RENDER-001 — OPEN

- **Severity:** Medium
- **Rule:** Public reader-visible visual order must not add an undeclared duplicate of a required narrative image. The declared lead image is after the founder disclosure, not a second pre-disclosure reader cover.
- **Evidence:** The static public reader sequence is public H1 → image 01 (proper ALT) → founder disclosure → image 01 again (empty ALT) → its caption → first H2. The three declared in-body positions otherwise pass and the PNG bytes match their local SHA-256 values.
- **Minimal `HUMAN_NEEDS_FIX`:** If Paragraph exposes a separate cover/feature-image setting, a human should remove only that extra cover while preserving the three correctly placed in-body images, captions, and body text. If the platform does not expose such a control, record that platform limitation with updated public evidence; do not alter the canonical article or attempt an editor workaround. Any public change requires a new R-P.

### PUBLIC-RENDER-002 — OPEN

- **Severity:** Medium
- **Rule:** The observable public description/excerpt must not silently replace the frozen raw SEO-description control with different copy when the package supplies an exact value.
- **Evidence:** The quoted public description differs from the exact frozen `SEO-DESCRIPTION.txt`/`title-and-metadata.md` value in the comparison table.
- **Minimal `HUMAN_NEEDS_FIX`:** A human should first determine whether Paragraph exposes a native description/excerpt control. If it does, use the exact frozen value and return fresh public-reader evidence; if it does not, record that platform-controlled limitation rather than manually changing canonical reader copy. Any public change requires a new R-P.

## Limitation attribution and UNVERIFIED surfaces

- The original user report that this **article** had no in-body images is not a permanent platform assertion. It is contradicted by this time-bounded public reader capture: all three in-body images and their captions are present. No missing-image finding is created.
- `USER_REPORTED_PLATFORM_LIMITATION`: the user reports that no ALT editing option exists for this article. The public source shows empty in-body `alt` attributes, so ALT is not reported as filled. This R-P did not enter an editor and therefore cannot independently prove whether an ALT UI control exists; no nonexistent-field remediation is demanded. The three local original images and their ALT/caption records remain retained canonical evidence, not a claim of public ALT persistence.
- `UNVERIFIED`: `HUMAN_ACCEPTED` has not been supplied; native editor field availability (including ALT and description), current account identity, any visual browser screenshot/responsive paint, rendered CDN-WebP pixels beyond declared 1600×900 HTML attributes, and an independent G-P decision. These are not inferred from the user URL, HTTP 200, local verifier, or public static source.
- Earlier local findings `VISUAL-NARRATIVE-001`, `PAYLOAD-TRANSPORT-001`, and `HANDOFF-STATE-001` remain resolved per Full R5. They are not reopened by the two new, public-render-only findings.

## Finding status

| Finding ID | Status | First report | Evidence |
| --- | --- | --- | --- |
| `VISUAL-NARRATIVE-001` | RESOLVED | `r3/full-review-1.md` | R2–R5 local re-checks; public in-body anchors also match. |
| `PAYLOAD-TRANSPORT-001` | RESOLVED | `r3/full-review-2.md` | Full R3–R5 local verifier/re-review. |
| `HANDOFF-STATE-001` | RESOLVED | `r3/full-review-3.md` | Full R5 local verifier/re-review. |
| `PUBLIC-RENDER-001` | OPEN | This report | `../evidence/public-reader-1.json` (public HTML and reader-source digests). |
| `PUBLIC-RENDER-002` | OPEN | This report | `../evidence/public-reader-1.json` (public description versus frozen raw value). |

`PUBLIC_REVIEW_CHANGES` is an R-P technical verdict only. It is not a publication instruction, human acceptance, G-P verdict, or final public-QA pass.
