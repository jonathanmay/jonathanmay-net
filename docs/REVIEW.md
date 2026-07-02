# Review — portfolio

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
