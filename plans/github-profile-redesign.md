# PROFILE-01 Goal

## Context and goal

The GitHub profile README currently opens with badges and a Rust-structured
bio, followed by a long skills inventory. Redesign it to express the portfolio
positioning used on eldermael.io: AI and systems engineering, useful and
dependable systems, selected verified work, and clear ways to explore and
contact Miguel. The intended result is a concise, accessible, native Markdown
profile README with one optional static circuitry visual accent.

The live portfolio's rendered public content is the source of truth for copy
and links. Its HTML currently confirms the title “Miguel Enriquez | AI &
Systems Engineering,” but is a JavaScript shell; the local portfolio checkout
is two commits ahead of `origin/master` at `5ee4b86`. Do not assume local-only
content is deployed. Reconcile proposed copy and links against the rendered
live pages immediately before finalizing publication.

Exclusions: no portfolio-site changes, workflows, CSS/JavaScript, animation,
visual replication of the website, extra graphics, or permission to publish,
change GitHub profile settings, or push. Preserve the pre-existing unstaged
Pulumi badge edit and untracked `.junie/` and `.pi/` user-owned files. Before
README implementation, resolve that edit with its owner; do not overwrite or
silently incorporate it. Explicitly review useful existing links and the
resume URL rather than silently dropping them. Keep unrelated files untouched.

Success: a visitor can understand Miguel's role and focus and reach the
portfolio and a contact path without loading images; selected claims and
links are verified; the Markdown remains readable at narrow and desktop
widths and in light and dark GitHub themes; the optional illustration carries
no essential copy and does not control layout or access to information.

## Journeys

J1: A prospective collaborator opens the profile README, understands Miguel's
AI and systems engineering focus and selected work, then reaches the portfolio
or contact channel. If images fail or are disabled, all essential content and
paths remain available as native text and links.

J2: A returning visitor seeks a useful profile link or resume. The revised
README retains relevant paths after an explicit inventory of the current
LinkedIn, portfolio, Twitter/X, Dev.to, TikTok, email, resume, and other
useful links; any removed or changed destination has a recorded rationale.
Dead or stale destinations are corrected or excluded only after verification.

J3: A visitor sees the optional circuitry accent in GitHub's rendered README.
At narrow and desktop widths, in light and dark themes, the image remains
nonessential; if unavailable, it does not cause layout dependence or obscure
content. Meaningful artwork has useful alternative text; decorative artwork
uses empty alternative text.

## Phase dependencies

P1: None; creates the content-only README redesign and verifies copy, claims,
and paths against rendered live portfolio content. P2 depends on P1's content
structure and rendered baseline; it adds only the static accent after J1 and
J2 succeed without an image. P2 may not begin until the caller accepts P1.
The README and plan are shared write surfaces, so use serial trunk commits.
P2 introduces a repository-local image asset and a README reference; these
must land atomically. No service or cross-project contract is changed.

## Phases

### P1: Concise portfolio-led native Markdown content

- Entry: actual trunk base was `683bf5481ecf65f860367e9f6c19ac608940ca4b`
  (`main`), not the plan's earlier `fd4f758` pre-plan README baseline. The
  owner explicitly authorized superseding the sole unstaged Pulumi badge edit
  with this redesign; it was not separately committed. Untracked `.junie/` and
  `.pi/` were left untouched and unstaged. Rendered live pages were inspected
  with headless Chrome immediately before implementation. The sibling source
  at `5ee4b86a50451ba5d26a654d4767f171396e0821` was read-only context only.
- S1 (J1, J2): deliver a self-contained README content redesign in native
  Markdown. Lead with identity and concise positioning; summarize AI and
  software, infrastructure and platforms, and data engineering; select only
  verified experience or contributions; provide visible portfolio and
  contact paths. Condense redundant badges, skill tables, and the Rust bio.
  Inventory old links, confirm relevant destinations and explicitly record
  their keep, replace, or remove disposition, including whether the existing
  resume URL remains useful and valid. Keep claims bounded by the live site's
  rendered content and verified public records; do not copy local-only site
  changes as published facts. Preserve unrelated user changes while editing.
  Anchors: `README.md`; portfolio evidence from read-only
  `portfolio-website/src/components/Home.tsx`, `About.tsx`, `Social.tsx`,
  `routes.ts`, and `public/circuitry.svg`. Write scope: README and this plan
  only. No flag or abstraction is needed. Acceptance checks: essential copy
  and portfolio/contact links render as ordinary Markdown without images;
  links resolve to intended destinations; selected claims are supportable;
  removed legacy links and resume disposition are documented; inspect
  GitHub-rendered narrow and desktop previews in light and dark themes; ensure
  no layout relies on third-party badges or image loading.
- S1 implementation evidence (text-only; P2 not started):
  - Base: `683bf5481ecf65f860367e9f6c19ac608940ca4b`. Live Home, About,
    Contact (`/contact-me`), and Social (`/social`) were rendered using
    headless Chrome. Live Home says “Miguel Enriquez · AI & systems
    engineering,” describes useful, dependable systems, and names AI &
    software, infrastructure & platforms, and data engineering. Live Home and
    About substantiate the selected OpenTelemetry Helm chart webhook fix and
    ClickHouse exporter DDL documentation; both PR pages responded HTTP 200.
    The deployed Home also links to Portfolio and LinkedIn. Contact renders a
    contact form at `/contact-me`.
  - Copy and claim inventory: README uses the rendered live positioning and
    three expertise areas. It selects only the two live-listed OpenTelemetry
    PRs; it does not carry forward unverified job-duration or broad skills
    claims. Portfolio, contact, LinkedIn, and resume are retained. Portfolio,
    contact, and resume responded HTTP 200; resume returned `application/pdf`.
    LinkedIn is linked from the deployed Home, but automated curl returned
    999 (access blocked), so it was not independently status-verified.
  - Legacy link dispositions: portfolio, LinkedIn, and resume kept. Old email
    badge replaced with the deployed contact-form path. Twitter URL redirects
    to X (HTTP 200) but omitted to keep the profile focused; Dev.to (HTTP 200)
    is not linked by the deployed site's rendered profile pages and omitted.
    TikTok (HTTP 200) is listed on deployed Social but omitted as secondary;
    the old TikTok tech-tips assertion is also omitted because live rendered
    copy does not substantiate it. Badge images, animated images, skill tables,
    Rust code bio, and third-party GitHub analytics removed; no image is needed
    for content or navigation.
  - Rendering and responsive evidence: GitHub's unauthenticated GFM Markdown
    API rendered the proposed README successfully as headings, paragraphs,
    bullets, and anchors, with no tables, images, or code blocks. All README
    absolute links were checked; the two PRs and four retained destinations
    resolve as recorded above. The API-rendered HTML was viewed in Chromium
    at 375px and 1440px with light and dark preview backgrounds; content
    reflowed without horizontal overflow or image dependencies. These local
    previews do not apply GitHub's full profile-page chrome or exact CSS.
    Hosted GitHub profile previews were not produced, and GitHub themes are
    largely user-agent/browser controlled. No public state was changed or
    pushed.
  - Local portfolio source consulted read-only at
    `5ee4b86a50451ba5d26a654d4767f171396e0821`: `src/components/Home.tsx`,
    `src/components/About.tsx`, `src/components/Social.tsx`, and
    `src/components/routes.ts`. The checkout is three commits ahead of
    `origin/master` (checked during implementation) and is background only; no
    local-only assertions were used as live evidence.
  - User-owned change resolution: owner approved superseding the unstaged
    Pulumi badge image edit as part of README replacement; no independent
    Pulumi change was staged or committed. `.junie/` and `.pi/` remain
    untouched and unstaged.
  - Change review and caller acceptance: Pending; P2 remains blocked until
    caller accepts P1. No publication or push is authorized.

### P2: Optional static circuitry accent

- Entry: P1 has landed and been accepted; P1's text-only rendering passes
  J1/J2; exact rendered appearance and image references are rechecked.
  The caller has resolved the unrelated README Pulumi edit before any README
  edit begins.
- S2 (J3): add one static circuitry accent, preferably a repository-local
  asset derived from the portfolio's existing `public/circuitry.svg` only
  after checking that it is suitable to reuse; otherwise create no new
  artwork without approval. Use native Markdown image syntax and no styling,
  scripting, animation, external image service, or second graphic. Keep it
  away from essential copy and make its alt text reflect whether it is
  decorative or informative. Anchor: README image reference and the approved
  local asset path (settle the path during implementation; no path is
  reserved yet). Write scope: one local asset, README, and plan update; commit
  them atomically. Acceptance checks: preview at narrow and desktop widths in
  light and dark GitHub themes; check contrast and crop/readability; confirm
  meaningful alt handling or empty alt for decoration; disable or fail the
  image and confirm all J1/J2 copy, links, and layout remain usable.
- Checkpoint: record asset provenance and review, exact rendered previews,
  alt-text and image-off results, base and story commit SHAs, and
  `change_review` findings for the marked commit at a pinned trunk SHA. Review
  scope includes
  Markdown rendering, accessibility, contrast, and independence from the
  artwork. Caller decision after evidence: Pending. No permission to publish
  or push is implied.

## Glossary and decisions

See [shared glossary](../docs/GLOSSARY.md). No ADR is proposed: the chosen
native Markdown and optional static image are local, reversible presentation
details, with no lasting public contract or hard-to-reverse data choice.

## Progress and open questions

- P1/S1 content implementation is complete at the recorded actual trunk base;
  record the landed commit SHA after commit. Owner approval resolved the
  Pulumi edit conflict. The plan records live rendering, claim/link evidence,
  and known rendering-preview gaps.

- P2 is blocked on P1 completion and acceptance. Asset reuse, final asset
  path, whether the circuitry is decorative or meaningful, and rendered
  suitability remain to be established; do not assume permission to add an
  asset before review.
- Change review and publication decision: Pending. No push or public state
  change was made.
