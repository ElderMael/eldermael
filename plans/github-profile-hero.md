# PROFILE-02 Goal

## Context and goal

The current GitHub profile README has the verified portfolio-led copy and a
circuitry illustration after the profile content. Give the profile the
portfolio's visual hierarchy: a single wide, shallow, static circuitry banner
near the top, followed by native Markdown identity and actions. The banner is
an accent, not a container for essential information. Use the portfolio's
charcoal and muted green palette and retain a concise, text-first profile.

The profile owner verified the live GitHub profile and portfolio title and
tagline before this plan; the verified profile README is the baseline at
`eb6239659106fe54db71f7b71055c3b62b8e2da0`. Use the read-only portfolio
source as copy and motif evidence, not as a write target. Keep the exact
portfolio headline, “Building systems that help people build.”, and
“Miguel Enriquez · AI & systems engineering.” Actions are portfolio, contact,
and résumé, with LinkedIn retained in a secondary, unobtrusive position.
Follow with one concise, source-supported expertise line and keep both
verified OpenTelemetry links, each with a concise description supported by
`Home.tsx`.

Success: on desktop and narrow mobile GitHub-like profile views, before
scrolling, the banner is intentional and not over-tall and the profile's
identity, hierarchy, and actions are clear. If the image is blocked, all
copy and actions remain available. The named GFM image link is keyboard
accessible. The candidate adds no badges, statistics, remote embeds, scripts,
or external image dependencies. Compare the pinned baseline and candidate in
a GitHub-profile-like shell where feasible, using the hosted live profile for
the real baseline and GitHub-rendered GFM for the candidate; clearly label the
hosted baseline and local candidate. Inspect light and dark appearance at
narrow and desktop widths. Save actual before/after screenshots for the user
and present them before any release or publication decision.

Exclusions: no sibling portfolio changes, workflows, scripts, remote embeds,
profile settings, push, release, or other public-state change. Replace only
the existing local circuitry asset and revise `README.md`; implementation
writes are not authorized by this planning task. Do not add an epic: this is
one independently acceptable profile outcome. No release or publication is
approved; explicit user acceptance of feature evidence precedes any later
release decision.

## Journeys

J1: A prospective collaborator opens the GitHub profile and quickly sees the
circuitry banner, Miguel's portfolio-aligned identity and headline, expertise,
selected OpenTelemetry contributions, and ways to connect. On a narrow screen
the banner remains shallow and the profile hierarchy remains easy to scan.

J2: A visitor uses keyboard navigation or views the profile with images
blocked. The GFM image link has a meaningful accessible name; essential copy
and all text actions remain present and usable without the image. No remote
asset or script is required.

## Feature acceptance

Feature acceptance is separate from release. The caller assembles one pinned
baseline-to-candidate evidence packet after implementation. Evidence is
Pending until produced; no acceptance, demo, or release is pre-approved.

- Demo and visual judgment (caller, then explicit user product acceptance):
  pinned hosted baseline and GitHub-rendered GFM candidate shown in a
  GitHub-profile-like shell, with real screenshot artifacts at narrow and
  desktop widths in light and dark appearances. Label live versus local
  renders and identify both revisions. Show the screenshots to the user
  before any release decision. No human pair or mob participation is claimed.
- Code/content checks (implementer): inspect changed README and asset; verify
  native Markdown copy, correct portfolio/contact/résumé destinations,
  secondary LinkedIn, concise expertise, and both OpenTelemetry descriptions
  against source. Verify the asset is static, first-party, and contains no
  external references or essential text. Verify passive Markdown/image markup
  has no scripts, remote embeds, badges, or statistics.
- Integration/render checks (implementer): render the candidate with GitHub's
  GFM renderer; confirm expected heading, actions, named image link, and
  descriptions. Inspect image blocked/off state and keyboard focus/name.
  Compare the hosted baseline with the local candidate in the stated shell,
  at mobile/narrow and desktop widths and light and dark appearances; report
  viewport dimensions and screenshot paths. Candidate is not represented as
  live GitHub output.
- End-to-end check (implementer): open the candidate rendering and hosted
  baseline in the same comparison shell, verify first-screen hierarchy at
  both widths and themes, and record actual screenshots and visual findings.
  A failure in the image request must leave copy and actions visible.
- Trust-boundary/security triage: static local SVG and passive Markdown only;
  no access control, sensitive data, external input, third-party dependency,
  or new exposure is intended. Confirm SVG has no scripts, foreign objects,
  external references, or active content and markup adds no remote fetches.
  On that verified scope, `security_review` is not applicable. Re-triage if
  implementation adds external resources or active content.
- Feature decision (user): explicit acceptance of the pinned evidence and
  screenshots is required before any release/push decision. Missing evidence
  or user decision remains Pending. Release is a separate, not-yet-authorized
  decision.

## Phase dependencies

P1: None. One serial trunk slice replaces the README's end-positioned image
with a wide shallow banner near the top and preserves/reorders verified text
and actions. The README and the one existing asset are shared write surfaces
within this slice; land their content change atomically. The plan is a
separate planning-only commit. There are no parallel slices, service
contracts, or cross-repository writes.

## Phases

### P1: Portfolio-hierarchical GitHub profile

- Entry: plan committed at baseline
  `eb6239659106fe54db71f7b71055c3b62b8e2da0`; implementation requires a
  later caller dispatch. Read-only anchors: `README.md`,
  `assets/circuitry-accent.svg`, prior `plans/github-profile-redesign.md`,
  `docs/GLOSSARY.md`, and sibling `Home.tsx`, `Home.css`, `App.css`, and
  `public/circuitry.svg` under
  `/home/eldermael/Repos/eldermael/portfolio-website/`. The sibling is
  evidence only.
- S1 (J1, J2): replace the end-positioned circuitry image with one wide,
  shallow, static branded banner near the top; retain essential content as
  native Markdown. Establish visual hierarchy with the portfolio headline
  and identity, inline portfolio/contact/résumé actions, LinkedIn as a
  secondary action, one concise expertise line, and both OpenTelemetry links
  with concise descriptions grounded in the existing Home source. Preserve
  the known destinations and do not add unsupported claims. Use a named GFM
  image link with a useful accessible name; verify image-off behavior and
  keyboard access. Keep the banner visually subordinate to the content and
  avoid all badges, stats, remote embeds, and scripts. Anchors: `README.md`,
  `assets/circuitry-accent.svg`; copy and motif evidence in the named
  read-only sibling files. Write scope for implementation: `README.md` and
  `assets/circuitry-accent.svg` only. No flag or abstraction is needed.
  Acceptance: checks in Feature acceptance, including pinned comparison,
  screenshots, light/dark and narrow/desktop inspection, image-off, GFM,
  keyboard/name, and SVG passive-content inspection.
  T1: revise the README and adapt the existing local SVG into a wide shallow
  banner; observable result is the described profile hierarchy with working
  text content when the image fails; evidence is the pinned GFM rendering,
  SVG/markup inspection, and comparison screenshots described above; status:
  proposed, not started; ordered commit references: Pending.
- Checkpoint: gather the complete evidence in Feature acceptance at one
  pinned trunk revision, with ordered marked story commits, screenshot paths,
  GFM and image-off results, viewport/theme details, security triage, and any
  remaining review findings. Applicable review is change review of cumulative
  PROFILE-02 commits at the pin. No separate integration contract changes;
  no integration review planned. User product acceptance: Pending. No push or
  release decision is included.

## Glossary and decisions

See [shared glossary](../docs/GLOSSARY.md). Updated the glossary with
**Profile banner** as the canonical term for this story's wide, shallow,
first-screen visual accent; it is not essential content. No ADR is proposed:
this static Markdown/SVG presentation is local and readily reversible, with
no public contract or hard-to-reverse data choice.

## Progress and open questions

- Plan prepared for new story PROFILE-02, not a revision of PROFILE-01.
- Baseline: `eb6239659106fe54db71f7b71055c3b62b8e2da0` (user-provided and
  checked as current `main` at planning start).
- P1/S1/T1: proposed; implementation, GFM rendering, screenshots, security
  triage verification, review, and explicit user acceptance are Pending.
- No feature changes, publication, push, or release are authorized by this
  planning increment. No open question; the concrete direction is user
  confirmed.
