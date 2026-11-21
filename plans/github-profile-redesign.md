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

- Entry: checkout is `main` at `fd4f758`; verify this pin and inspect the
  README and working tree. The pre-existing Pulumi badge edit and untracked
  `.junie/` and `.pi/` are caller-owned; the writer may not alter or stage
  them. Before implementation, obtain resolution from the owner of the
  pre-existing README edit. Reconcile exact current portfolio copy and links
  against rendered live pages, not just the local sibling checkout. Review
  the local portfolio evidence at `5ee4b86` only as read-only background.
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
- Checkpoint: capture the exact README diff and link/claim inventory, the
  rendered-live-site evidence and pinned portfolio source/revision consulted,
  and the `main` base SHA and story commit SHA. Run Markdown/link checks and
  review the rendered previews. Request `change_review` for the marked story
  commit at its pinned trunk SHA and the README delta; include content accuracy,
  link dispositions, image independence, and the preserved user-owned changes.
  Record actual outcomes; checks not run are Pending. Caller decision after
  evidence: Pending. Do not start P2 without caller acceptance.

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

- Planning complete; no profile implementation is authorized by this plan.
- P1 is ready after the owner resolves the pre-existing README edit and the
  live rendered portfolio content and target links are reconciled. Exact
  wording, selected contribution, link dispositions, and resume validity need
  that evidence and review.
- P2 is blocked on P1 completion and acceptance. Asset reuse, final asset
  path, whether the circuitry is decorative or meaningful, and rendered
  suitability remain to be established; do not assume permission to add an
  asset before review.
- Commit SHAs, link-check results, rendered previews, reviews, caller decisions,
  and publication decision: Pending.
