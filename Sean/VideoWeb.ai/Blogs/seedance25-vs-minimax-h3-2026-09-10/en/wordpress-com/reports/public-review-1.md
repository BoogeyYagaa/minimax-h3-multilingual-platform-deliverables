verdict: PUBLIC_REVIEW_CHANGES

# EN-01 Public R-P 1 — WordPress.com reader page

article: EN-01  
review_scope: public_readonly  
public_url: https://videowebai.wordpress.com/2026/09/10/seedance-2-5-vs-minimax-h3-for-product-videos-a-same-brief-decision-protocol/  
canonical_payload_fingerprint: `human-release/wordpress-com/fingerprint.json` SHA-256 `129f2c67afdd240d203f8abf068a4ce217c57336bc9437365af3fa0a6b793f64`  
canonical_markdown: `canonical/article.md` SHA-256 `a10fb344f17f701f22eb5116068c6005a921a060d08df46f70e65f08956ffb99`  
public_reader_evidence: `evidence/public-reader-001.json` SHA-256 `64b85f318db1ec12cf376412e053ed3f6a97716f09a888a124b5c12e242b345e`

## Verdict

The anonymous public reader source is reachable at the supplied URL (HTTP 200) and preserves the post title text, the full canonical H2/H3 label sequence, the two required links, founder disclosure, three ordered image records, captions, and observed description metadata. It does not preserve the required post-title H1 semantics: the public document assigns H1 to the site name `videowebai` and renders the post title as H2. This is a reproducible public-reader mismatch, so the R-P verdict is `PUBLIC_REVIEW_CHANGES`.

This is an R-P result only. It is not a G-P decision, human acceptance, or `PUBLIC_QA_PASSED` claim.

## Evidence and external actions

- Read all EN-01 R1/R2, resolution, local G, release-package, canonical, fingerprint, transport, local SEO, image-manifest, checklist, and user-returned-URL records before public comparison.
- A cookie-free anonymous HTTP GET of the exact public URL returned `200`, no redirect, `text/html; charset=UTF-8`, HTML SHA-256 `14694429ae33179d08a8ea78a1277f9800da2ec1111f8f3fb5503e95705f695e`, and 140686 bytes. The deidentified extraction is the evidence file above.
- Profile 11 was read only through its documented CDP endpoint: one version check, one new tab directly to the public URL, and one runtime read. It exposed an authenticated administrative bar, so it is excluded from anonymous-reader comparison. No editor URL, login, account setting, upload, save, submission, edit, deletion, or repost action was performed; MusicMaker was not accessed.
- No further public-page, feed, image-byte, or screenshot request was made after the close instruction.

## Field-by-field public comparison

| Field | Canonical / package expectation | Anonymous public evidence | Result |
| --- | --- | --- | --- |
| HTTP reader access | Public reader page at supplied URL | HTTP 200, no redirect, same final URL | PASS |
| Document title | Post title text plus platform suffix allowed | `Seedance 2.5 vs MiniMax H3 for Product Videos: A Same-Brief Decision Protocol – videowebai` | PASS |
| Post title / H1 transport | Separate title field produces the sole post semantic H1; public body begins at H2 | Site name is document H1; the exact post title is `<h2 class="wp-block-post-title">` | FINDING `PUBLIC-RENDER-001` |
| H2/H3 reader structure | 13-item payload-body sequence in fingerprint | All 13 expected H2/H3 labels occur in the same source order, including two planning rewrites, three FAQ H3s, and conclusion | PASS |
| Full paragraphs, lists, blockquote order | Complete canonical reader body in source order | Opening disclosure, all body headings, links, image records/captions, and closing image before sharing controls were extracted. A durable full raw-body artifact was not retained before close. | UNVERIFIED |
| Founder disclosure | Near opening: `I am the founder of VideoWeb AI.` | Visible in first reader-content block | PASS |
| Required links | Each exact VideoWeb URL once with descriptive anchor | Both exact hrefs and expected anchors extracted from anonymous source | PASS |
| Image order / ALT / captions | Three declared lead/middle/closing files with mapped ALT and caption | Three WordPress source images occur in 01/02/03 order; each returned ALT and figcaption exactly matches the manifest. Public renditions are 1024×576 (16:9). | PASS for source attributes/order |
| Remote image bytes, final pixels, rendered column width | Source/release byte parity and visually reviewed placement | No separate remote-byte fetch or screenshot evidence after close | UNVERIFIED |
| SEO / social metadata | Fingerprinted SEO description | `description` and `og:description` exactly match the package SEO description; `og:title` matches canonical title | PASS |
| Native tags, excerpt display, canonical tag, comments | Platform-dependent fields | Not extracted in retained evidence | UNVERIFIED |

## Public finding

### PUBLIC-RENDER-001 — OPEN

- Severity: High
- Rule: public title/H1 transport / `fingerprint.json.heading_transport` / `REQ-PAYLOAD-001`
- Evidence: `evidence/public-reader-001.json#semantic_title_observation` records the canonical title text under an H2 post-title element while the theme's H1 is the site label `videowebai`. The canonical fingerprint requires the title field to carry semantic level 1 and the body to have no H1.
- Reader impact: the reader-facing post has no semantic H1 for the article, while an unrelated site title occupies the page H1.
- Minimal human fix: in the WordPress.com theme/template or post-title block configuration, restore the post title element to H1 without adding a body H1 or changing canonical reader copy. Then supply a fresh public reader URL/source capture for a new R-P. This is a platform-rendering repair, not authorization to alter the canonical article.

## UNVERIFIED surfaces

- Complete paragraph/list/blockquote byte- or text-level order, because the anonymous source capture was retained as a deidentified structural digest rather than the entire source body before close.
- Public original-image bytes, displayed pixels, content-column width, and visual placement beyond source order/ALT/caption.
- Public tag visibility, excerpt rendering, canonical-link tag, comments state, human acceptance, and any G-P outcome.

## Finding status

| ID | Status | First public report |
| --- | --- | --- |
| PUBLIC-RENDER-001 | OPEN | public-review-1.md |

No legacy pre-public finding is reopened. The three R1 local findings remain resolved in `full-review-2.md`.
