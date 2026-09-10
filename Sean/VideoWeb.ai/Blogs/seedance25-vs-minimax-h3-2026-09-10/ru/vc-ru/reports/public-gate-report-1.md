verdict: PUBLIC_QA_CHANGES

# RU-01 G-P 1 — public-reader gate for vc.ru

article_id: `RU-01`  
campaign_id: `videoweb-seedance25-vs-minimax-h3-short-video-2026-09-10`  
platform/account: `{vc.ru, VIDEOWEB_OWNER_ACCOUNT_PRIORITY}`  
public_url: `https://vc.ru/id6106995/3131047-kak-sobrat-brif-dlya-produktovogo-rolika-seedance-2-5-i-minimax-h3`

## Decision and boundary

`PUBLIC_QA_CHANGES` is the only current G-P state. It consumes the independent R-P verdict `PUBLIC_REVIEW_CHANGES`; it does not redo language, fact, SEO, or image-quality review, and performs no browser, account, editor, upload, publication, deletion, or retry action.

`PUBLIC_QA_PASSED` is forbidden: `HUMAN_ACCEPTED` is absent. The publication receipt/state records `human_acceptance: NOT_YET_PROVIDED`, and neither the returned URL, HTTP 200, nor source-level reader match substitutes for an explicit human acceptance. In addition, the two open reader-visible rendering findings below must be resolved and independently rechecked.

No root campaign config, root `r3/state.json`, lane status, canonical article, local release package, or image was modified by this G-P. This report is the sole written output.

## Evidence accepted from R-P

R-P is reproducible anonymous reader evidence, not an editor read-back:

| Input | SHA-256 | What it establishes |
| --- | --- | --- |
| `r3/public-review-1.md` | `3c50f468601fdf010cd0e070d62cb8ffe3e5bdae800e761eb3a02cab4d1c6efc` | Independent `PUBLIC_REVIEW_CHANGES`, the two findings, and field-by-field comparison. |
| `evidence/public/anonymous-2026-09-10/capture-manifest.md` | `2db92be7beb9c8aa0a291d5d466fbb306417fb8eeebfeb3b8e6799b0c2b843eb` | One stateless anonymous GET; no login or editor interaction. |
| `evidence/public/anonymous-2026-09-10/headers.txt` | `fd43ce676ffdc7977b5aa1418c28ddc495f5839bea20261b10f03e7dea53f0be` | HTTP/2 200, `text/html; charset=utf-8`, length 179470, dated 2026-09-10 08:42:59 GMT. |
| `evidence/public/anonymous-2026-09-10/page.html` | `a57f533f89a9d5d9170f36dd6f178e1cb2155f5876bd1f4a3043b5ccde385808` | Full SSR reader article rather than an empty client shell. |
| `evidence/public/anonymous-2026-09-10/transfer.txt` | `e9761b71d449fbb0bbd65db52cb432262d34aefd9b6891c63272e961bbadf115` | Capture URL, HTTP 200, content type/length, and `curl_exit=0`. |

R-P records a source-level match for the public title/H1 and H2/H3 order, complete reader body other than the findings, the founder disclosure, both exact VideoWeb destinations with their Russian anchors (vc.ru redirect wrappers decode to the frozen destinations), and all three images in LEAD/MIDDLE/CLOSING order with the manifest ALT values. The governed local reference remains `human-release/RU-01/vc.ru/fingerprint.json` (`05aaaba1220ab73b57c67488499188c583fcaf7badbfb7c9831a7a32f7fff3b8`): canonical Markdown `9e6e6030cb9db3e47f7be600b7f6dd96d83dab6f256c4a08f42c8ffddf54d321`, canonical HTML `6d0012dabf1ef73a9ecbeb8c29d22c1083da150ca12d705ea7923dfbeff4823f`, and visual payload `1d32ac596f7a480be48171e10d3aae69ddb5d8fb699e45226c45587ce70c0a2d`.

## Open public findings and minimal human action

| ID | Status | Reader-visible evidence | Required human-only remediation |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | OPEN | Each of the two canonical six-field untested prompt templates lost its blockquote and line structure on the reader page; the fields appear as run-on paragraphs. R-P records zero public template blockquotes and no template line breaks, while the canonical HTML/payload has two quote blocks with six separately lined fields each. | In vc.ru, restore each template as six visibly separate lines in a quote/indented block, or a native equivalent, without changing its text, links, disclosure, images, or factual boundaries. |
| `PUBLIC-RENDER-002` | OPEN | Each planned public image adds an unplanned visible title that duplicates its ALT before the intended adjacent Russian editorial-illustration disclosure. R-P separately verifies that the image order and actual ALT values match the manifest. | In the native image controls, remove the three visible ALT-duplicate titles/captions while preserving every image ALT and its immediately following Russian disclosure. If vc.ru cannot separate the visible title/caption from ALT, return that observed limitation; do not guess or alter the ALT to compensate. |

The G-P does not infer whether vc.ru's native editor can make either correction. The human must report the observed outcome, complete a fresh reader-page check, and return the explicit `HUMAN_ACCEPTED` only if the repaired page is accepted; otherwise return `HUMAN_NEEDS_FIX`. A new anonymous capture then requires the same article R-P and a fresh G-P before any final public result.

## Still unverified; not silently promoted

- Screenshot/raster evidence, public image pixels, CSS paint, viewport behavior, and screen-reader exposure remain `UNVERIFIED`.
- Native vc.ru TAGS/SEO-description/image-control persistence and semantics remain `UNVERIFIED`; the observed public description/empty keywords are platform-controlled observations, not an additional frozen-contract finding.
- Robot/indexing semantics remain `UNVERIFIED`. The captured `x-robots-tag: noindex` is retained as a response observation, not proof of intended or persistent robot policy.
- Human acceptance remains absent and is a separate hard precondition for `PUBLIC_QA_PASSED`.

## Continuity

The local `DELIVERY-ALT-CONTRACT-001` is resolved by R-Δ (`r3/review-report-2.md`); it is unrelated to these reader-page defects. Open public findings for this G-P are exactly `PUBLIC-RENDER-001` and `PUBLIC-RENDER-002`. No rollback recommendation is supported by the current evidence: both discrepancies have scoped human remediation, while native fixability is deliberately left unasserted.
