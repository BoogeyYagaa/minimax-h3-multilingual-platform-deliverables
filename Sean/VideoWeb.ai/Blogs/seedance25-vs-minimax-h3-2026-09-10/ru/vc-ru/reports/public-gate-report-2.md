verdict: PUBLIC_QA_DEFERRED

# RU-01 G-P 2 — public-reader gate for vc.ru

article_id: `RU-01`  
campaign_id: `videoweb-seedance25-vs-minimax-h3-short-video-2026-09-10`  
platform/account: `{vc.ru, VIDEOWEB_OWNER_ACCOUNT_PRIORITY}`  
public_url: `https://vc.ru/id6106995/3131047-kak-sobrat-brif-dlya-produktovogo-rolika-seedance-2-5-i-minimax-h3`

## Verdict and strict boundary

`PUBLIC_QA_DEFERRED` is the only supported G-P2 verdict. `PUBLIC_QA_PASSED` is forbidden because full-article `HUMAN_ACCEPTED` is **not explicitly provided**. The user-confirmed limitation record expressly says `full_article_human_acceptance: NOT_EXPLICITLY_PROVIDED`; a returned URL, HTTP 200, anonymous SSR match, R-P2 approval, or the limited editor disposition cannot substitute for that acceptance.

This fresh G-P consumes R-P2 only. It does not redo Russian language, factual, SEO, image-quality, or native-editor review; it performs no browser, login, editor, upload, save, publish, repost, deletion, rollback, or retry action. No campaign config, root `r3/state.json`, RU lane status, canonical article, release package, or image has been modified.

## Evidence consumed

| Input | SHA-256 | G-P use |
| --- | --- | --- |
| `r3/public-review-2.md` | `8753ce08f3b0a55c3284f4e00b062c3cf5b3eb731e49987e9f5b3cf98f66e1ea` | `PUBLIC_REVIEW_APPROVED`; records the fresh comparison and bounded finding disposition. |
| `evidence/public/anonymous-rp2-2026-09-10/page.html` | `cdead2318727241a1942620d602226e775473a20e4b35bea4122e7e24dd67b44` | One new anonymous full SSR reader response, HTTP/2 200, 179863 bytes. |
| `evidence/public/anonymous-rp2-2026-09-10/headers.txt` | `fd6de2460518a7d121fd529d1d5b3650c8a3d05350369403e5f22e31a7bdabe2` | Captured response headers, including the dated HTTP 200 response. |
| `evidence/public/anonymous-rp2-2026-09-10/transfer.txt` | `abae4cf0ebcee29fdd251d0fc21c2f43990253a51eab5ca2711d80e33da85706` | Capture URL, content type/length, and successful one-GET transfer record. |
| `evidence/RU-01-user-confirmed-image-title-editor-limitation.json` | `a1f923a833c675a34091cbb32a7333607790e01bdbd746fc8edb04bb3df27217` | Exact, narrow owner disposition for repeated visible image titles only. |
| `human-release/RU-01/vc.ru/fingerprint.json` | `05aaaba1220ab73b57c67488499188c583fcaf7badbfb7c9831a7a32f7fff3b8` | Local comparison baseline: title, heading transport, fixed links, images and claim boundaries. |

The R-P2 report and the raw capture SHA-256 values above were independently recomputed from the stored files before this decision.

## Public-finding continuity

| ID | Current status | Evidence-led disposition |
| --- | --- | --- |
| `PUBLIC-RENDER-001` | `RESOLVED` | The new anonymous SSR response has two six-field templates with five real `<br />` line breaks each (ten total). The native reader uses paragraphs instead of canonical blockquotes, but the six visible lines are the required scoped equivalent. R-P2 records no body, title/heading, link, disclosure, image-order/ALT, or operator-leakage regression. |
| `PUBLIC-RENDER-002` | `USER_CONFIRMED_EDITOR_LIMITATION_NO_REPAIR_REQUIRED` | The three visible image titles still repeat their ALT. The exact owner record scopes the limitation to those repeated titles only. This item is no longer a repair-list item, but it is **not `RESOLVED`** and this report does not claim a public render fix. |
| `DELIVERY-ALT-CONTRACT-001` | `RESOLVED` (pre-public) | R-Delta 2 remains closed; R-P2 confirms the three public ALT values match the reviewed Russian manifest. It is not reopened by the visible-title limitation. |

There are no remaining OPEN public-quality repair findings after the verified template repair and the strictly limited owner disposition. The absence of an OPEN repair item does not complete public QA without explicit human acceptance.

## Limitation scope and still-unverified surfaces

The `PUBLIC-RENDER-002` disposition does **not** waive, repair, or accept any other surface. In particular, it does not extend to template rendering, metadata/tag behavior, robots/indexing behavior, or full-article human acceptance.

- Template rendering is separately `RESOLVED` by the fresh anonymous SSR evidence above, not by the title limitation.
- Native vc.ru metadata-field persistence and semantics (SEO description, tags, image ALT/title/caption controls) remain `UNVERIFIED`; public description variance and empty JSON-LD keywords remain platform-controlled observations, not a claimed fix.
- Robots/indexing remains `UNVERIFIED`; the captured `x-robots-tag: noindex` is an observed response header, not an accepted or repaired condition.
- Public pixels, final CSS paint, responsive behavior, and screen-reader exposure remain `UNVERIFIED` because no screenshot/raster evidence was supplied.

## Exact required human input

For this exact public URL, provide an explicit full-article acceptance token: `HUMAN_ACCEPTED`. It must represent acceptance of the reader page as a whole, not merely the image-title editor limitation.

If the reader page is not accepted, provide `HUMAN_NEEDS_FIX` and name the failed reader-check item(s). Do not infer acceptance from silence, the prior URL return, the HTTP response, or R-P2. No additional editor repair is requested by this G-P for `PUBLIC-RENDER-002`.

After explicit `HUMAN_ACCEPTED`, the campaign controller may record the acceptance and consume this fresh G-P evidence; until then RU-01 is deferred, is not `PUBLIC_QA_PASSED`, does not count toward the public-QA target, and is not eligible for harvest or public-completion claims.
