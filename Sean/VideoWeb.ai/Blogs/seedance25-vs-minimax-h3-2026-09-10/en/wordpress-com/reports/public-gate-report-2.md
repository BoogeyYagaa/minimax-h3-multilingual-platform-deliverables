verdict: PUBLIC_QA_CHANGES

# EN-01 WordPress.com public gate 2 — evidence-correction closeout

article: EN-01  
gate: ARTICLE_PUBLIC_GATE (fresh, independent, on-disk evidence only)  
scope: current public-reader semantic evidence and the inherited public finding; no browser, editor, account, upload, save, publication, repost, deletion, or other external action  
public_url: https://videowebai.wordpress.com/2026/09/10/seedance-2-5-vs-minimax-h3-for-product-videos-a-same-brief-decision-protocol/  
current_anonymous_evidence: `evidence/public-reader-002.json` SHA-256 `e065eae8bc1a33a66336f2e48a30944dad90b88715dd2e84a3a7e5763d4787f6`  
current_evidence_captured_at_utc: `2026-09-10T10:05:47.000Z`  
human_acceptance: NOT_YET_PROVIDED

## Decision

The verdict remains `PUBLIC_QA_CHANGES`. The fresh anonymous no-cookie GET reached the exact reader URL with `200 OK`, no redirect, and the same complete HTML SHA-256 as the earlier capture, but it confirms that the article title is semantically an `h2`, not the required article `h1`.

The frozen `SEPARATE_TITLE_FIELD` package requires a title-panel semantic level of 1 and zero H1 elements in the copied body. It does not permit the site-shell H1 to substitute for the article title. Therefore `PUBLIC-RENDER-001` remains **OPEN**. Neither the public URL nor HTTP success establishes `HUMAN_ACCEPTED`, and the missing explicit human acceptance independently prevents `PUBLIC_QA_PASSED`.

## Exact current semantic map

| Surface | Exact selector and tag | Location / classification | Gate result |
| --- | --- | --- | --- |
| Site title | `header h1.wp-block-site-title` → `<h1 class="wp-block-site-title">videowebai</h1>` | Header/site shell, before `main`; home link next to navigation | Site H1 only; not the article title. |
| Article title | `main h2.wp-block-post-title` → `<h2 class="has-text-align-center wp-block-post-title has-large-font-size">…</h2>` | Inside `main`, immediately before `.entry-content` | Actual article title, but semantic H2: `PUBLIC-RENDER-001` OPEN. |
| Article entry | `main .entry-content.wp-block-post-content` | Follows the post title; contains the disclosure, required links, frozen H2/H3 sequence, and figures; H1 count is zero | Consistent with the required zero-body-H1 rule, but does not supply the required article H1. |

`has-large-font-size` and `has-text-align-center` are presentation/CSS classes. They do not convert the actual HTML `h2` to a semantic H1. This evidence establishes no page, region, selector, site-shell/article, or visual-style confusion.

## Old evidence correction disposition

`PUBLIC-RENDER-001` is **RETAINED — OPEN**, not superseded or replaced.

- `public-reader-001.json` records an asserted capture time of `2026-09-10T07:34:48Z` and is a structural digest, rather than retained raw HTML. Its time/provenance is therefore retained as asserted historical context, not raw-source replay proof.
- The old and current complete-document digest is the same: `14694429ae33179d08a8ea78a1277f9800da2ec1111f8f3fb5503e95705f695e` (140686 bytes).
- The new evidence adds the raw selectors, tags, source contexts, and a fresh retrieval time. It independently confirms the old observation: the site name is the header H1 and the post-title element is the H2 inside `main`.

Accordingly, the strengthened evidence retention/time context is not a correction of the semantic finding. No cause for the WordPress template tag choice, and no author-controllable setting, is asserted.

## Acceptance and human-only boundary

The user-returned URL receipt records `human_acceptance: NOT_YET_PROVIDED`. It remains distinct from publication evidence, HTTP access, public-source parity, R-P, and this G-P outcome.

The controller's remediation hold remains respected. This report issues no editor action or repair card. The sole evidence-grounded human-only condition is: if the responsible human later elects to repair the existing reader rendering, the **existing article title** must render as semantic H1 while the article body remains at zero H1, without changing canonical reader copy, title text, links, disclosure, images, ALT, captions, metadata values, author identity, or URL for this finding. Any such human decision requires fresh anonymous reader evidence, an R-P recheck, and a fresh G-P; `HUMAN_ACCEPTED` remains separately required for any eventual `PUBLIC_QA_PASSED`.

## Other observed public fields and evidence limits

The current evidence supports the same previously recorded public fields: exact post-title text, all 13 frozen H2/H3 labels in source order, opening founder disclosure, two required links once each with their descriptive anchors, and three images in the declared order with matching ALT/captions. It does not newly establish complete paragraph/list/blockquote parity, remote image bytes or final pixels, content-column width, native tags/excerpt/comments, a rendering cause, author control, or human acceptance. These remain evidence limits, not new content findings.

## Finding status

| ID | Status | Current evidence | Disposition |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | OPEN / retained | `evidence/public-reader-002.json#semantic_mapping`; `r3/public-review-2.md` | Article title is `main h2.wp-block-post-title`; the site-shell title is `header h1.wp-block-site-title`. |

No local pre-public finding is reopened, no new finding ID is created, and no campaign/root state is changed by this article-local report.

## Inputs consumed

- `human-release/wordpress-com/fingerprint.json` — SHA-256 `129f2c67afdd240d203f8abf068a4ce217c57336bc9437365af3fa0a6b793f64`
- `human-release/wordpress-com/visual-payload.html` — SHA-256 `85f5b487d3bd64d559cec5f849071f2b0bf8fa656bc88f6d85ae078e060cba75`
- `r3/public-review-1.md` — SHA-256 `d53a5eb1bac028550259ffa7e1d286e233be5a96c79ae6a4f17df79f07457c4c`
- `r3/public-gate-report-1.md` — SHA-256 `fcce097bbe12f7364b865f5bff25854ca67c56fe4581d45e6f33257f344eaa24`
- `r3/public-review-2.md` — SHA-256 `e60c3ce7761e941fa9b674449f6c02bf1125005c7cdce4e6b0375956881e7e75`
- `evidence/public-reader-001.json` — SHA-256 `64b85f318db1ec12cf376412e053ed3f6a97716f09a888a124b5c12e242b345e`
- `evidence/public-reader-002.json` — SHA-256 `e065eae8bc1a33a66336f2e48a30944dad90b88715dd2e84a3a7e5763d4787f6`
