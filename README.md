# lennarteing.github.io

Personal academic website, built with [Jekyll](https://jekyllrb.com) and served by GitHub Pages from the `gh-pages` branch.

Based on the [Allan Lab website template](https://www.allanlab.org/aboutwebsite.html) as adapted by
[Simon Giebenhain](https://github.com/SimonGiebenhain/simongiebenhain.github.io). The code is released under the MIT License, the content is not; see `LICENSE`.

## Where things are

| What | Where |
|---|---|
| Name, email, profile links, photo | `_config.yml` → `author`; position line in `_data/i18n.yml` |
| Bio text | `_pages/home.md`, `_pages/home-de.md` |
| Publications | generated: `_data/publist.yml` (do not edit) from the CV's `.bib` + `_data/pub_extras.yml` |
| Research | `_data/projects.yml`, images in `images/projects/` |
| Theses | `_data/theses.yml` |
| CV | `docs/cv.pdf` (English), `docs/lebenslauf.pdf` (German), copied from the cv repo |
| Languages | English page `_pages/home.md` (`/`), German page `_pages/home-de.md` (`/de/`); UI strings in `_data/i18n.yml`; `en`/`de` fields in the data files |
| Styles | `css/main.scss` |

## Updating publications and the CV

The publication list and the CV PDF come from the (private) cv repository. Put its location in a
git-ignored `.env` (`CV_REPO=path/to/cv`), then:

```sh
pip install -r scripts/requirements.txt
task sync-cv        # copies the CV PDF, regenerates _data/publist.yml
```

## Local preview

```sh
task serve        # Docker; then open http://localhost:4000 (German: http://localhost:4000/de/)
```
