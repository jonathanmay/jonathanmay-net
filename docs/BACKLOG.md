# Backlog — portfolio

> What's next, most important first. The control plane picks the top unchecked item when you dispatch without an explicit task.

- [ ] Stop shipping `docs/` in the deployed image — `.dockerignore`'s `*.md` only matches the repo root, so `docs/REVIEW.md`, `docs/STATUS.md`, `docs/BACKLOG.md` and `docs/DECISIONS.md` are copied into nginx and served publicly (change to `**/*.md` or add `docs`)
- [ ] Decide and document an open-source release plan for the listed projects (index.html:375 promises it)
- [ ] Refresh the project cards against current reality — status pills for the in-development entries (Hubbub Deals, Homewise, MeetMe), and Iris's card copy, which still reads "AI intelligence layer / strategic prototype" rather than the CRM it is now
- [ ] Site plumbing: schema.org structured data, sitemap + robots.txt, a real 1200×630 OG image, and lightweight privacy-friendly analytics
