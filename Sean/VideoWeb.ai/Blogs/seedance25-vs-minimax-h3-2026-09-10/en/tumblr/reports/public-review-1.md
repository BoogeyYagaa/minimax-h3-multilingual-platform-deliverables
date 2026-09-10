verdict: PUBLIC_REVIEW_CHANGES
role: ARTICLE_LANGUAGE_REVIEWER
article_id: EN-04
review_scope: public read-only R-P
public_url: https://www.tumblr.com/videowebai/827355403965890560/a-travel-photo-to-video-prompt-plan-three-motion?source=share
public_evidence: evidence/public-reader-observation-1.md
reviewed_at: 2026-09-10
human_accepted: NOT_YET_PROVIDED

## Decision

The exact user-supplied public Tumblr reader URL is reachable and contains the actual EN-04 post, not merely an HTTP shell. Public reader text, paragraph/list order, title, disclosure, supplied VideoWeb anchors/hrefs, three images, ALT, captions, and placeholder removal all match the canonical comparison surfaces. However, Tumblr rendered the three canonical H3 motion directions as H2 elements. This changes the required public heading hierarchy, so the technical public review is `PUBLIC_REVIEW_CHANGES`.

This report is a read-only R-P. It does not modify local state, infer account control, authorize an external edit, or confer `HUMAN_ACCEPTED`, public-QA pass, G-P approval, or any release status. The local files still record `NOT_PUBLISHED` / `NOT_STARTED`; those stale local declarations were not overwritten from a URL alone.

## Canonical fingerprint and public evidence

| Input | SHA-256 |
| --- | --- |
| `article.md` | `f964429defc48401a2a7ef37cefcd35570169ed6ffd1524ab8d892ded505a732` |
| `article.html` | `86af2774ea15cb6fc20641dd02e6ebac8e54eb694cfc32b8c9a1a86cd64db083` |
| `human-release/Tumblr/content.md` | `d3f7b26caf0b312204ded94695aa00142a26e5535176fc21614242e229377ac2` |
| `human-release/Tumblr/visual-payload.html` | `514350c322f8cb461763723ced753e871dbd8a3063e540dc27df9de129b14454` |
| Public HTML response at collection | `6c1c546336be951f2bdfea9fe0e2758d148fa835dd18a8f837bf7606478e91d1` |

The response was an actual `HTTP/2 200` reader document collected anonymously at `Thu, 10 Sep 2026 08:15:55 GMT`; it had a real post container and 8,563-byte normalized reader text equal to canonical HTML. Full non-sensitive observation and comparison details are in `evidence/public-reader-observation-1.md`.

## Public reader comparison

| Surface | Result |
| --- | --- |
| Title / H1 | PASS — canonical title appears as one public H1; page title identifies `@videowebai`. |
| Body paragraphs and four-item list | PASS — normalized public reader text and order exactly match canonical. |
| H2 / H3 hierarchy | CHANGES — six canonical H2 remain H2, but all three canonical H3 motion directions are public H2; public H3 count is zero. |
| Founder disclosure | PASS — exact disclosure occurs once near the opening. |
| Two provider links | PASS — each exact URL and visible anchor occurs once in the provider-attributed paragraph. |
| Images, ALT, captions, placement | PASS — three public images have exact manifest ALT, expected LEAD/MIDDLE/CLOSING positions, and one matching English caption each. |
| Placeholder removal | PASS — no Chinese placeholder label, filename marker, or yellow-placeholder instruction survives in public reader text. |
| Observable metadata | PASS / observed — description begins with canonical opening; `og:title` reports three images; `og:type` is `article`; canonical `og:url` differs only by removal of the sharing query. |
| User acceptance | UNVERIFIED — `HUMAN_ACCEPTED` is not provided. |

## Open public finding

### PUBLIC-HEADING-HIERARCHY-001 — OPEN — P1

- **Expected:** Canonical structure is one H1, six H2, and three H3; the three numbered motion directions are H3 beneath “Three controlled motion directions for a travel image.”
- **Observed:** The public post has one H1, nine H2, and zero H3. The three numbered motion-direction labels retain their wording and order but are rendered as H2.
- **Effect:** Reader prose is intact, but the public semantic hierarchy is not canonical parity.
- **Required next action:** A human-authorized Tumblr correction must restore those three labels to the intended subordinate heading level, then a fresh read-only R-P must verify the public result. This review neither edits nor authorizes editing the live post.

## UNVERIFIED boundaries

- `HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`.
- The public account label observed in URL/metadata is not proof of owner-account authorization or login state.
- No public G-P review has occurred.

## External read-only actions

- Read the user-supplied URL through an anonymous public reader request only. The returned document was inspected for actual post content; no HTTP-200 shell was accepted as proof.
- A local anonymous in-app browser surface was unavailable; that was recorded only as a tooling limitation and was not treated as a site failure.
- No browser login, CDP session, account operation, editor access, upload, visibility change, post edit, repost, deletion, interaction with MusicMaker, or root-state write occurred.
