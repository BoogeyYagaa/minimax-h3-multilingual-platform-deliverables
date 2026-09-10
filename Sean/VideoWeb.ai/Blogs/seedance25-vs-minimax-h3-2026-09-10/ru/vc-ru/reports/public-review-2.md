verdict: PUBLIC_REVIEW_APPROVED

# RU-01 independent public-reader review 2 — VideoWeb campaign

## Scope and completion boundary

This R-P2 rechecks only the remaining public-template rendering finding and its direct reader-visible dependencies, using a new anonymous capture. It is not a G-P verdict, not `HUMAN_ACCEPTED`, and not final public completion.

The owner record `evidence/RU-01-user-confirmed-image-title-editor-limitation.json` applies only to the repeated visible image titles. It does not establish full-article human acceptance; its explicit value is `NOT_EXPLICITLY_PROVIDED`.

canonical_payload_fingerprint: `human-release/RU-01/vc.ru/fingerprint.json` SHA-256 `05aaaba1220ab73b57c67488499188c583fcaf7badbfb7c9831a7a32f7fff3b8`; canonical Markdown SHA-256 `9e6e6030cb9db3e47f7be600b7f6dd96d83dab6f256c4a08f42c8ffddf54d321`; canonical HTML SHA-256 `6d0012dabf1ef73a9ecbeb8c29d22c1083da150ca12d705ea7923dfbeff4823f`; visual payload SHA-256 `1d32ac596f7a480be48171e10d3aae69ddb5d8fb699e45226c45587ce70c0a2d`.

public_url: `https://vc.ru/id6106995/3131047-kak-sobrat-brif-dlya-produktovogo-rolika-seedance-2-5-i-minimax-h3`

## Fresh anonymous evidence

- `articles/RU-01/evidence/public/anonymous-rp2-2026-09-10/capture-manifest.md`.
- Raw headers SHA-256: `fd6de2460518a7d121fd529d1d5b3650c8a3d05350369403e5f22e31a7bdabe2`.
- Raw full SSR reader HTML SHA-256: `cdead2318727241a1942620d602226e775473a20e4b35bea4122e7e24dd67b44`.
- Transfer record SHA-256: `abae4cf0ebcee29fdd251d0fc21c2f43990253a51eab5ca2711d80e33da85706`.
- The one new GET returned HTTP/2 200 at `Thu, 10 Sep 2026 09:31:46 GMT`, 179863 bytes. This is a fresh response and not an inference from the unchanged callback URL: its raw HTML hash and byte length differ from R-P1’s capture.

## Stable public-finding status

| ID | R-P1 status | R-P2 status | Exact current evidence / disposition |
| --- | --- | --- | --- |
| PUBLIC-RENDER-001 | OPEN | RESOLVED | The fresh public reader has two template paragraphs with five real `<br />` elements each (ten total), preserving all six fields as reader-visible separate lines. R-P1’s independent response had zero template line breaks. vc.ru still uses a paragraph rather than canonical `<blockquote>`, but the visible six-line native equivalent satisfies the scoped repair; no wording, link, disclosure, image, or fact change is present. |
| PUBLIC-RENDER-002 | OPEN | USER_CONFIRMED_EDITOR_LIMITATION_NO_REPAIR_REQUIRED | The owner’s explicit scope is only the visible media titles that repeat ALT. The fresh reader still has three such titles; this report does **not** claim a rendering change or mark the finding `RESOLVED`. It is an accepted editor limitation with no retry/repair required, not an OPEN public-quality repair item. |
| DELIVERY-ALT-CONTRACT-001 | RESOLVED pre-public | RESOLVED | No re-opening: the three public ALT values remain the reviewed Russian manifest values. |

There are no OPEN public-quality findings after applying the narrowly scoped owner-confirmed limitation.

## Fresh comparison and regression spot-check

| Surface | Result | Evidence |
| --- | --- | --- |
| Two brief templates | PASS | Each public six-field template now has five actual `<br />` separators. The source has zero `<blockquote>` tags, but the lines are independently present in this new SSR reader response rather than inferred from prior evidence. |
| Title / H1 / H2-H3 | PASS | H1 exactly matches the canonical/platform title; public body has H2 × 6 and H3 × 3 in the canonical sequence. |
| Complete reader prose / founder disclosure | PASS | Full Russian body is present; opening disclosure remains first and exactly identifies the author as `основатель VideoWeb AI` with no independent-results test. |
| Two fixed destinations and anchors | PASS with vc.ru wrapper recorded | Both Russian anchors occur once. Each vc.ru redirect wrapper’s decoded `to` parameter is exactly one frozen VideoWeb destination; no extra authored VideoWeb target appears. |
| Images, positions and ALT | PASS for source-level delivery | Three media blocks occur in the canonical LEAD/MIDDLE/CLOSING positions. Each has the exact Russian ALT in the manifest; all three editorial-illustration disclosure paragraphs remain after their images. |
| Repeated visible image titles | Accepted limitation | The three titles still repeat the ALT before the disclosure. This is exactly `PUBLIC-RENDER-002`’s owner-confirmed limitation; no caption/ALT separation retry was required or performed. |
| Operator-instruction leakage | PASS | No Chinese insertion-card content, copy-target/control name, release instruction, TAGS/SEO-control text, hash, or internal workflow text appears in the public SSR article body. |
| Public metadata / robots | UNVERIFIED / platform-controlled | Public description still differs from the local supplied SEO description; JSON-LD `keywords` remains empty; response includes `x-robots-tag: noindex`. Native metadata behavior and indexability are not frozen public requirements, so these are observations rather than quality findings. |

## Remaining UNVERIFIED surfaces

- Full-article `HUMAN_ACCEPTED` remains `NOT_EXPLICITLY_PROVIDED`; this R-P approval must not be used as final public completion.
- No screenshot/raster evidence was supplied. Public pixels, CSS paint, responsive viewport behavior and screen-reader exposure remain `UNVERIFIED`; SSR supplies source-level reader evidence only.
- Native vc.ru metadata-field persistence, image ALT/title/caption semantics, account/policy state and publication eligibility remain unverified beyond the observed public markup.

## Inputs re-read

Current RU-01 canonical article and release package/fingerprint/transport/local-SEO/links/image manifest; all current RU-01 local R/G reports including `public-review-1.md` and `public-gate-report-1.md`; `evidence/RU-01-user-confirmed-image-title-editor-limitation.json`; and the new anonymous raw headers/HTML capture. No other campaign or brand was consulted.

`PUBLIC_REVIEW_APPROVED` here means only that the current public reader comparison has no remaining OPEN quality finding after the owner-confirmed limited disposition. It does not authorize a G-P pass, publication, further editor action, or final completion without explicit full-article `HUMAN_ACCEPTED` and a fresh G-P.
