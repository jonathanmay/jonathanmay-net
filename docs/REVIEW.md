# Review — portfolio

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
