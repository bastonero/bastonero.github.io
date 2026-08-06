# bastonero.github.io

Source of my personal academic website: <https://bastonero.github.io/>

Built with [Jekyll](https://jekyllrb.com/) on top of the
[academicpages](https://github.com/academicpages/academicpages.github.io) template,
and deployed automatically by GitHub Pages on every push to `master`.

## How the content is organized

| Folder | Shown at | What goes there |
| --- | --- | --- |
| `_pages/` | — | The pages themselves (home, publications, software, talks, teaching, outreach, CV) |
| `_publications/` | `/publications/` | One file per paper. `category` must be one of `manuscripts`, `preprints`, `conferences` (see `publication_category` in `_config.yml`) |
| `_software/` | `/software/` | One file per code. `role` must be one of `main`, `maintainer`, `contributor`; the numeric filename prefix sets the display order |
| `_talks/` | `/talks/` | Talks and posters. `type: "Poster"` sends the entry to the *Posters* section, anything else to *Talks* |
| `_teaching/` | `/teaching/` | Lectures, teaching assistantships, thesis supervision |
| `_outreach/` | `/outreach/` | Lectures given at schools and workshops |
| `_data/cv.json` | `/cv-json/` | JSON-Resume version of the CV (alternative rendering of `/cv/`, not linked in the menu) |
| `images/`, `files/` | — | Static assets; drop a CV PDF in `files/` and set `cv_pdf` in `_config.yml` to show a download button |

Adding an entry is just a matter of copying an existing file in the relevant folder and
editing its front matter — no other file needs to be touched.

## Running the site locally

```bash
bundle install
bundle exec jekyll serve -l -H localhost
```

then open <http://localhost:4000>. Alternatively, `docker compose up` uses the provided
`Dockerfile` and does not require a local Ruby installation.
