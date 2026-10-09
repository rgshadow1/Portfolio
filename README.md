# Mohamed Hda: personal site

A static, dependency-free personal site: plain HTML and CSS, black background, white text.

```
index.html          Homepage (About, Projects, Experience & Activities, Contact)
cv/index.html       CV page (served at /cv/)
assets/style.css    All styling
assets/cv.pdf       PLACEHOLDER CV (replace with your real one)
assets/favicon.svg  Simple "MH" icon
404.html            Not-found page
.nojekyll           Tells GitHub Pages to serve files as-is
```

## Run locally

```bash
cd site
python3 -m http.server 8080
# open http://localhost:8080
```

## What to edit

| What | Where |
| --- | --- |
| Name, intro text, About, experience | `index.html` |
| Email and university email | `index.html` and `cv/index.html` (search `hdamohammed1@gmail.com`, `2713854@dundee.ac.uk`) |
| GitHub | search `github.com/rgshadow1` in `index.html` and `cv/index.html` |
| **LinkedIn** | search `YOUR-LINKEDIN-USERNAME` in `index.html` (contact line and footer) and add it to `cv/index.html` |
| Source-code link for the project | `index.html`, uncomment the `<li>` inside the Advanced Breach Checker block |
| Adding another project | copy the whole `<article class="entry">` block in the Projects section |
| **CV PDF** | replace `assets/cv.pdf` with your real CV, keeping the same file name |
| CV page details (placeholders in grey italics) | `cv/index.html`; remove the "template" note (`.cv-note`) once done |

## Deploy on GitHub Pages

1. Create a repository (for example `rgshadow1.github.io` or `portfolio`).
2. Push the contents of this folder to the `main` branch.
3. Repository Settings > Pages > Deploy from branch > `main` / root.
4. For a `.info` domain: buy it from a registrar, then in Settings > Pages enter it under "Custom domain". Add a `CNAME` file in the repo root containing just the domain.
5. At the registrar, add DNS records: four `A` records for the apex (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`) and a `CNAME` for `www` pointing to `rgshadow1.github.io`.
6. Tick "Enforce HTTPS" once the certificate is issued.

The 404 page uses absolute paths (`/assets/...`), which is correct for a custom domain or a `username.github.io` repo. If you deploy to a project-path URL (`username.github.io/portfolio/`), change them to relative paths.
