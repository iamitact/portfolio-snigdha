# Deploying this site on GitHub Pages

## Files in this folder

| File | What it is |
|---|---|
| `index.html` | The whole page |
| `style.css` | All styling, including phone/tablet layouts |
| `script.js` | Mobile menu, scroll reveal, active nav link, footer year |
| `portrait.jpg` | Hero photo |
| `project-elevator.svg` | Diagram for the PLC elevator project |
| `project-safety-device.svg` | Diagram for the wearable safety device |
| `favicon.svg` | Browser tab icon |

No build step, no framework, no npm. GitHub Pages serves these as-is.

Typography: Cormorant Garamond (headings) over DM Sans (body), loaded from Google Fonts.

---

## Still to fill in

Search `index.html` for `[` and `TODO`:

1. **Availability line** in the hero — or delete that whole `<p class="availability">` line.
2. **LinkedIn URL** in the contact block — real URL in both the `href` and the visible text.
3. **CV PDF** — save it in this folder as `snigdha-cv.pdf`, or change the hero link to match your filename.
4. **`og:url`** in `<head>` — the real site address, so link previews work.
5. Delete each `<span class="ph">…</span>` wrapper once the real text is in; it only exists to make placeholders visible.

Adding a third project later: copy one `<article class="card">` block, swap the image, meta line, title, text and tags.

---

## Publishing (browser only, no git needed)

1. Create a GitHub account. **The username becomes the web address**, so pick something like `snigdharoychowdhury` — not a nickname.
2. **New repository** → name it exactly `USERNAME.github.io` (same username, lowercase) → **Public** → Create. Do not tick "Add a README".
3. On the empty repo page click **uploading an existing file** → drag in the **files** from this folder (the files themselves, not the folder) → **Commit changes**.
4. **Settings** → sidebar **Pages** → under "Build and deployment", Source: **Deploy from a branch**, Branch: `main`, folder `/ (root)` → **Save**.
5. Wait 1–10 minutes, then open **https://USERNAME.github.io**.

Later edits: upload the changed file again, commit, wait a minute, then hard-refresh (Ctrl/Cmd + Shift + R).

### If it does not work

| Symptom | Cause |
|---|---|
| 404 | `index.html` is not at the repo root — the folder was uploaded instead of the files |
| Page loads but unstyled | Filename case. `Style.css` and `style.css` are different files on GitHub Pages |
| Images missing | An `.svg`/`.jpg` was not uploaded, or its name differs in case |
| Old version showing | Browser cache — hard-refresh |

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

Then enable Pages as in step 4.

---

## Worth knowing

- **Free GitHub Pages repos are public.** Everything committed here is readable by anyone and indexable by Google. That is why the site lists an email and LinkedIn but no phone number — keep it that way unless you want the number scraped.
- **A custom domain is optional.** Settings → Pages → Custom domain accepts a domain bought separately (~$10–15/year). `USERNAME.github.io` is perfectly respectable for a first portfolio.
