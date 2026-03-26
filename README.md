# GitHub Pages Migration

This repository root now contains the GitHub Pages-ready migration of the legacy academic site from `oldsite/`.

## Repository Structure

- `_layouts/default.html`: shared Jekyll page wrapper.
- `assets/css/site.css`: shared stylesheet for the migrated pages.
- Root `*.html` pages: preserved legacy filenames, now rendered through the shared Jekyll layout.
- Course directories and downloadable assets: copied over with original filenames wherever practical.
- `MIGRATION_REPORT.md`: migration notes, URL mapping summary, changed files, and unresolved issues.

## Local Preview

Because the migrated root pages use Jekyll front matter, preview with Jekyll rather than a plain static file server.

1. `cd accessibilitytestpage`
2. Run `jekyll serve` if Jekyll is installed globally, or `bundle exec jekyll serve` if you are using Bundler in this repository.
3. Open the local URL printed by Jekyll, usually `http://127.0.0.1:4000/`.

## GitHub Pages Deployment

This repository is already arranged so GitHub Pages can publish directly from the repository root.

1. Commit the repository contents on the `main` branch.
2. Push to the GitHub repository you want to publish.
3. In GitHub Pages settings, publish from the branch root if GitHub asks for a source.
4. No custom GitHub Actions workflow is required for this migration.

## Notes

- `index.html` remains the real homepage.
- A compatibility `home.html` redirect was added to point to `index.html`.
- A compatibility `publication.html` redirect was added to point to `publications.html`.
- The root HTML pages were cleaned up to remove legacy frame/target assumptions and old Utah-hosted internal links where matching local files existed.
