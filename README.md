# Hyunjun Kim — Academic Homepage

Source for [rla-guswns.github.io](https://rla-guswns.github.io), the personal
academic website of Hyunjun Kim (김현준), Integrated M.S./Ph.D. student in
Intelligence Robotics at Sungkyunkwan University ([RISE LAB](https://rise.skku.edu/)).

## Content

| Path | What lives there |
| --- | --- |
| `_pages/about.md` | Front page: intro and publication list |
| `_pages/cv.md` | CV: education, teaching, publications |
| `_publications/` | One Markdown file per paper |
| `images/publications/` | Representative figure for each paper |
| `_config.yml` | Site title, sidebar profile, social links |
| `_data/navigation.yml` | Header menu |

### Adding a publication

Drop a file in `_publications/` named `YYYY-MM-DD-short-title.md`. The front
page, `/publications/`, and the CV all pick it up automatically.

```yaml
---
title: "Paper title"
collection: publications
category: manuscripts        # manuscripts | conferences | preprints
permalink: /publication/YYYY-MM-DD-short-title
date: YYYY-MM-DD
authors: '<b>Hyunjun Kim</b>, Coauthor Name'   # own name in bold
venue: 'Journal or conference name'
header:
  teaser: publications/figure.png              # relative to images/
paperurl: 'https://...'
projecturl: 'https://...'                      # optional
citation: 'Full citation string.'
---
```

## Local preview

```sh
docker compose up
# http://localhost:4000
```

Note that `_config_docker.yml` overrides `url` to an empty string for local
runs. That makes `base_path` empty, so anything depending on absolute URLs
looks different than it will in production. To check those, build with the
production config:

```sh
docker compose exec jekyll-site jekyll build --config _config.yml -d /tmp/prodout
```

Editing `_config.yml` requires a restart — Jekyll's watcher does not reload it:

```sh
docker compose restart
```

## Deployment

GitHub Pages publishes the `master` branch automatically, because the
repository is named `<username>.github.io`. Pushing is all that is needed.

## Credits

Built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io)
template, itself a fork of the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)
Jekyll theme (© 2016 Michael Rose, MIT License). See `LICENSE`.
