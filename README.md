# jonathanmay.net

Personal portfolio site for Jonathan May — a brief CV and a tour of the things
I've built. Static site, no build step.

## Stack

Plain HTML, CSS, and a little vanilla JavaScript (theme toggle + scroll
reveal). Served by Nginx on [Fly.io](https://fly.io).

- `index.html` — the main page (CV + projects)
- `manual.html` — "A User Manual to Me"
- `styles.css` — styles (light by default, dark via the toggle)
- `script.js` — theme toggle and scroll reveal
- `portrait.jpg`, `favicon*`, `apple-touch-icon.png` — imagery
- `Dockerfile`, `nginx.conf`, `fly.toml` — deployment

## Local preview

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

## Deploy

```sh
fly deploy
```
