# GST Pragyan — website

Three static pages. No framework, no build step, no dependencies.

    index.html        the app, what it does, what it will not do, contact
    compliance.html   twelve GST charts + a late fee & interest calculator
    privacy.html      privacy policy
    style.css         one stylesheet for all three
    assets/           logo, wordmark and social preview (120 KB in total)
    robots.txt        allows indexing
    .nojekyll         tells GitHub Pages not to run Jekyll over the files

## Preview locally

    python3 -m http.server 8000     # then open http://localhost:8000

## Editing

- **Email** — search for `pragyan.gst@gmail.com` in all three pages.
- **Download link** — `index.html`, the section with `id="download"`. Replace the
  disabled button with a real link when the app is published.
- **Colours** — the `:root` block at the top of `style.css`.
- **Dates** — `privacy.html` carries a "Last updated" line. Add one to
  `compliance.html` too whenever you review the statutory figures.

## Logo assets

Generated from the supplied artwork with the white background flood-filled away from the
EDGES only, so the white eye and bars inside the mark stay white. Knocking out every white
pixel makes them transparent and the mark falls apart on the navy hero.

    mark.png            300px  the P mark, transparent
    mark-64.png          64px  favicon
    wordmark.png        860px  header, on light backgrounds
    wordmark-light.png  860px  footer, navy letters recoloured white
    lockup.png          700px  stacked mark + wordmark
    og.jpg        1200x630px   social preview

## Hosting: GitHub Pages

1. Create a public repository, e.g. `pragyan-site`.
2. Upload these files to the root of the `main` branch.
3. Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)` → Save.
4. Live in a minute or two at `https://<username>.github.io/pragyan-site/`.

Custom domain: Settings → Pages → Custom domain, then at your registrar add a CNAME
record pointing to `<username>.github.io`. Tick *Enforce HTTPS* once the certificate is
issued.
