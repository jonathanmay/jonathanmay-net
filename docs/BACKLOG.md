# Backlog — portfolio

> What's next, most important first. The control plane picks the top unchecked item when you dispatch without an explicit task.

- [ ] Stop shipping `docs/` in the deployed image — `.dockerignore`'s `*.md` only matches the repo root, so `docs/REVIEW.md`, `docs/STATUS.md`, `docs/BACKLOG.md` and `docs/DECISIONS.md` are copied into nginx and served publicly (change to `**/*.md` or add `docs`)
- [ ] Make the nav usable on mobile (`styles.css:91-92` hides every nav link below 620px, so the new User Manual page has no route in from `index.html` on a phone)
- [ ] Decide and document an open-source release plan for the listed projects (index.html:374 promises it)
- [ ] Add a project-status sync for the in-development projects shown (Iris, Hubbub Deals, Homewise, MeetMe)
- [ ] Site plumbing: schema.org structured data, sitemap + robots.txt, a real 1200×630 OG image, and lightweight privacy-friendly analytics
