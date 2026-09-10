verdict: PUBLIC_REVIEW_CHANGES

# EN-01 public R-P 2 — evidence-correction review

article: EN-01  
review_scope: public_readonly evidence correction  
public_url: https://videowebai.wordpress.com/2026/09/10/seedance-2-5-vs-minimax-h3-for-product-videos-a-same-brief-decision-protocol/  
canonical_payload_fingerprint: `human-release/wordpress-com/fingerprint.json` SHA-256 `129f2c67afdd240d203f8abf068a4ce217c57336bc9437365af3fa0a6b793f64`  
canonical_markdown: `canonical/article.md` SHA-256 `a10fb344f17f701f22eb5116068c6005a921a060d08df46f70e65f08956ffb99`  
new_public_reader_evidence: `evidence/public-reader-002.json` SHA-256 `e065eae8bc1a33a66336f2e48a30944dad90b88715dd2e84a3a7e5763d4787f6`  
prior_public_reader_evidence: `evidence/public-reader-001.json` SHA-256 `64b85f318db1ec12cf376412e053ed3f6a97716f09a888a124b5c12e242b345e`

## Scope, source material, and external action

I re-read the frozen EN-01 canonical article and WordPress.com release package (including fingerprint, visual payload, transport check, local SEO reference, image manifest, metadata/raw controls, release card, and checklist), the campaign/confirmation/contract/state entries for EN-01, shared long-tail and product-fact boundaries, all EN-01 R/W/finding/G/public reports, the user-returned URL receipt, and `public-reader-001.json`.

One new anonymous action was taken: at `2026-09-10T10:05:47.000Z`, a new process made one cookie-free HTTP GET to the exact supplied reader URL. It returned `200 OK`, no redirect, `text/html; charset=UTF-8`, 140686 bytes, and SHA-256 `14694429ae33179d08a8ea78a1277f9800da2ec1111f8f3fb5503e95705f695e`. No profile/CDP/browser, login, account, editor, media request, upload, save, publish, delete, repost, MusicMaker, or other external write was used.

`HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. This R-P is neither human acceptance nor a G-P/public-QA decision.

## Current semantic mapping: site shell versus article

| Surface | Current raw selector and tag | Evidence that it belongs there | Conclusion |
| --- | --- | --- | --- |
| Site name | `header h1.wp-block-site-title` → `<h1 class="wp-block-site-title">videowebai</h1>` | It is inside `<header class="wp-block-template-part">`, before `<main>`, and is an `rel="home"` link adjacent to the site navigation. | This is site-shell H1, not the article title. |
| Article title | `main h2.wp-block-post-title` → `<h2 class="has-text-align-center wp-block-post-title has-large-font-size">…</h2>` | It is inside `<main id="wp--skip-link--target" ...>`, immediately before the post-content block. | This is the actual article-title element, and its semantic tag is H2. |
| Article reader content | `main .entry-content.wp-block-post-content` → `<div class="entry-content wp-block-post-content ...">` | It follows the post title in `main`; it begins with the article’s long-tail boundary and founder disclosure; it contains the two frozen anchors, 13 frozen H2/H3 labels, and the three figures. Its H1 count is zero. | This is the article-content container. |

`has-large-font-size` and `has-text-align-center` on the post-title element are presentation classes. They do not make an HTML `h2` a semantic `h1`. The local `SEPARATE_TITLE_FIELD` fingerprint instead requires the post title to carry semantic level 1 and the body to contain zero H1s.

## Field-by-field reader comparison

| Field | Frozen expectation | Current anonymous evidence | Result |
| --- | --- | --- | --- |
| Reader access / URL | Exact supplied public reader URL | HTTP 200; same final URL; no redirect | PASS |
| Document/post title text | `Seedance 2.5 vs MiniMax H3 for Product Videos: A Same-Brief Decision Protocol` | Exact post title under `main h2.wp-block-post-title`; document title adds `– videowebai` | PASS for text |
| Article-title semantic level | Separate title field produces sole article semantic H1 | Site label is `header h1.wp-block-site-title`; actual post title is `main h2.wp-block-post-title`; article entry has zero H1 | FINDING `PUBLIC-RENDER-001` |
| Frozen article heading order | 13 H2/H3 labels after the title | All 13 occur in the required source order under `.entry-content`; the later `<h3 class="sd-title">Share this:</h3>` is a platform share widget, not a frozen article heading | PASS |
| Founder disclosure | Near opening | `Disclosure: I am the founder of VideoWeb AI.` occurs in the entry opening | PASS |
| Required target links | Each exact VideoWeb href once with a descriptive anchor | Each exact href occurs once in the entry; anchors are `Seedance 2.5 short-video workflow page` and `MiniMax H3 short-video workflow page` | PASS |
| Three image records | Ordered lead/middle/closing figures with expected ALT/caption | `01` / `02` / `03` WordPress image files occur in that order; each reports original `1664,936`, rendered `1024×576`, and exact local-manifest ALT/caption text | PASS for source attributes/order |
| Metadata | Frozen title/description where observable | The full current HTML SHA-256 is identical to the old capture whose recorded document title, `og:title`, `description`, and `og:description` matched the package; no separate metadata interpretation is needed to establish the unchanged source. | PASS for the previously extracted source fields |
| Complete text/list/blockquote byte-level comparison | Full canonical reader-copy parity | The new artifact deliberately preserves semantic mapping and field records, not a second full raw-body artifact. | UNVERIFIED |
| Remote image bytes, displayed pixels, and column width | Public image/render verification | No remote media fetch or screenshot was performed. | UNVERIFIED |
| Excerpt/tag rendering, comments, acceptance | Platform/native human surfaces | Not established by the anonymous source read or user receipt. | UNVERIFIED |

## Provider and fact boundary recheck

The captured entry opening retains the editorial-long-tail limitation and founder disclosure. The verified article heading/link/image/caption records contain no new comparison score, benchmark, output test, performance/quality/speed/reliability result, official-vendor provenance, price, free-entitlement, availability, or winner claim. A complete fresh body-token comparison remains `UNVERIFIED`, rather than being inferred from the local package.

## Disposition of the disputed old evidence and finding

`PUBLIC-RENDER-001` is **RETAINED — OPEN**. It is not superseded and no new finding ID is created.

- `public-reader-001.json` asserted capture time `2026-09-10T07:34:48Z`; the user URL receipt records `2026-09-10T07:34:48.349840+00:00`. The old record is a structural digest rather than retained raw HTML, so that asserted time/provenance does not itself provide raw-source replay evidence.
- Its HTML digest, `14694429…05f695e`, exactly equals the newly captured complete document digest. The current raw selectors independently reproduce its stated observation: the site name is the header H1, while the actual post-title element is H2 inside main.
- Therefore the old `PUBLIC-RENDER-001` observation was not factually wrong and did not select the wrong page, shell element as the post title, or a visually large element as a semantic H1. `public-reader-002.json` supplies the previously missing exact selectors, raw tags, concise contexts, and a fresh retrieval timestamp. No explanation for the template's tag choice is asserted.

No human repair is requested by this report. The controller’s existing hold on remediation is respected. The open public finding alone requires `PUBLIC_REVIEW_CHANGES`; an approval would be incompatible with the frozen semantic-H1 transport requirement.

## Finding status

| ID | Status | Origin | Current evidence |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | OPEN / retained | `r3/public-review-1.md` | `evidence/public-reader-002.json#semantic_mapping` |

No local pre-public finding is reopened. The resolved `SEO-SUPPORT-TERM-001`, `PAYLOAD-FINGERPRINT-001`, and `VISUAL-EVIDENCE-MANIFEST-001` statuses from Full R2 remain unchanged.
