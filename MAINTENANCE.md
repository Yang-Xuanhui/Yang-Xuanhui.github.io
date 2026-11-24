# Homepage maintenance

## Review workflow

Edit source content, preview locally, review the visible page and Git diff, then commit/publish only when ready. Generated `public/` and `resources/` files are not content sources. The original visual version is preserved at commit `8e011c7`.

## Content sources

- `config.toml`: name, position, institution, academic links and the single top menu.
- `content/_index.md`: About text in Markdown.
- `content/publications/_index.md`: ordered publication records; `selected: true` includes a record on the homepage. `title`, `authors` (Markdown supported), `venue`, `year`, and `doi` are rendered separately. Resource fields include `pdf`, `video`, `code`, `project`, `slides`, `demo` and custom `resources`.
- `content/services/_index.md`: Service text in plain Markdown. Use category headings and bullet points, with role or conference names before dates. Keep each reviewing conference/year as a separate entry; retain newest years first within each category. Edit role names and years directly.
- `static/images/` and `static/pdf/`: image and paper files.

## Appearance and preview

Global colors live at the top of `assets/css/custom.css`. Layout and appearance are separate from factual content. Section headings identify the content targeted by the top menu; they are not a second menu. Desktop retains the left profile and top menu; mobile stacks the profile above the main content.

Run `hugo server --bind 127.0.0.1 --port 1313` and open http://127.0.0.1:1313/. Check desktop and mobile before publishing. Pushing to `main` triggers the existing GitHub Pages deployment.

## Pending factual review

- Confirm the institution abbreviation currently written as `CSE, HKSUT`.
- Review publication author lists, venue names, awards and links together after the visual review.
