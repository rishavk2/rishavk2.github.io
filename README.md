# Personal website

Plain HTML + CSS, no build step. Edit `index.html`, commit, push.

## Deploy (GitHub Pages, one time)

1. Create a **public** repo named exactly `<your-github-username>.github.io`.
2. From this folder:
   ```sh
   git init && git add . && git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<username>/<username>.github.io.git
   git push -u origin main
   ```
3. Repo → Settings → Pages → Source: *Deploy from a branch*, `main` / `/ (root)`.
4. Settings → Pages → tick **Enforce HTTPS**.
5. The site is live at `https://<username>.github.io` within a minute or two.

## Updating

- Edit `index.html` → `git commit -am "Update" && git push`. Live within ~1 minute.
- Photo: add `photo.jpg` (square, ~400×400) and swap the `RK` avatar `<div>` for the `<img>` line in the comment above it.
- News: copy an `<li>` in the News section (newest first).
- GitHub/LinkedIn: fill in the username in the commented icon blocks and uncomment them.
- CV: add a **redacted** `cv.pdf` (no phone/home address) and uncomment the CV link.
- Publications: uncomment the Publications section and copy the `<li>` per paper.
- Update the "Last updated" footer.

## Security notes

- No JavaScript, forms, or third-party fonts/scripts; the CSP meta tag blocks anything else from loading.
- Turn on 2FA for your GitHub account — that account is the only way to change the site.
- Don't commit anything private: the repo is public, and so is its history.
