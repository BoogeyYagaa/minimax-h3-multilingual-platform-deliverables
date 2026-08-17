# DEV platform audit

## Verdict

`APPEAL SENT — AWAITING DEV RESPONSE; HUMAN TECHNICAL REVIEW REQUIRED`

This is a completed editorial package, not a publication approval.

## Task card

- Reader: German-speaking developers and technical marketers implementing a SaaS explainer workflow.
- Type: technical implementation tutorial.
- Core idea: generated metaphor and real UI require separate evidence paths.
- Main phrase: SaaS-Erklärvideos mit MiniMax H3.
- Tone: technical, restrained, no first-person testing claim.
- Must include: official API request, polling flow, UI boundary matrix, error handling, human gate.
- Must avoid: commercial promotion, affiliate link, invented endpoint, unexecuted-success claim.
- Sources: MiniMax official global documentation and DEV official AI policy.
- Output: DEV Markdown with four tags and unpublished front matter.

## Checks

| Area | Result | Evidence |
|---|---|---|
| Technical scope | Pass with human gate | Uses official `v2/video_generation`, query path, model name and documented fields. |
| Code status | Explicit limit | Article states examples were checked against docs but not run against a real account. |
| AI disclosure | Pass | Disclosure appears before the body and requires a human author to stand behind the work. |
| Commercial promotion | Pass | No Best Image AI, affiliate, referral, tracking or business CTA links. |
| UI truth | Pass | Matrix separates generated metaphor from real product evidence. |
| DEV tags | Pass | Exactly four technical tags. |
| Local duplicate check | Pass with boundary | Local `writer/output` contains no MiniMax H3 DEV package; remote account history remains unverified. |
| Publication status | Hold | The logged-in DEV account returned `Forbidden` because it is suspended. An authorized restoration appeal was sent to `support@dev.to` on 2026-08-17; human technical and policy responsibility remains required after access is restored. |

## Fact ledger

| Claim | Evidence | Action |
|---|---|---|
| H3 accepts text, image, video and audio | MiniMax official video guide | Keep and cite |
| Resolution is 768P/2K and duration 4–15 seconds | MiniMax official video guide/API reference | Keep and cite |
| Create endpoint is `POST /v2/video_generation` | MiniMax official V2 API reference | Keep and cite |
| Query path returns `task.content.url` after success | MiniMax official guide/API response | Keep and cite |
| Text-to-video requires concrete `ratio` | MiniMax official V2 API reference | Keep and explain |
| Code has run successfully | No execution evidence | Explicitly not claimed |

## Humanization pass

- Voice target: German developer tutorial with direct engineering boundaries and no promotional enthusiasm.
- Patterns revised: converted marketing examples into an evidence matrix, API flow and failure model.
- Meaning and verified claims preserved: yes.
- Code, field names, URLs and uncertainty rechecked: yes.
- Remaining risk: DEV must respond to the appeal and restore posting access, and only the human publisher can satisfy DEV’s requirement to understand and stand behind the technical content.

## Sources

- [DEV guidelines for AI-assisted articles](https://dev.to/guidelines-for-ai-assisted-articles-on-dev/)
- [DEV writing and editing help](https://dev.to/help/writing-editing-scheduling)
- [MiniMax H3 video generation guide](https://platform.minimax.io/docs/guides/video-generation)
- [MiniMax H3 V2 create task reference](https://platform.minimax.io/docs/api-reference/video-generation-v2-create)
