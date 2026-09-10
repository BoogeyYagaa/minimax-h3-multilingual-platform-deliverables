verdict: PUBLIC_QA_DEFERRED
article_id: EN-07
platform: LinkedIn
gate: ARTICLE_PUBLIC_GATE (fresh, on-disk evidence only)

# EN-07 LinkedIn public gate 1

## Decision

`PUBLISHED` and public QA remain distinct. The native receipt records exactly one LinkedIn Publish action and an authenticated reader-side 40/40 block check, so it supports `PUBLISHED_PENDING_INDEPENDENT_PUBLIC_QA`. It is publication evidence only; it cannot establish anonymous reader accessibility or parity.

The only supplied anonymous reader retrieval followed the canonical `www.linkedin.com` URL through a `302` to `www.linkedin.cn`, then received `451` with a zero-byte final entity. It exposed no reader document. This does **not** prove deletion, publication failure, general anonymous unavailability, or a content defect. It leaves the body/order, title and heading rendering, links, founder disclosure, images/ALT/captions, metadata, author/canonical URL, and public image bytes `UNVERIFIED`.

`HUMAN_ACCEPTED` remains `NOT_YET_PROVIDED`. Therefore EN-07 is not `PUBLIC_QA_PASSED`, is not complete, and must not be harvested. No `PUBLIC-RENDER-*` finding is opened: an empty inaccessible entity cannot reproduce a reader-visible mismatch.

## Evidence consumed

| Evidence | SHA-256 | Gate use |
| --- | --- | --- |
| `articles/EN-07/r3/full-review-2.md` | `9740ea41a68f948fcfc0941bff5f489912a4c1cff79d67cb07ee701fedabaf44` | Local package R2 approved; no open local R finding. |
| `articles/EN-07/r3/gate-report-1.md` | `7ddfc033c597b95c05297a6cdf7fbf4e7ef1353c0ab1919e5d85b5b722a34f2e` | Local G result is `HUMAN_RELEASE_READY` only. |
| `articles/EN-07/human-release/LinkedIn/fingerprint.json` | `dfa1a1daad197258828ed238be5e6ffa50f88844ea0fd3f961b04ee6c36300b6` | Canonical public-comparison baseline. |
| `articles/EN-07/human-release/LinkedIn/visual-payload.html` | `ab360896ad915f8590a5c5850d97c425b0628c09f6ecd84ad40760f3110a58e5` | Local final payload only; it is not a public render. |
| `articles/EN-07/human-release/LinkedIn/transport-check.md` | `b18d8cf47ab2a72b7c45d220cf0c1067d32db24565f8940843faa8e40d9bf01a` | Confirms local transport checks; expressly excludes publication and public rendering. |
| `articles/EN-07/human-release/LinkedIn/local-seo-issues-reference.md` | `f01ed2a2de1b800cb0f4dcff32801bd49fff01310e45900615f234b1c229f2b4` | Local controllable fields only. |
| `articles/EN-07/human-release/LinkedIn/RELEASE-CARD.md` | `1d2e510503204c3440c2aa8a3e101f1b4aa7be92080ac9a2d9ce850c70cf670c` | Requires a public URL plus `HUMAN_ACCEPTED` or `HUMAN_NEEDS_FIX`; neither is supplied. |
| `publication-automation/EN-07-linkedin-editor-transport-blocker.json` | `b8fff60cff8342204cf181b8a42e6f7738f6d61a603ad6812b78701e31bcdfd8` | Native receipt, authenticated 40/40 reader check, and one Publish action; not anonymous-public proof. |
| `evidence/cu-cdp-switch-authorization.json` | `692df91a6e6d2e74782b9d2838f24f3da392995a4ad351f4808ea480f15c4f16` | Historical control-path authorization only; it does not alter QA semantics. |
| `articles/EN-07/r3/public-review-1.md` | `dec7a1571c126a40624927b8c0353a34a72dca3eafcc5c7e998c0047a7c952de` | R-P found no reproducible mismatch, while preserving every unavailable public surface as unverified. |
| `articles/EN-07/evidence/public-reader-1.json` | `de7d032cd3f8f72fa7a22736e34526e612d1925f3250d3d506a0427bace8d33a` | Anonymous chain: `www.linkedin.com` 302, then `www.linkedin.cn` 451. |
| `articles/EN-07/evidence/public-reader-1-body.html` | `e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855` | Final entity is empty (0 bytes). |

## Required next evidence

Any recheck needs both (1) fresh anonymous, accessible reader-page evidence that exposes the final reader document and permits the fingerprint surfaces to be compared, and (2) the human's explicit `HUMAN_ACCEPTED`. The article-scoped R-P must then compare the newly accessible reader evidence; a fresh G-P must make the next public-gate decision.

This is an evidence handoff, not an instruction to change author identity, share, repost, edit, publish again, or otherwise alter the LinkedIn item.

## Required root-state update

Update `r3/state.json` only through the campaign controller, preserving the already-recorded publication fact:

- `publication.article_release_packages["EN-07"].status`: `PUBLIC_QA_DEFERRED`
- `publication.article_release_packages["EN-07"].publication_status`: retain `PUBLISHED_PENDING_INDEPENDENT_PUBLIC_QA`
- `publication.article_release_packages["EN-07"].public_gate`: `PUBLIC_QA_DEFERRED`
- `publication.article_release_packages["EN-07"].human_acceptance`: retain `NOT_YET_PROVIDED`
- `publication.article_release_packages["EN-07"].public_review_status`: `PUBLIC_REVIEW_APPROVED` with an explicit unverified-surface limitation
- `publication.article_release_packages["EN-07"].public_review_report`: `articles/EN-07/r3/public-review-1.md`
- `publication.article_release_packages["EN-07"].public_gate_report`: `articles/EN-07/r3/public-gate-report-1.md`
- `publication.article_release_packages["EN-07"].public_evidence_hashes`: record the R-P report, anonymous JSON, and zero-byte body hashes above.
- `publication.article_release_packages["EN-07"].public_unverified_surfaces`: record every reader surface listed in the Decision section.
- `publication.article_release_packages["EN-07"].deferred`: record `ANONYMOUS_ACCESS_RESTRICTED_451_AFTER_LINKEDIN_302_REDIRECT`, the two required next-evidence conditions, and the prohibition on a duplicate final publication.

Keep `publication.public_qa_passed_count` at `0`; do not count EN-07 as complete or harvestable. The existing `publication.published_count` remains a publication counter, not a public-QA counter.
