verdict: PUBLIC_QA_DEFERRED
role: ARTICLE_PUBLIC_GATE
gate: fresh independent public G-P; current on-disk evidence only
article_id: EN-04
platform: Tumblr
public_url: https://www.tumblr.com/videowebai/827355403965890560/a-travel-photo-to-video-prompt-plan-three-motion?source=share
reviewed_at: 2026-09-10
human_accepted: NOT_YET_PROVIDED

# EN-04 Tumblr public gate 4

## Decision

`PUBLIC_QA_DEFERRED` is the only supported public verdict. The latest independent public R-P evidence documents an actual public reader post with current semantic structure **1 H1 / 6 H2 / 0 H3**. This retains the recovered title H1 and all six major H2 elements, but it does not match the frozen package structure of **1 H1 / 6 H2 / 3 H3**: the three subordinate motion-direction headings remain non-H3.

The user's documented statement that the editor has no H3 changes the disposition of `PUBLIC-HEADING-HIERARCHY-001` to `USER_CONFIRMED_EDITOR_LIMITATION_NO_REPAIR_REQUIRED`. It is a narrow no-repair disposition for that named heading limitation only. It neither restores H3 nor establishes native-editor capabilities beyond the user's report, and it does not make the observed public structure match the frozen structure.

`HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. The limited user-confirmed disposition is not full-article human acceptance. Accordingly, this gate does not issue `PUBLIC_QA_PASSED`, does not close public-QA as canonical-parity matched, and makes no completion, harvest, publication, or root-state determination. `PUBLIC_QA_CHANGES` is not used because the sole residual difference is explicitly recorded as no-repair-required and this gate requests no editor, alternative-editor, code-path, or public-page retry.

## Exact disposition and acceptance mapping

| Item | On-disk evidence | Gate mapping |
| --- | --- | --- |
| Frozen heading target | `human-release/Tumblr/fingerprint.json`: 1 title H1, 6 H2, and 3 named H3 motion directions | Intended package structure; not redefined by this gate. |
| Latest observed public structure | `r3/public-review-3.md` and `evidence/public-reader-observation-3.md`: 1 H1 / 6 H2 / 0 H3 | Observable non-parity remains. The title and six H2 recovery are retained; the three H3 elements are absent. |
| `PUBLIC-HEADING-HIERARCHY-001` | `evidence/EN-04-user-confirmed-no-h3-editor-limitation.json` and `r3/public-heading-limitation-addendum-1.md` | `USER_CONFIRMED_EDITOR_LIMITATION_NO_REPAIR_REQUIRED`, limited to the three subordinate motion-direction headings. This is not semantic-parity restoration or a general finding closure. |
| Body, order, list, disclosure, and two provider links | Latest R-P3 / public reader observation | Retained PASS evidence; no new public retrieval is claimed by this G-P. |
| Three images, ALT, captions, placement, and placeholder removal | Latest R-P3 / public reader observation | Retained PASS evidence; no new public retrieval is claimed by this G-P. |
| Human acceptance | User URL record and limitation record: `NOT_YET_PROVIDED` / `NOT_EXPLICITLY_PROVIDED` | No full-article `HUMAN_ACCEPTED` is present. The narrow heading disposition cannot be substituted for it. |
| Public-QA outcome | This report | `PUBLIC_QA_DEFERRED`; neither public-QA pass nor full acceptance is granted. |

## Evidence integrity

| Input | SHA-256 |
| --- | --- |
| `articles/EN-04/human-release/Tumblr/fingerprint.json` | `36d31aae752372395df92377518d674d7eee17c76d51e250a5b9a6d887db7770` |
| `articles/EN-04/r3/public-review-3.md` | `845fb6e86c81c24407dbc5bdb5b2f5aaa0b4ff3e5fde789a31aee3596af819a3` |
| `articles/EN-04/evidence/public-reader-observation-3.md` | `d0b1f719a550d45447f1f766ead513e4025e737f2b6706195ff539223d2e4c46` |
| `articles/EN-04/r3/public-gate-report-3.md` | `0b4c453d650db35d8be5d826f201709854a9ef454eeedd9ebb80f6969e39d9ae` |
| `articles/EN-04/r3/public-heading-limitation-addendum-1.md` | `22aee856320e58649cdd52408be73de918b7c319ea92c6e5d1a53bd668cad7dc` |
| `evidence/EN-04-user-confirmed-no-h3-editor-limitation.json` | `b6b3de766bbc1e4e92dfea639d57a7cae134e789ac4440cb01bd270a7f2071a7` |
| `evidence/EN-04-user-publication-url.json` | `d90a7bc6e87b76550d3a35ba198257dfe93d13b0a96181374598a53e01e5bf12` |

The public R-P3 evidence was collected before this fresh G-P and remains the only public-reader evidence relied upon here. It records actual reader content rather than an HTTP-status shell, normalized body/order/list parity, the exact founder disclosure and two provider anchor/href pairs, three public images with recorded ALT/captions/positions, and placeholder removal. This report does not convert those recorded passes into a claim that the frozen heading structure was matched.

## Boundaries and required restraint

- No H3 is claimed restored, and no native Tumblr capability, editor control, account authority, or cause is inferred beyond the user's recorded editor-limitation statement.
- No repair, alternate editor, code path, repost, replacement post, deletion, upload, save, publish, visibility change, or recheck is requested or authorized by this report.
- A future explicit full-article human acceptance, if supplied, remains distinct from this limited disposition and requires its own evidence-led acceptance assessment; it cannot be retroactively inferred from the URL, public reader evidence, or the no-H3 statement.
- No browser, public-site, editor, account, login, CDP, MusicMaker, upload, edit, save, publish, repost, delete, visibility, sharing, or root-state action occurred. This article-local report is the sole write of this G-P.
