# Review — portfolio

## Nightly review — 2026-07-07

### 1. Refactor / simplify / improve

None new. Verified tonight: source is byte-for-byte unchanged since the last five runs (`index.html` June 23; `styles.css`/`script.js` June 2). The four standing proposals all still hold and are not re-argued here — in priority order: dark-mode FOUC + honour `prefers-color-scheme` via a tiny inline `<head>` script (`script.js:4-5`, ~20 min, best value/minute); restore mobile nav (`styles.css:91` still hides every link below 620px, ~15 min to stop hiding / ~1 hr for a menu); a real ~1200×630 OG image (`og:image` at `index.html:13` still points at the square `apple-touch-icon.png`, ~30 min, folds into the SEO backlog item); and the literal `## YYYY-MM-DD — Project created` heading in `docs/DECISIONS.md:5` (confirmed still present — a 30-second human fix, outside my write scope).

### 2. Step back

Positioning, voice, and structure are right; no case to pause, merge, or abandon. Two carried points, both needing a human decision rather than another night of observation:

- **Cadence is now the whole finding.** This is the *sixth* consecutive nightly run producing an identical section for a page that has not changed in two weeks. That is itself the signal: an unattended nightly review of a portfolio that changes a few times a year is pure waste — it pays every night to re-confirm a stable page and to generate diminishing-value notes like this one. The single highest-value action available is a config change, not site work: switch this job to weekly, or trigger it only when `index.html`/`styles.css`/`script.js` actually change.
- **The open-source promise (`index.html:374`)** stays the only live item with real downside — a public "I'll figure out how to share it" the site can't yet honour, now unresolved across six reviews. It wants a decision, not another observation: release 2–3 repos or soften the wording. Backlog #1, correctly.

## Nightly review — 2026-07-06

### 1. Refactor / simplify / improve

None new. Source is untouched since the June 23 FoosTrainer commit (`index.html`; `styles.css`/`script.js` June 2), so tonight adds nothing to the four standing proposals. I re-confirmed each against the live files and all still hold — not re-argued here; see 2026-07-05 for detail. In priority order: dark-mode FOUC + honour `prefers-color-scheme` (`script.js:4-5`, ~20 min, best value/minute); restore mobile nav (`styles.css:91` hides every link below 620px, ~15 min); a real ~1200×630 OG image (`index.html:13` still points at square `apple-touch-icon.png`, ~30 min, folds into SEO backlog); replace the literal `## YYYY-MM-DD — Project created` heading in `docs/DECISIONS.md` (30-sec human fix, outside my write scope).

### 2. Step back

Positioning is right; no case to pause, merge, or abandon. Two points, both already on record and both needing a human, not another observation:

- **Cadence is now the finding.** This is the *fifth* consecutive nightly run reaching identical conclusions on a page that has not changed in two weeks. An unattended nightly review of a portfolio that changes a few times a year is pure waste — it pays every night to re-confirm a stable page. Switch this job to weekly, or trigger only when `index.html`/`styles.css`/`script.js` actually change. This is the single highest-value action available and it is a config change, not site work.
- **The open-source promise (`index.html:374`)** remains the only live item with downside — a public "I'll figure out how to share it" the site can't yet honour, now sat across five reviews. Decision, not observation: release 2–3 repos or soften the wording. Backlog #1.


## Nightly review — 2026-07-05

### 1. Refactor / simplify / improve

None worth doing that isn't already on record. I re-verified the four carried items against
the live files tonight and all four still stand, unchanged and unregressed (source untouched
since index.html June 23, styles.css/script.js June 2):

- **Dark-mode FOUC + honour `prefers-color-scheme`** — `script.js:4-5` still applies the
  stored theme only after first paint, and there is still no `prefers-color-scheme` fallback,
  so a dark-OS first-time visitor gets a light flash then a light page. One inline `<head>`
  script fixes both. Highest value/minute. ~20 min.
- **Mobile nav** — `styles.css:91` still hides every nav link below 620px, leaving only the
  toggle. ~15 min to stop hiding them, ~1 hr for a proper menu.
- **Real OG image** — `index.html:13` still points `og:image` at the square
  `apple-touch-icon.png`; no canonical or Twitter-card tags. ~30 min once an image exists;
  folds into the SEO backlog item.
- **`docs/DECISIONS.md` placeholder** — still a literal `## YYYY-MM-DD — Project created`
  heading. 30-second human fix (out of my write scope).

### 2. Step back

The site is fine exactly as it stands — right positioning, right voice, no case for pausing,
merging, or abandoning.

- **The open-source promise (`index.html:374`) is still the only item with real downside** —
  a public invitation ("I'll figure out how to share it") the site can't yet honour. It has
  now sat across four reviews. It needs a human decision, not more observation: release 2–3
  projects, or soften the wording to something you're happy leaving up indefinitely. Backlog
  #1, correctly.
- **Cadence, again — and this is now the actionable point.** This is the *fourth* consecutive
  nightly review reaching identical conclusions on an unchanged page. That is the real finding:
  a portfolio that changes a few times a year does not warrant a nightly unattended run. Switch
  this to weekly or on-change (trigger a review only when index.html/styles.css/script.js
  actually change). Until then each night pays to re-confirm the same stable page.


## Nightly review — 2026-07-04

### 1. Refactor / simplify / improve

None worth doing. The source is unchanged since the last two reviews (index.html last
edited June 23; styles.css / script.js June 2), so nothing new has appeared. The four
proposals already on record still stand and are **not repeated here** — in priority order:
the dark-mode FOUC fix folded together with honouring `prefers-color-scheme` for first-time
visitors (highest value/minute), restoring mobile nav (`styles.css:91` still hides every nav
link below 620px), a real ~1200×630 OG image (`index.html:13` still points at the square
`apple-touch-icon.png`), and replacing the literal `## YYYY-MM-DD` heading in
`docs/DECISIONS.md`. I re-verified each against the current files tonight; all four remain
live and none has regressed or been fixed.

### 2. Step back

The site is fine exactly as it stands — no case for pausing, merging, or abandoning. The
positioning, voice, and structure are right and need no rethink.

Two honest flags, both carried, because nothing has changed to retire them:

- **The open-source promise at `index.html:374` is the only item with real downside** (an
  invitation the site can't yet honour). It has now sat unresolved across three reviews. The
  clean fix is a decision either way — release 2–3 projects, or soften the wording to
  something you're happy leaving up indefinitely. This is backlog #1 and belongs at the top.

- **A meta-note on cadence.** This is the third consecutive nightly review of a finished,
  unchanged static site, each necessarily reaching the same conclusions. That is itself a
  signal: a portfolio that changes a few times a year doesn't need nightly automated review.
  Consider dropping this to weekly or on-change only — the run is currently paying to
  re-observe a stable page. (Not something I can change from here; flagging for the morning.)

## Nightly review — 2026-07-03

### 1. Refactor / simplify / improve

The code is unchanged since yesterday's review, so **the four items from the 2026-07-02
section below still stand** and are not repeated here. In priority order they remain: the
dark-mode FOUC fix (highest value/minute), restoring mobile nav, a real OG preview image,
and the DECISIONS.md placeholder date. One genuinely new observation:

- **Honour `prefers-color-scheme` for first-time visitors.** The theme is light by default
  and only flips to dark if the user has previously chosen it (`script.js:4-5`, `styles.css`
  has no `@media (prefers-color-scheme: dark)` block). A visitor whose OS is in dark mode and
  who has never toggled the site gets a bright light page. Fix: on first load, when there's no
  stored `theme`, fall back to `window.matchMedia("(prefers-color-scheme: dark)")`. Best done
  in the same inline `<head>` script proposed for the FOUC fix, so it's one small change, not
  two. Effort: folds into the FOUC item, ~10 min extra.

Nothing else is worth doing. The site is genuinely in good shape.

### 2. Step back

Reviewed one day ago and unchanged, so there is little new to say and that is the honest
answer, not an evasion. The positioning is right, the voice is strong, and the site earns its
place as a low-maintenance, live shop-window. No case for pausing, merging, or abandoning.

The one thing worth a human's judgement (carried over, because it's the only item with real
downside rather than polish): the public open-source promise at `index.html:374` is a cheque
the site can't yet cash. It has now sat for a while. The cleanest resolution is a decision
either way — pick 2–3 projects to actually release, or soften the wording to something you're
comfortable leaving up indefinitely — rather than leaving an open invitation you may not be
ready to answer. This is exactly backlog item #1; it deserves to stay at the top.

## Nightly review — 2026-07-02

### 1. Refactor / simplify / improve

- **Fix the dark-mode flash (FOUC).** `script.js` runs at the bottom of `<body>`, so
  the stored theme is applied only after first paint. A user who chose dark mode sees a
  light flash on every load. Fix: move the ~4 lines that read `localStorage` and set
  `data-theme` into a tiny inline `<script>` in `<head>`, before the stylesheet. Leave
  the rest of `script.js` where it is. Effort: ~15 min.

- **Restore navigation on mobile.** `styles.css:91` hides *every* nav link below 620px
  (`.site-nav a:not(:last-child) { display: none }`), leaving only the theme toggle. On
  phones the site becomes scroll-only with no way to jump to sections. Options: a simple
  hamburger/drawer, or just don't hide the links (they're short and could wrap or shrink).
  Effort: ~1 hr for a minimal menu, ~15 min to simply stop hiding them.

- **Give social shares a real preview image.** `og:image` (index.html:13) points at
  `apple-touch-icon.png`, a small square icon — LinkedIn/Slack/iMessage previews will look
  poor. Add a purpose-built ~1200×630 OG image, plus a `<link rel="canonical">` and Twitter
  card tags. This overlaps the existing SEO backlog item and could be folded into it.
  Effort: ~30 min once an image exists.

- **Tidy the DECISIONS.md placeholder.** `docs/DECISIONS.md` still has a literal
  `## YYYY-MM-DD — Project created` heading. Replace with the real creation date. Trivial.
  (Out of scope for tonight — I'm limited to STATUS/BACKLOG/REVIEW — but worth a human's 30
  seconds.)

None of these are urgent; the site is in good shape. The FOUC fix is the highest
value-per-minute item.

### 2. Step back

The positioning is strong and coherent: a clear voice, a real CV spine, and a well-organised
tour of projects. It does its job — a credible personal site — and does not need rethinking.

Two honest flags:

- **The open-source promise writes a cheque (index.html:374).** "I'm hoping to open-source
  most of these projects" is a public commitment with no follow-through visible yet. Either
  commit (backlog item #1 is the right call — pick 2–3 projects, add repos and licences) or
  soften the wording to something you can stand behind indefinitely. Right now it invites an
  email you may not be ready to answer.

- **"Project-status sync" (backlog #2) is probably over-engineering.** For a hand-maintained
  static page with ~20 cards, automating status pills is more machinery than the problem
  needs — editing the HTML when a project ships is a two-minute job done a few times a year.
  Suggest either dropping this item or reframing it as a lightweight manual checklist
  ("review project statuses quarterly") rather than building a sync.

Otherwise: this project is worth keeping exactly as it is. It's low-maintenance, it's live,
and it earns its place. No case for pausing, merging, or abandoning.
