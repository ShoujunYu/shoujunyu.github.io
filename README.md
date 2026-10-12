# Shoujun Yu — Minimal Academic Homepage

A standalone, single-page academic website, inspired by text-first research homepages. This project uses **no Academic Pages or third-party theme**. It uses Jekyll only to render the publication collection.

## Contents

- `index.html`: About Me, Education, Publications (single page)
- `assets/css/style.css`: all styling, no JavaScript or third-party CSS
- `_publications/`: eight complete paper records, sorted by date on the homepage
- `_config.yml`: minimal Jekyll configuration
- `_layouts/publication.html`: keeps previously shared publication detail URLs working
- `about/`, `cv/`, `publications/`: redirects of the former page URLs to sections of the homepage
- `images/profile.jpg`, `images/my-favicon.png`: **must be copied from the original repository** (not bundled in this package)

## Updating content

To edit your biography/education, edit `index.html`. To add a paper, create another `.md` file in `_publications/` with YAML front matter fields `title`, `date`, `authors`, `venue`, `paperurl`; optional `pdfurl`, `codeurl`, `dataurl` or `dataseturl`. The homepage sorts it automatically by date.

## Publishing

1. **Back up the existing repository first.** Do not delete the remote repository or its Git history.
2. Run `migration/prepare_from_existing_repo.sh` from the enclosing ZIP package, passing the local existing repo checkout path. It produces a **separate** `ready_to_publish/` folder containing this website **plus your original images** and an `original_content_backup/` folder with your other useful personal files.
3. Review the generated folders. Copy only the contents of `ready_to_publish/` into a clean Git working tree, not over the existing Academic Pages files. Remove the old Jekyll layout, `_pages/about.md` (which claims `/`) and theme files, **after you have backed them up**.
4. GitHub → Settings → Pages → Build and deployment → Source: **Deploy from a branch** → Branch: **master**, folder: **/(root)** (unless your repo is intentionally configured differently). GitHub Pages renders Jekyll sites by default when no `.nojekyll` file is present.
5. Push, and visit https://shoujunyu.github.io/ . Check image, Publications and old redirects.

For a safe command-line migration with a separate clone, see `MIGRATION.md` in the outer package.
