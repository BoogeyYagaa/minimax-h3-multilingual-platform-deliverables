verdict: PUBLIC_QA_CHANGES
scope: EN-08_PUBLIC_GATE_READONLY
article_id: EN-08
platform: PromoteProject / VIDEOWEB_OWNER_ACCOUNT_PRIORITY
public_url: https://www.promoteproject.com/article/227862/seedance-25-vs-minimax-h3-a-video-creative-testing-plan-for-short-video-creation
date: 2026-09-10

# EN-08 independent public gate report 1

## Public verdict

`PUBLIC_QA_CHANGES`.

The public reader evidence is sufficient to preserve the R-P conclusion `PUBLIC_REVIEW_CHANGES`: three stable public-rendering findings remain OPEN. The local `PASS` in `gate-report-1.md` established only `HUMAN_RELEASE_READY`; it neither proves nor cures public-reader parity. This G-P makes no editor, account, browser, public-site, root-state, or external-system action.

`HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. It is an independent required human result, not something established by the public URL, HTTP 200, matching fields, the user limitation report, R-P, or this G-P. Therefore this report cannot be `PUBLIC_QA_PASSED`.

## Evidence read

- Frozen public-comparison contract: `human-release/PromoteProject/fingerprint.json`, SHA-256 `93457d23f045547a0964ae4884dfc0c667871c2d3c186668a7fd625b76e29c45`.
- Independent R-P: `r3/public-review-1.md`, verdict `PUBLIC_REVIEW_CHANGES`, SHA-256 `675e4b8adcdd12f41a08537f87aae8794b0fd08b8e0e912766e6146e015ffea3`.
- Anonymous public-reader record: `evidence/public-reader-1.json`, SHA-256 `81daee0290cdad0dc07e9d30814d591ca1c96a04022866385f6be0e581333a51`; it records public HTML SHA-256 `92060d14bfdb3246ae77ef08cb182a17951166b5d0bb90a8f1cff035646a579d` and article-fragment SHA-256 `c54615ef3ec4b125e0d8d4c779539a89629a829db9f39b2b335247850f00a33c`.
- User-returned URL/limitation record: `../../../evidence/EN-08-user-publication-url-and-image-limitation.json`, SHA-256 `e0a775fa5b95974470d5789bbbb81b2a63b34524b49c67df8a92a73b73503b2a`.
- Full EN-08 local research, R1/R2, repair, local-G, requirements, release-package, and traceability history. Local findings `VISUAL-NARRATIVE-001` and `VISUAL-ASPECT-001` remain resolved for the canonical/release assets only; they are not relabelled by the distinct public finding below.

## Confirmed public matches

- The title is the exact frozen title in the document title, Open Graph title, and article H1.
- All 41 normalized non-image/non-caption canonical body units occur in the public article in order. The public article body has zero H1, as required by `SEPARATE_TITLE_FIELD` transport.
- All three required H3 FAQ questions match in text and order.
- The founder disclosure text is present near the start of the public article. The distinct disclosure-before-approved-lead-image arrangement remains failed only through `PUBLIC-RENDER-002`, because the observed cover is before that disclosure and no approved lead image is attributable on the reader page.
- The Google Ads anchor/href pair matches once, as do both required VideoWeb anchor/href pairs: `Seedance 2.5 short-video workflow` to `https://videoweb.ai/model/seedance-2-5/`, and `VideoWeb’s MiniMax H3 workflow page` to `https://videoweb.ai/model/minimax-h3/`.
- The reader retains the provider-attribution, eligible-campaign, control/one-variable, prerequisite, selected-metric, and no-executed-test/no-winner boundaries.
- No temporary Chinese image insertion card, planned local filename, or operation text entered the public reader body.

## Exact stable public-finding mapping

| Stable finding | Status | Public evidence and exact disposition | Frozen requirement relationship |
| --- | --- | --- | --- |
| `PUBLIC-RENDER-001` | OPEN | The three existing strings `What a video creative testing plan is—and is not`, `Declare one creative variable: the opening hook`, and `FAQ` are public paragraphs with `<br>`, not H2 elements. Their prose and order remain intact. Carry the R-P finding unchanged; do not create a duplicate heading finding. | `REQ-PAYLOAD-001` public heading transport; no canonical wording change is indicated. |
| `PUBLIC-RENDER-002` | OPEN | Actual image state is one responsive platform cover after the article H1 and before the disclosure, with empty ALT and no caption; there are zero article-body images, all three planned in-body images and captions are absent, and no temporary insertion cards are present. The cover's bytes, pixels, intrinsic ratio, identity as approved image 01, load/render state, and reader readability are UNVERIFIED. Carry the R-P finding unchanged; it is a new public-rendering issue, not a reopening of either resolved local visual finding. | `REQ-PAYLOAD-001` and the public-reader part of `REQ-PUBLICATION-001`: required LEAD/MIDDLE/CLOSING public image/caption parity is not demonstrated. |
| `PUBLIC-RENDER-003` | OPEN | The public description is platform-generated/truncated; public meta keywords are `seedance,2.5,minimax,h3`; visible tags are `SEEDANCE`, `2.5`, `MINIMAX`, `H3`; and JSON-LD adds generic startup terms. These differ from the frozen raw SEO description and raw TAGS. Author control of these fields is UNVERIFIED. Carry the R-P finding unchanged; do not turn the difference into body text. | `REQ-PAYLOAD-001` raw SEO-description/TAGS mapping; no platform-control conclusion is inferred. |

No new stable public finding is created. The absent `HUMAN_ACCEPTED` value is kept separate from the three public-rendering findings and is not given a substitute finding ID.

## Image-limitation and acceptance boundaries

The user statement is exactly `USER_REPORTED_UPLOAD_LIMITATION`: `编辑区或网络原因无法上传图片`. Its recorded root cause is `UNDETERMINED_EDITOR_OR_NETWORK`, and its scope is this EN-08 publication attempt only.

It does not prove a PromoteProject limitation, editor capability, network cause, field availability, a successful image upload, an image waiver, or an `ACCEPTED_PLATFORM_LIMITATION` disposition. No owner acceptance of an image limitation is present. This G-P does not require the user to make another upload attempt.

The reported limitation likewise does not establish `HUMAN_ACCEPTED`. Only an explicit human return of `HUMAN_ACCEPTED` or `HUMAN_NEEDS_FIX` can resolve the missing human-result surface; either result remains independent of the public evidence and does not silently close the three OPEN findings.

## Human-only next steps

1. No corrective reattempt is demanded. If the owner later elects to correct the native post, that work is human-only and must preserve existing reader wording, URLs, and claim boundaries.
2. For an owner-chosen correction, the existing R-P target state is the only scope: retain the three downgraded strings in place as H2; restore the three approved LEAD/MIDDLE/CLOSING assets with their captions and any available native ALT controls; and map the frozen raw SEO description/TAGS only if the native author-controlled fields actually exist. An unavailable field must remain recorded as unavailable, not silently treated as accepted or waived.
3. The owner may separately return an explicit `HUMAN_ACCEPTED` or `HUMAN_NEEDS_FIX`. This is still needed for the human-acceptance record, but does not override public parity evidence.
4. If the public page changes or a human result is supplied, capture fresh read-only public evidence and repeat the article R-P then fresh G-P. Until then, do not harvest, mark completion, or report `PUBLIC_QA_PASSED`.

## Results

- Public verdict: `PUBLIC_QA_CHANGES`.
- R-P conclusion consumed: `PUBLIC_REVIEW_CHANGES`.
- Stable public findings: `PUBLIC-RENDER-001`, `PUBLIC-RENDER-002`, and `PUBLIC-RENDER-003` are all OPEN.
- Human acceptance: `NOT_YET_PROVIDED`.
- Image limitation: `USER_REPORTED_UPLOAD_LIMITATION` only; root cause `UNDETERMINED_EDITOR_OR_NETWORK`; no waiver or accepted limitation.
