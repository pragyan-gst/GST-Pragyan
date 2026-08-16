# Pragyan — website

Three static pages. No framework, no build step, no dependencies.

    index.html       the app, what it does, what it will not do, contact
    compliance.html  GST due dates, late fee, interest, ITC time limit + calculator
    privacy.html     privacy policy
    style.css        one stylesheet for all three
    robots.txt       allows indexing
    .nojekyll        tells GitHub Pages not to run Jekyll over the files

## To preview locally

    python3 -m http.server 8000

then open http://localhost:8000

## To edit

- **Email address** — appears in `index.html`, `compliance.html` and `privacy.html`.
  Search for `pragyan.gst@gmail.com`.
- **Download link** — in `index.html`, the section with `id="download"`. Replace the
  disabled button with a real link when the app is published.
- **Colours** — the `:root` block at the top of `style.css`.
- **Privacy policy date** — near the top of `privacy.html`, look for `Last updated`.

## Hosting: GitHub Pages

1. Create a public repository, e.g. `pragyan-site`.
2. Upload these files to the root of the `main` branch.
3. Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)` → Save.
4. Live in a minute or two at `https://<username>.github.io/pragyan-site/`.

For a custom domain: Settings → Pages → Custom domain, then at your registrar add a
CNAME record pointing to `<username>.github.io`. Tick *Enforce HTTPS* once the
certificate is issued. GitHub creates a `CNAME` file in the repo — leave it there.
