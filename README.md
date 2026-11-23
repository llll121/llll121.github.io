# llll121.github.io

Personal academic website of Jinbo Liu, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll template and hosted on GitHub Pages at <https://llll121.github.io>.

## Where to edit

| What | File |
| --- | --- |
| Bio, photo caption | `_pages/about.md`, photo at `assets/img/prof_pic.jpg` |
| Publications | `_bibliography/papers.bib` (`selected = {true}` puts a paper on the home page; thumbnails go in `assets/img/publication_preview/`) |
| News | one Markdown file per item in `_news/` |
| CV page and PDF | `_data/cv.yml` (the "Render a CV" GitHub Action rebuilds the PDF when this file changes) |
| Social links | `_data/socials.yml` |
| Site settings | `_config.yml` |

Pushing to `main` runs the "Deploy site" GitHub Action, which builds the site and publishes it to the `gh-pages` branch.

## Local preview (Windows)

Ruby 3.3 with DevKit is installed at `C:\Ruby33-x64`. From this folder:

```bash
bundle install
bundle exec jekyll serve --config _config.yml,../_config_local.yml
```

`../_config_local.yml` turns off ImageMagick (not installed locally). The site is then at <http://localhost:4000>.
