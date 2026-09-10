verdict: PUBLIC_REVIEW_CHANGES

# RU-01 independent public-reader review 1 — VideoWeb campaign

## Scope and status boundary

This is a fresh anonymous, read-only R-P of the public vc.ru reader page, compared with the current local canonical/release package. It is not a G-P decision, not publication completion, and not a platform action.

`HUMAN_ACCEPTED` is **UNVERIFIED**: `evidence/RU-01-user-publication-url.json` records `human_acceptance: NOT_YET_PROVIDED`. The returned URL and this HTTP capture do not substitute for human acceptance or final public completion.

canonical_payload_fingerprint: `human-release/RU-01/vc.ru/fingerprint.json`; canonical Markdown SHA-256 `9e6e6030cb9db3e47f7be600b7f6dd96d83dab6f256c4a08f42c8ffddf54d321`; canonical HTML SHA-256 `6d0012dabf1ef73a9ecbeb8c29d22c1083da150ca12d705ea7923dfbeff4823f`; local visual-payload SHA-256 `1d32ac596f7a480be48171e10d3aae69ddb5d8fb699e45226c45587ce70c0a2d`.

public_url: `https://vc.ru/id6106995/3131047-kak-sobrat-brif-dlya-produktovogo-rolika-seedance-2-5-i-minimax-h3`

## Anonymous evidence

- Capture manifest: `articles/RU-01/evidence/public/anonymous-2026-09-10/capture-manifest.md`.
- Raw headers: `articles/RU-01/evidence/public/anonymous-2026-09-10/headers.txt`, SHA-256 `fd43ce676ffdc7977b5aa1418c28ddc495f5839bea20261b10f03e7dea53f0be`.
- Raw full SSR reader HTML: `articles/RU-01/evidence/public/anonymous-2026-09-10/page.html`, SHA-256 `a57f533f89a9d5d9170f36dd6f178e1cb2155f5876bd1f4a3043b5ccde385808`.
- The one ordinary anonymous GET returned HTTP/2 200 at `Thu, 10 Sep 2026 08:42:59 GMT`. The article is present in SSR markup; this is not an empty-shell inference.

## Public findings

| ID | Status | Rule / observed public difference | Minimal human correction |
| --- | --- | --- | --- |
| PUBLIC-RENDER-001 | OPEN | The two reader-visible untested brief templates no longer preserve the canonical blockquote/line structure. Canonical `article.html` has two `<blockquote><p>` blocks, each with six `<br>`-separated fields. The public SSR article has zero `<blockquote>` and zero `<br>` elements; each six-field template is one run-on `<p>`. All words remain, but the designed field-by-field brief is visibly collapsed. | In vc.ru, restore each template as six visibly separate lines in a quote/indented block (or equivalent native formatting) without changing text, links, disclosure, images, or facts; then provide fresh public evidence for a new R-P. |
| PUBLIC-RENDER-002 | OPEN | Each of the three public media blocks adds a visible `media-title` that exactly repeats that image’s ALT. This title is not in canonical `article.md`/HTML or the reviewed reader payload. It appears before the intended adjacent Russian editorial-illustration disclosure, creating duplicate visible image text. The actual `img alt` values themselves correctly match the manifest. | In the native image controls, remove the three visible ALT-duplicate titles/captions while preserving each image’s ALT and the immediately following editorial-illustration disclosure. If vc.ru cannot separate title/caption from ALT, return that observed limitation rather than guessing. Re-capture the public reader page. |

## Field-by-field comparison

| Surface | Result | Evidence |
| --- | --- | --- |
| Reachability / reader body | PASS | HTTP/2 200; SSR has full article body, not a partial shell. |
| Public title and H1 | PASS | H1 exactly matches the canonical/platform title. Browser `<title>` adds the normal vc.ru/author suffix. |
| H2/H3 order | PASS | Public article has H2 × 6 and H3 × 3 in the canonical order. |
| Reader prose, disclosure, facts | PASS except findings above | Full disclosure is present first; the narrow brief-preparation angle, VideoWeb attribution, no-independent-test limitation, and fact/parameter/free/Trends boundaries remain intact. |
| Fixed links | PASS with platform wrapper recorded | Exact Russian anchors are present once each. vc.ru wraps both authored hrefs in its `api.vc.ru/v2.8/redirect?to=` URL, but decoding `to` yields exactly the two frozen VideoWeb URLs, once each. No extra authored VideoWeb destination appears. |
| Images, order and ALT | PASS for source-level delivery | Three public media blocks occur LEAD/MIDDLE/CLOSING in the canonical positions; each has the exact Russian ALT from the manifest. `PUBLIC-RENDER-002` concerns the additional visible title, not the ALT value. |
| Captions / adjacent disclosure | CHANGES | The three intended Russian editorial-illustration disclosures remain adjacent after their respective images, but each is preceded by an unplanned visible ALT duplicate (`PUBLIC-RENDER-002`). |
| Internal-operation leakage | PASS | No Chinese insertion cards, copy-target names, release instructions, TAGS/SEO-control text, hashes, or other operator instructions occur in the SSR article body. |
| Public meta description / tags | UNVERIFIED / platform-controlled difference | Public description is `Бриф для ролика Seedance 2.5, MiniMax H3, проверяемые кадры, планирование, критерии проверки, создание короткого видео`, not the local supplied SEO description. Public JSON-LD has `keywords: []`. Local package explicitly records vc.ru native description/tags support as `UNVERIFIED`, and the frozen contract requires separate local fields rather than public native support; this observation is not an additional blocking finding. |
| Robots / indexing | UNVERIFIED / platform-controlled | The anonymous response has `x-robots-tag: noindex`. No frozen requirement requires indexability, so this is recorded rather than promoted to a quality finding. |

## Remaining UNVERIFIED surfaces

- `HUMAN_ACCEPTED` / human native reader acceptance is absent.
- No screenshot or raster-render capture was available in this R-P. The SSR article markup proves source-level image position, ALT and visible caption/title text, but public pixel identity, final CSS paint, viewport behavior and screen-reader exposure are not independently verified.
- Native vc.ru support and persistence for TAGS, SEO description, image ALT versus visible title/caption, account/policy status, and publication eligibility remain unverified beyond the observed reader markup.

## Finding continuity and next action

Pre-public `DELIVERY-ALT-CONTRACT-001` remains `RESOLVED` per `review-report-2.md`; it is unrelated to these public rendering defects. `PUBLIC-RENDER-001` and `PUBLIC-RENDER-002` are new, open public-reader findings. The minimal next action is a human-only native correction of those two formatting/caption surfaces, followed by a fresh anonymous R-P and later fresh G-P. Do not treat this report, the URL, or HTTP 200 as final public completion.

## Inputs re-read

`writer-review-3p/SKILL.md`; campaign `campaign.config.json`, `confirmation.md`, `requirements-contract.md`, `r3/state.json`; RU `assignment.json`, `research-status.json`, all `r3/{research-review-1.md,review-report-1.md,review-report-2.md,gate-report.md,gate-report-1.md,finding-resolutions-1.md,editor-preflight-diff-1.md,w-local-alt-parity-check-2.md,writer-handoff-1.md,w-local-check-1.md}`; canonical article; `evidence/product-facts/fact-boundaries.md`; and final vc.ru `visual-payload.html`, fingerprint, transport/local-SEO, image manifest, links, metadata, release card, checklist, content files and images.
