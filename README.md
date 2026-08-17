# GST Pragyan — website

Three static pages. No framework, no build step, no dependencies. 228 KB in total.

    index.html        who it's for, what the charts cover, the desktop tool, contact
    compliance.html   11 chart sections + 3 calculators, including the full late fee and
                      interest history since 01.07.2017 and the notice/order limitation dates
    privacy.html      privacy policy
    style.css         one stylesheet for all three
    assets/           logo, wordmark and social preview (109 KB)
    robots.txt        allows indexing
    .nojekyll         tells GitHub Pages not to run Jekyll over the files

## Preview locally

    python3 -m http.server 8000     # then open http://localhost:8000

## Editing

- **Email** — search for `pragyan.gst@gmail.com` in all three pages.
- **Download link** — `index.html`, the section with `id="download"`. Replace the two
  buttons with a real link when the app is published.
- **Colours** — the `:root` block at the top of `style.css`.
- **Statutory figures** — `compliance.html`. The hero carries a review date; change it
  whenever you check the figures, and change the "Last updated" line in `privacy.html`
  whenever that policy changes.
- **Limitation dates** — the `YEARS` object in the script at the foot of
  `compliance.html` drives the third calculator. Each year has the annual return due date
  and the s.73 / s.74 notice and order dates. Add a year by copying an entry.

## What to review, and when

The charts are only as good as their last review. Two things change often:

- **Due dates** are extended by notification, sometimes at a few days' notice.
- **Limitation dates for FY 2018-19 and 2019-20** rest on Notification No. 56/2023-CT,
  which is under challenge in several High Courts. If it is struck down those two rows
  change, and the page says so — keep that caveat until the position settles.

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
