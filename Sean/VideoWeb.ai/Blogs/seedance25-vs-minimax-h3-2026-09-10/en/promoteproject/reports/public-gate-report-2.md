verdict: PUBLIC_QA_CHANGES
scope: EN-08_FRESH_PUBLIC_GATE_READONLY
article_id: EN-08
platform: PromoteProject / VIDEOWEB_OWNER_ACCOUNT_PRIORITY
public_url: https://www.promoteproject.com/article/227862/seedance-25-vs-minimax-h3-a-video-creative-testing-plan-for-short-video-creation
date: 2026-09-10

# EN-08 fresh independent public gate report 2

## Decision and boundary

`PUBLIC_QA_CHANGES`.

This fresh G-P decision is made from the current on-disk canonical package, public-reader record, R-P report, owner metadata-disposition evidence, and the EN-08 local review chain. It does not reuse the earlier G-P decision as authority. I made no public fetch, browser, editor, account, upload, save, publish, repost, deletion, MusicMaker, or campaign/root-state action.

The frozen package requires `SEPARATE_TITLE_FIELD` transport with eight body H2s and three H3s, plus three approved LEAD/MIDDLE/CLOSING images with reviewed captions and ALT. The public record independently supports the matching title/article H1, all 41 normalized non-image/non-caption body units in order, zero body H1s, all three H3s, the disclosure text, all three required links, and no leaked image-operation cards. Those matches do not cure the remaining public-rendering differences below.

`HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. The URL, HTTP 200 result, public-source observations, the owner metadata disposition, and this report are not human acceptance and cannot support `PUBLIC_QA_PASSED`.

## Evidence independently consumed

- Canonical public-comparison contract: `human-release/PromoteProject/fingerprint.json`, SHA-256 `93457d23f045547a0964ae4884dfc0c667871c2d3c186668a7fd625b76e29c45`.
- Public reader evidence: `evidence/public-reader-1.json`, SHA-256 `81daee0290cdad0dc07e9d30814d591ca1c96a04022866385f6be0e581333a51`; it records an anonymous HTTP 200 observation, public HTML SHA-256 `92060d14bfdb3246ae77ef08cb182a17951166b5d0bb90a8f1cff035646a579d`, and article-fragment SHA-256 `c54615ef3ec4b125e0d8d4c779539a89629a829db9f39b2b335247850f00a33c`.
- R-P comparison: `r3/public-review-1.md`, SHA-256 `675e4b8adcdd12f41a08537f87aae8794b0fd08b8e0e912766e6146e015ffea3`.
- Metadata-only disposition: `r3/public-review-1-metadata-limitation-disposition.md`; source owner record `../../../evidence/EN-08-user-confirmed-metadata-editor-limitation.json`, SHA-256 `9a19fa50eb9aba732489536cdf2d7f2fc2ceae2890f3645eb70078ad53b257a0`.
- Image-limitation boundary: `../../../evidence/EN-08-user-publication-url-and-image-limitation.json`, SHA-256 `e0a775fa5b95974470d5789bbbb81b2a63b34524b49c67df8a92a73b73503b2a`.

## Exact public-finding mapping

| Finding | Current disposition | On-disk public observation | Requirement relationship and gate effect |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | **OPEN** | `What a video creative testing plan is—and is not`, `Declare one creative variable: the opening hook`, and `FAQ` are public paragraph elements with `<br>`, rather than H2 elements. Their text and order are present. | `REQ-PAYLOAD-001` heading transport is not publicly met. This remains a repairable public-rendering finding. |
| `PUBLIC-RENDER-002` | **OPEN** | The public source has one responsive cover before the disclosure, with empty ALT and no caption, and zero article-body `<img>` elements. The three approved LEAD/MIDDLE/CLOSING assets, their captions, and their local filenames are absent. The cover's bytes, pixels, intrinsic ratio, approved-asset identity, load state, and readability are unverified. | `REQ-PAYLOAD-001` and the public-reader part of `REQ-PUBLICATION-001` are not demonstrated. This is a distinct public image/caption parity finding, not a reopening of the locally resolved visual findings. |
| `PUBLIC-RENDER-003` | **USER_CONFIRMED_EDITOR_LIMITATION_NO_REPAIR_REQUIRED** | The public description, keywords, visible tags, and JSON-LD keywords differ from the frozen raw SEO description and TAGS. The non-parity remains recorded in the public-reader evidence. | Applies only to description/tags. It is removed from repair/retry instructions, but has not been repaired, transferred, or shown to be supported by an editor field. It does not close either remaining finding or establish human acceptance. |

No new stable finding is created. The two OPEN findings and the metadata-only disposition are intentionally separate concepts.

## Image-report boundary

The upload statement remains `USER_REPORTED_UPLOAD_LIMITATION` for this EN-08 publication attempt only, with root cause `UNDETERMINED_EDITOR_OR_NETWORK`. It establishes neither a PromoteProject-wide platform limitation nor an editor or network cause. It is not an image waiver, an accepted image limitation, a successful upload, or a finding resolution.

## Minimal human-only route for the remaining findings

No action was performed or requested from an editor in this gate. If the owner elects to correct the native post, the minimum human-only scope is:

1. For `PUBLIC-RENDER-001`, keep the three existing strings and their locations, but restore each as an H2. Do not change canonical prose, links, disclosure, or claim boundaries.
2. For `PUBLIC-RENDER-002`, place the three already-approved local assets at their declared LEAD/MIDDLE/CLOSING anchors, retain the reviewed captions, and set the reviewed ALT only where the native UI actually exposes an ALT control. A generic cover is not a substitute for this parity evidence.
3. Do not retry or repair `PUBLIC-RENDER-003`; do not move raw metadata into the reader body. Its metadata non-parity remains documented under the scoped owner disposition.

Any reader-visible canonical wording, link, image-asset, ALT, caption, or metadata-value change must return through W and the same article R before a regenerated package. A native-only correction that preserves the canonical package still requires fresh public evidence, R-P, and a new fresh G-P.

## Acceptance and completion boundary

The owner must separately provide an explicit `HUMAN_ACCEPTED` or `HUMAN_NEEDS_FIX`; neither is supplied by the current records. `HUMAN_ACCEPTED` alone would not override `PUBLIC-RENDER-001` or `PUBLIC-RENDER-002`. Until the two OPEN public findings are resolved with fresh public evidence and the acceptance boundary is independently met, EN-08 remains in `PUBLIC_QA_CHANGES`; it is not `PUBLIC_QA_PASSED`, complete, or eligible for harvest.
