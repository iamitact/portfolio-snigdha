# Deploying this site on GitHub Pages

## Files in this folder

| File | What it is |
|---|---|
| `index.html` | The whole page |
| `style.css` | All styling, including the phone/tablet layouts |
| `script.js` | Mobile menu, scroll reveal, active nav link, footer year |
| `portrait.jpg` | Hero photo (900 px wide, 96 KB) |
| `favicon.svg` | Browser tab icon |

No build step, no framework, no npm. GitHub Pages serves these as-is.

---

## Before you publish — fill these in

Search the files for `[` and `TODO` and replace every one:

1. **Contact block** (`index.html`, section `05 / Contact`) — email, phone, LinkedIn.
   Put the real address in **both** the `href` and the visible text:
   `<a href="mailto:real@address.com">real@address.com</a>`
2. **Availability line** in the hero.
3. **Three project cards** — title, year, tools, the two-sentence write-up, and an
   image. Drop the image in this folder and swap the placeholder:
   ```html
   <div class="card__media"><img src="project-01.jpg" alt="Short description of the project"></div>
   ```
4. **CV download** — save the CV here as `snigdha-cv.pdf` (or change the link in
   the hero to whatever you name it).
5. **`og:url`** in `<head>` — your real site address, so link previews work.
6. Delete every leftover `<span class="ph">…</span>` wrapper once the real text is in;
   it is only there to make placeholders visible.

---

## Publishing (browser only, no git needed)

1. Create a GitHub account if there isn't one. **The username becomes the web
   address**, so pick something like `snigdharoychowdhury` — not a nickname.
2. **New repository** → name it exactly `USERNAME.github.io` (same username,
   lowercase) → **Public** → Create.
3. On the empty repo page: **uploading an existing file** → drag in all the files
   from this folder (the files themselves, not the folder) → **Commit changes**.
4. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder
   `/ (root)` → Save.
5. Wait 1–2 minutes, then open **https://USERNAME.github.io** — done.

Any later edit: upload the changed file again, wait a minute, then hard-refresh
(Ctrl/Cmd + Shift + R) — GitHub caches aggressively.

### If the repo is named something else

A repo named e.g. `portfolio` also works, but the address becomes
`https://USERNAME.github.io/portfolio/`. All links in this site are relative, so
it works either way.

---

## Using git instead

```bash
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/USERNAME/USERNAME.github.io.git
git push -u origin main
```

Then enable Pages in Settings → Pages as above.

---

## Two things worth knowing

- **Free GitHub Pages repos are public.** Anything you commit — the phone number,
  the CV PDF — is readable by anyone and gets indexed by Google. If you would
  rather not have a phone number scraped, list email and LinkedIn only.
- **A custom domain is optional.** Settings → Pages → Custom domain accepts a
  domain you buy separately (~$10–15/year). `USERNAME.github.io` is perfectly
  respectable for a first portfolio.
