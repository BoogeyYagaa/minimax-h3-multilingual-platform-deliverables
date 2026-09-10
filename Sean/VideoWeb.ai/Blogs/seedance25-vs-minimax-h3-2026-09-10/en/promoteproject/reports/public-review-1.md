verdict: PUBLIC_REVIEW_CHANGES
review_scope: public_reader_readonly
article_id: EN-08
platform: PromoteProject / VIDEOWEB_OWNER_ACCOUNT_PRIORITY
public_url: https://www.promoteproject.com/article/227862/seedance-25-vs-minimax-h3-a-video-creative-testing-plan-for-short-video-creation

# EN-08 independent public reader review 1

## Scope, evidence, and boundary

This is the same article-scoped R performing an anonymous public-reader comparison only. I re-read the frozen campaign/confirmation/requirements/state records; EN-08 canonical article and release package/fingerprint; all EN-08 R1/R2, repair, and G reports; the current reviewer registration; product-fact boundaries; and the user-returned URL receipt. I did not open an editor, account, login, browser profile, or publishing surface, and did not alter article content, release artifacts, root state, or any external system.

The public URL returned HTTP 200 as `text/html; charset=UTF-8` in a fresh HTTPS retrieval with no supplied session or cookie jar. The machine-readable observation is [public-reader-1.json](../evidence/public-reader-1.json), SHA-256 `81daee0290cdad0dc07e9d30814d591ca1c96a04022866385f6be0e581333a51`. Its public document SHA-256 is `92060d14bfdb3246ae77ef08cb182a17951166b5d0bb90a8f1cff035646a579d`; the extracted article-body fragment SHA-256 is `c54615ef3ec4b125e0d8d4c779539a89629a829db9f39b2b335247850f00a33c`.

`canonical_payload_fingerprint`:

- Reader body: `39ff0e9aa200f1d8bd969d830b9c9814564ccc69f50b021d94a925a167d5f2a8`
- Canonical article HTML: `0a1b82b37177979919af779b903d7879bd914c700eb3fd0d668966f6abf57804`
- Visual payload: `7c2b43f57b281f39931d790bc07e0d2dad6a1d5a284770b8b1ababd973a31905`
- Fingerprint file: `93457d23f045547a0964ae4884dfc0c667871c2d3c186668a7fd625b76e29c45`
- Heading transport: `SEPARATE_TITLE_FIELD`; expected title as platform H1, body H1 count `0`, H2 count `8`, H3 count `3`.

The returned public URL is status/accessibility evidence only. `HUMAN_ACCEPTED` is still `NOT_YET_PROVIDED`; this report is neither human acceptance nor a public gate decision.

## Field-level public comparison

| Field | Frozen canonical/package value | Public reader observation | Result |
| --- | --- | --- | --- |
| Title / H1 | `Seedance 2.5 vs MiniMax H3: A Video Creative Testing Plan for Short Video Creation` | Exact title in document title, Open Graph title, and the article's public H1. Other page H1s are platform chrome/modal, not the article title. | PASS |
| Body completeness and order | Canonical body after the separate title; 41 non-image/non-caption normalized body units | All 41 units occur in order in the public article fragment. No textual body unit was missing after whitespace and inline-markup normalization. | PASS |
| Body H1 transport | `0` | `0` in the article-body fragment | PASS |
| H2 transport | Eight expected H2 headings | Only five are H2. `What a video creative testing plan is—and is not`, `Declare one creative variable: the opening hook`, and `FAQ` are plain `<p>` elements followed by `<br>`. | FAIL — `PUBLIC-RENDER-001` |
| H3 transport | Three FAQ questions | All three public H3 strings and order match the fingerprint. | PASS |
| Founder disclosure | Visible before the intended lead image | Exact disclosure substance is visible near the start of the article. However, the observed platform cover appears after the H1 and before the disclosure; no approved intended lead image is public. | FAIL — covered by `PUBLIC-RENDER-002` |
| Google method source | `Google Ads’ video-experiment documentation` → exact Google Ads href once | Exact anchor/href pair occurs once. | PASS |
| Fixed VideoWeb CTA 1 | `Seedance 2.5 short-video workflow` → `https://videoweb.ai/model/seedance-2-5/` once | Exact anchor/href pair occurs once. | PASS |
| Fixed VideoWeb CTA 2 | `VideoWeb’s MiniMax H3 workflow page` → `https://videoweb.ai/model/minimax-h3/` once | Exact anchor/href pair occurs once. | PASS |
| Provider/experiment boundary | Provider-attributed workflow descriptions; eligible paid-video campaign, control, one declared creative variable, platform prerequisites, selected metric, and no executed-test/result/winner claim | These reader-visible constraints remain. I found no public performance/growth result, benchmark, winner, price, free-entitlement, or official model-maker-provenance assertion. | PASS |
| Temporary image cards | Three Chinese operation cards must not enter the reader page | None of the three card markers or canonical local filenames appears in the public article source. | PASS |
| Planned reader images/captions | Three reviewed exact-16:9 assets at LEAD/MIDDLE/CLOSING, with matching ALT/caption | Article-body `<img>` count is `0`; none of the three planned captions or filenames appears. One responsive platform cover is present before the body, but it is not verifiably any planned asset and has empty ALT/no caption. | FAIL — `PUBLIC-RENDER-002` |
| SEO description / tags | Raw description: `Build a video creative testing plan for short video creation: define one opening-hook variable, a control, platform prerequisites, and a selected metric.` Raw tags: `Video Creative Testing Plan, Short Video Creation, Seedance 2.5, MiniMax H3, Paid Video Campaigns` | Public description is platform-generated/truncated text; public meta keywords are `seedance,2.5,minimax,h3`; visible tags are `SEEDANCE`, `2.5`, `MINIMAX`, `H3`; JSON-LD adds generic startup keywords. | FAIL — `PUBLIC-RENDER-003` |

## Stable public findings

### PUBLIC-RENDER-001 — OPEN

- **Severity:** High
- **Rule:** The separate-title field transport keeps the article title as the platform H1 while preserving every canonical body H2/H3 semantic heading.
- **Observed:** Three frozen H2 headings are public paragraph elements, not H2 elements: `What a video creative testing plan is—and is not`, `Declare one creative variable: the opening hook`, and `FAQ`. The text remains in the correct body order; this is a semantic/navigation transport loss, not missing prose.
- **Evidence:** [public-reader-1.json](../evidence/public-reader-1.json) → `reader_text_and_structure.expected_h2`, `observed_h2`, and `h2_downgraded_to_p`.
- **Minimal correction target:** Preserve these three existing strings, in place, as H2 elements. No canonical wording, URL, or claim change is requested. Native editability is `UNVERIFIED`.

### PUBLIC-RENDER-002 — OPEN

- **Severity:** High
- **Rule:** The public reader page must carry the three declared LEAD/MIDDLE/CLOSING editorial planning images at their canonical semantic anchors, with the reviewed ALT/captions; a generic cover cannot substitute without public identity/placement parity.
- **Observed actual image state:** The source exposes one logical responsive cover after the title and before the disclosure/body: desktop `https://www.promoteproject.com/img/articles/227862.jpg` (`alt=""`, HTML `800×600`) and mobile `https://www.promoteproject.com/img/thumbs/227862.jpg` (`alt=""`, HTML `400×300`). The article-body fragment has zero `<img>` elements; all three planned captions and local planned filenames are absent. Thus no public in-body MIDDLE or CLOSING image exists, the lead is not publicly attributable to approved image 01, and the actual cover reverses the expected disclosure-before-planned-lead order.
- **Evidence:** [public-reader-1.json](../evidence/public-reader-1.json) → `images`; expected assets and exact local 16:9 SHA-256 values are in [fingerprint.json](../human-release/PromoteProject/fingerprint.json) and [image-manifest.md](../human-release/PromoteProject/image-manifest.md).
- **Minimal correction target:** Restore the three already-approved canonical assets at their declared LEAD/MIDDLE/CLOSING positions, with their reviewed captions and ALT where the native platform exposes that field. The target preserves the standing-bottle control → same-bottle hand-lifting treatment in image 02 and the local 16:9 asset identity; it does not ask for any content rewrite. Native controls and their availability are `UNVERIFIED`.

### PUBLIC-RENDER-003 — OPEN

- **Severity:** Medium
- **Rule:** The raw SEO description and raw TAGS remain separately mapped reader/search fields and must not silently become a different authored metadata value.
- **Observed:** Title/OG title match, but public description, meta keywords, visible tags, and JSON-LD keywords differ from the frozen raw values listed above.
- **Evidence:** [public-reader-1.json](../evidence/public-reader-1.json) → `metadata`; canonical raw controls in [title-and-metadata.md](../human-release/PromoteProject/title-and-metadata.md).
- **Minimal correction target:** If the native post actually exposes author-controlled SEO-description and tag fields, map the frozen raw values to those fields; otherwise retain the difference as platform-controlled/unverified evidence. This review does not infer the field's availability or request an editor retry.

## Minimal HUMAN_NEEDS_FIX record

This is a target-state record for an authorized human correction route, **not** a request for the user to retry and not a claim that the native fields are available.

- `HUMAN_NEEDS_FIX-EN08-001`: preserve the three existing downgraded strings as H2 at their current locations; do not change reader wording.
- `HUMAN_NEEDS_FIX-EN08-002`: place the three approved local image assets at their declared LEAD/MIDDLE/CLOSING anchors and preserve their captions; set each reviewed ALT only where an actual native ALT control is available.
- `HUMAN_NEEDS_FIX-EN08-003`: only if an author-controlled description/tag field is actually exposed, map the frozen raw SEO description and TAGS; otherwise leave this item `UNVERIFIED` rather than placing metadata in the body.

## Images: observed fact, user report, and root-cause boundary

These are deliberately separate:

1. **Observed public fact:** the source contains one responsive, empty-ALT cover before the article body, zero article-body images, no planned captions, and no temporary Chinese insertion cards. The cover's remote bytes, pixels, intrinsic ratio, content identity, and relation to local image 01 are `UNVERIFIED`; the HTML width/height attributes alone are not byte/pixel proof.
2. **User report:** [EN-08-user-publication-url-and-image-limitation.json](../../../evidence/EN-08-user-publication-url-and-image-limitation.json) records `USER_REPORTED_UPLOAD_LIMITATION` with the statement `编辑区或网络原因无法上传图片`, scoped only to this EN-08 publication attempt.
3. **Cause:** `UNDETERMINED_EDITOR_OR_NETWORK`. This review does not turn the user report into a PromoteProject-wide limitation, an image waiver, a proven cause, or an accepted-platform-limitation disposition. It does not ask the user to retry.

## Unverified surfaces and acceptance boundary

- No anonymous screenshot/browser viewport was available, so responsive selection, load success, visual readability, and rendered cover pixels are `UNVERIFIED`; the HTML source observations above remain independently captured.
- Native editor state; account state; upload history; ALT/caption/metadata/tag field availability; and human correction feasibility are all `UNVERIFIED` because this R-P did not access them.
- `HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. A returned URL, HTTP 200, source match on passing fields, or this R-P is not human acceptance or final public QA.
- The prior local `VISUAL-NARRATIVE-001` and `VISUAL-ASPECT-001` remain resolved only for local canonical/release assets. `PUBLIC-RENDER-002` is a new public-rendering finding and does not relabel their local resolution.

## Finding status and writer gate

| Finding ID | Status | First report | Disposition |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | OPEN | `public-review-1.md` | Public heading transport needs correction evidence. |
| `PUBLIC-RENDER-002` | OPEN | `public-review-1.md` | Public LEAD/MIDDLE/CLOSING image/caption parity is absent. |
| `PUBLIC-RENDER-003` | OPEN | `public-review-1.md` | Public metadata differs; author control is unverified. |

**Writer/public correction gate:** closed for public parity. If a corrective path changes any canonical reader wording, link, image asset, ALT, caption, or metadata value, it must return through the existing W → same R review path and produce a new release package before a subsequent R-P. If it is only a native rendering/manual-entry correction, retain the canonical package and re-run R-P against fresh public evidence. This is an R-P review only: no G decision, publication decision, human-acceptance decision, or campaign/root-state mutation is made here.
