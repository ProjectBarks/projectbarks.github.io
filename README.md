# projectbarks.github.io

Deployed output for [brandonbarker.me](https://brandonbarker.me).

> **Don't edit files here directly.** This repo is overwritten on every
> release. Edit the source instead:
>
> 👉 **Source repo:** [ProjectBarks/personal-site](https://github.com/ProjectBarks/personal-site)

## what this is

GitHub Pages user-pages repo. Serves at `https://projectbarks.github.io/`
and redirects to `https://brandonbarker.me/` via the `CNAME` file.

## what gets pushed here

`personal-site` builds a tiny static site (one HTML, one CSS, favicons,
resume PDFs) and pushes the contents of `./build/` here on `master` via
`gh-pages`. The release commit message is `Release vX.Y.Z`.

```text
.
├── CNAME                    ← brandonbarker.me
├── index.html               ← rendered from src/index.pug + data/resume.json
├── style.css
├── images/favicons/         ← full set of favicon sizes
└── downloads/
    ├── brandon_barker_resume_2020.pdf
    └── quadtree_spatialhash.pdf
```

## releasing a new version

From the source repo:

```bash
cd personal-site
npm install
npm run release
```

That builds and pushes a new commit to `master` here. GitHub Pages picks it
up automatically (~30s).
