verdict: PUBLIC_QA_CHANGES

# EN-01 WordPress.com public gate 1

article: EN-01  
gate: ARTICLE_PUBLIC_GATE (fresh, on-disk evidence only)  
scope: public-reader evidence assessment; no browser, login, CDP, editor, or external action  
public_url: https://videowebai.wordpress.com/2026/09/10/seedance-2-5-vs-minimax-h3-for-product-videos-a-same-brief-decision-protocol/  
publication_status_observed: USER_REPORTED_PUBLISHED_PENDING_PUBLIC_QA  
human_acceptance: NOT_YET_PROVIDED

## Decision

`PUBLIC_QA_CHANGES` is required because the anonymous public reader evidence reproducibly renders the article title as an `h2` while the unrelated site label `videowebai` is the document `h1`. This conflicts with the frozen `SEPARATE_TITLE_FIELD` contract: the post title must be the sole semantic H1 and the payload body must contain no H1.

This is a reader-visible transport mismatch, not a conclusion about why WordPress.com produced it. The evidence does not establish whether the responsible control is a theme/template, post-title block configuration, or another platform-controlled rendering rule.

The public URL itself is meaningful technical evidence: its cookie-free request returned HTTP 200 with no redirect and a 140686-byte HTML response. It is not rejected because a prior controller tool had a safe-to-open error; that tool error retrieved no page content and is not access evidence.

This gate does not treat the returned URL as `HUMAN_ACCEPTED`, does not classify the post as deleted or unpublished, and does not issue `PUBLIC_QA_PASSED` or permit harvest.

## Inputs independently read

| Input | SHA-256 | Use in this gate |
| --- | --- | --- |
| `canonical/article.md` | `a10fb344f17f701f22eb5116068c6005a921a060d08df46f70e65f08956ffb99` | Canonical title, two links, disclosure, reader copy, and intended three-image sequence. |
| `human-release/wordpress-com/fingerprint.json` | `129f2c67afdd240d203f8abf068a4ce217c57336bc9437365af3fa0a6b793f64` | Frozen title/H1 transport, heading map, link values, and image metadata. |
| `human-release/wordpress-com/visual-payload.html` | `85f5b487d3bd64d559cec5f849071f2b0bf8fa656bc88f6d85ae078e060cba75` | Separate semantic-H1 title panel; zero-H1 body; payload links and image-card positions. |
| `human-release/wordpress-com/transport-check.md` | `dd87eba0fcbf51826950e6edf90d755f9a6c1f2dce25f23cd97d206149bf2843` | Local declaration of `SEPARATE_TITLE_FIELD`, zero body H1, and ordered H2/H3 transport. |
| `human-release/wordpress-com/local-seo-issues-reference.md` | `5f3998163832af2a756a027a3d77a10862469c74d82b9d24c4e50224935da29e` | Local controllable-field expectations only; not public proof. |
| `human-release/wordpress-com/image-manifest.md` | `18911af117d8d2ed07fb65b793d8e3c3ace7a31efea9c6a7bba4779d37989fd8` | Required 01/02/03 order, ALT, captions, and LEAD/MIDDLE/CLOSING positions. |
| `r3/gate-report-1.md` | `38a9fbce5155e2e4d0f168c9ecb68f82915d62dd5adfcac8326b7ee3fc05aad5` | Local G is `HUMAN_RELEASE_READY` only; it is not public QA. |
| `evidence/EN-01-user-publication-url.json` | `ce7950cae16403539eb249c4086eeed41c233a57a424da61dbcdd973c0c57727` | User-returned URL; `HUMAN_ACCEPTED` remains absent. |
| `evidence/public-reader-001.json` | `64b85f318db1ec12cf376412e053ed3f6a97716f09a888a124b5c12e242b345e` | Anonymous HTTP response and extracted public reader fields. |
| `r3/public-review-1.md` | `d53a5eb1bac028550259ffa7e1d286e233be5a96c79ae6a4f17df79f07457c4c` | Reusable EN-01 R-P comparison and inherited public finding. |

Also read: campaign configuration, confirmation, requirements contract, current campaign state for scope only, EN-01 research review, Full R1/R2, W resolution, assignment/traceability, release card, and all listed local package materials. No root-state mutation is made by this fresh G-P.

## Public-reader evidence assessment

| Surface | Frozen expectation | Anonymous reader evidence | Gate result |
| --- | --- | --- | --- |
| Accessibility | Supplied public reader URL | HTTP 200; no redirect; same final URL; `text/html; charset=UTF-8` | Verified reader access at capture time. |
| Title text | `Seedance 2.5 vs MiniMax H3 for Product Videos: A Same-Brief Decision Protocol` | Exact title text appears in document title and post-title record | PASS for text. |
| Post-title semantic level | Title field carries sole semantic H1; body begins at H2 | `site_h1: videowebai`; `post_title_tag: h2`; expected post title tag `h1` | `PUBLIC-RENDER-001` OPEN. |
| H2/H3 sequence | 13 payload-body headings in fingerprint order | All 13 expected H2/H3 labels recorded in source order | PASS for recorded heading sequence. |
| Required VideoWeb links | Two exact hrefs, once each, with descriptive anchors | Both expected anchor/href records present | PASS for extracted records. |
| Founder disclosure | Near opening | `Disclosure: I am the founder of VideoWeb AI.` extracted from reader source | PASS. |
| Images | Three ordered figures with frozen ALT and captions | 01/02/03 source records, each with matching ALT/caption and 1024x576 rendition | PASS for source order/attributes only. |
| Description metadata | Frozen SEO description | `description` and `og:description` match; `og:title` matches canonical title | PASS for extracted metadata. |

The R-P correctly distinguishes the verified source-extracted fields from unretained or unobserved fields. It does not use the authenticated Profile 11 administrative-bar view as anonymous public proof.

## Public finding status

| ID | Status | Evidence | Disposition |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | OPEN | `evidence/public-reader-001.json#semantic_title_observation`; `r3/public-review-1.md` | The public post title is an H2 while the site name is H1. This reproducible mismatch requires a human repair/recheck. |

No local R finding is reopened. The prior local findings `SEO-SUPPORT-TERM-001`, `PAYLOAD-FINGERPRINT-001`, and `VISUAL-EVIDENCE-MANIFEST-001` remain resolved by Full R2; this gate adds no new local-content finding.

## UNVERIFIED surfaces

- Full public paragraph, list, and blockquote text/order: the retained anonymous evidence is a structural digest rather than a durable full raw-body comparison artifact.
- Public original-image bytes, final pixels, content-column width, and visual placement beyond source order, ALT, caption, and rendition dimensions.
- Native tag visibility, excerpt rendering, canonical-link tag, and comments state.
- The exact WordPress.com rendering mechanism and whether an author-controllable title/template setting exists.
- `HUMAN_ACCEPTED` or `HUMAN_NEEDS_FIX` from the publisher.

These are not silently converted into missing-content findings. They remain evidence limits.

## Smallest human-only repair card

`HUMAN_NEEDS_FIX — PUBLIC-RENDER-001`

1. On the existing WordPress.com post/site rendering configuration, restore the **post title itself** to semantic H1 output.
2. Do not add a second H1 to the post body, and do not change the canonical article text, links, disclosure, images, ALT, captions, title text, metadata values, author identity, or URL merely to address this transport finding.
3. Return the unchanged-or-repaired public reader URL and a new anonymous-accessible reader-page capture. The next capture must preserve sufficient full-reader evidence to compare the repaired title/H1 and all formerly unverified body/visual surfaces that it claims to verify.
4. If the current WordPress.com configuration cannot author-control this semantic level, report that observed limitation explicitly. Do not call the current H2 output exact payload parity or imply a confirmed theme-specific cause.

The original EN-01 R can perform the next technical R-P as soon as fresh anonymous evidence exists; that read-only recheck does **not** wait for `HUMAN_ACCEPTED`. A fresh G-P is required after that R-P. `HUMAN_ACCEPTED` remains separately necessary for any eventual `PUBLIC_QA_PASSED` completion.

## Prohibitions and handoff boundary

- No duplicate publication, repost, deletion, rollback, editor entry, metadata change, image upload, share action, author-identity change, or automated repair by this G-P or any machine.
- Do not change canonical EN-01 reader content for this public-rendering issue unless a later human reports a substantive content mismatch and the normal W → R → G cycle is re-entered.
- Do not count this post toward public-QA-passed quota and do not harvest a WordPress.com platform skill from this result.

Required campaign-controller state suggestion only: retain `publication_status=USER_REPORTED_PUBLISHED_PENDING_PUBLIC_QA`; set the EN-01 public gate outcome to `PUBLIC_QA_CHANGES`; preserve `human_acceptance=NOT_YET_PROVIDED`; retain `PUBLIC-RENDER-001` as OPEN; record this report and its evidence hashes. The campaign controller alone owns that state update.
