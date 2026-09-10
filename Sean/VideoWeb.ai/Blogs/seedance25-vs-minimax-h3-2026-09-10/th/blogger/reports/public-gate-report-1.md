verdict: PUBLIC_QA_CHANGES

# TH-01 fresh public gate (G-P1)

Scope: only TH-01's frozen Thai → Blogger reader surface in campaign `videoweb-seedance25-vs-minimax-h3-short-video-2026-09-10`. This fresh G-P consumes the local R2/G1, frozen release package/fingerprint, publication and bounded native-label records, and R-P1. It does not re-review article quality, operate a browser/editor/theme, or make an external change.

## Decision and status boundary

`PUBLIC_QA_PASSED` is unavailable. R-P1 is `PUBLIC_REVIEW_CHANGES` with two OPEN public-rendering findings, and the lane records `human_acceptance: null`. Both prerequisites independently prevent a public-QA pass.

The publication record supports a limited technical state: the exact URL is recorded as `PUBLISHED_PENDING_PUBLIC_QA`, and R-P1 anonymously retrieved its public reader document with HTTP 200. The bounded native-label correction records exactly `Seedance 2.5` and `MiniMax H3`, with exact label `x` absent, and records no title/body/image/link/URL change. These are not a `HUMAN_ACCEPTED` receipt or final acceptance. `HUMAN_ACCEPTED` remains `null` / `UNVERIFIED`; this decision neither fabricates it nor treats publication/technical readability as acceptance or campaign completion.

## Inputs and gate confirmation

- Frozen requirements and authority: `requirements-contract.md`, `confirmation.md`, `campaign.config.json`. TH-01 is Thai-language readers on Blogger; public/read-only verification remains required by `REQ-PUBLICATION-001`.
- Local accepted baseline: R2 is `APPROVED`; G1 is `PASS` for the local package only. The current release `visual-payload.html` SHA-256 is `e6fdf4e446bdfc8790ff087b3a21774bf07892522e6d65a0700b7ed86188b546`, equal to the frozen fingerprint.
- Publication boundary: `publication-automation/TH-01-blogger-publication-record.json` records one native publish action and the exact public URL, explicitly directs that it not be called `HUMAN_ACCEPTED` or `PUBLIC_QA_PASSED`; `evidence/TH-01-native-label-correction.json` confines the executed correction to native labels and says the source package was unchanged.
- Independent public review: `r3/public-review-1.md` directly reports anonymous read-only GET/HEAD plus direct public HTML comparison. It verifies parity of title text, normalized post body, H2/H3 sequence, two fixed hrefs/anchors, one image's ALT/caption/placement, disclosures, canonical URL, and corrected labels; it independently leaves only the two findings below OPEN.

G-P accepts R-P1's bounded public evidence rather than repeating a prose-quality review. R-P1 also records its evidence limits: it did not separately inspect browser-pixel rendering and source-only inspection does not establish remote image-byte identity. These limits do not erase the directly evidenced structural metadata defects below, and they cannot support a broader rendering or completion claim.

## OPEN public-rendering findings

### PUBLIC-RENDER-001 — OPEN — post title is H3; template site title is the only H1

- Public evidence in R-P1: the post title is `<h3 class='post-title entry-title'>…</h3>`, while the only H1 is unrelated template/site branding, `Best Affordable AI Video Tools for Startup Growth Tests`.
- Frozen-reader basis: the release fingerprint transports the canonical article title as the separate title field with H1 semantics; public delivery must not replace the article H1 with site branding.
- Gate result: OPEN. This is a reader-surface heading-semantic defect, not a local article-quality finding.

### PUBLIC-RENDER-002 — OPEN — public document root declares English, not Thai

- Public evidence in R-P1: `<html dir='ltr' lang='en'>`, while the public post body is Thai.
- Frozen-reader basis: TH-01 is assigned `th`, and the canonical/release payload declares `lang="th"`.
- Gate result: OPEN. This is a reader-surface language-metadata/accessibility defect, not a reason to alter the accepted Thai copy.

## Minimal HUMAN_NEEDS_FIX

Owner/human approval is required before a Blogger theme/blog-language remediation because it may affect template or blog-wide behavior. After approval, the human owner must configure the applicable Blogger theme/template so that this individual post's title renders as the article H1 and the Thai reader surface emits `lang="th"` (root document, or a complete Thai article subtree only if root-level per-post language is unavailable).

The remediation must not change the approved title text, Thai body, lead image or its ALT/caption, either fixed VideoWeb link, canonical/public URL, or native labels. Do not automatically change the template, blog language, post, title, body, image, links, URL, or labels. No repost, unpublish, blind retry, or automated update is authorized by this G-P.

After an owner/human-approved remediation, obtain fresh public evidence, then run fresh TH-01 R-P followed by a fresh G-P. TH-01 remains `PUBLIC_QA_CHANGES` unless both findings are resolved, a fresh R-P returns `PUBLIC_REVIEW_APPROVED`, a fresh G-P returns `PUBLIC_QA_PASSED`, and a genuine human acceptance receipt exists; it is not completed and must not be harvested as a public-QA pass.
