# Presentation Repository Structure

This repository hosts slide decks meant to be published on GitHub Pages. Each presentation is stored in its own folder under `slides/`.

```
slides/
  <presentation-id>/
    index.md          # Slide content in Markdown
    images/           # Images specific to this presentation
    meta.yaml         # Metadata about the presentation
assets/
  images/             # Images shared across presentations
  meta.yaml           # Descriptions of shared assets
```

## Folder naming
Use `YYYY-MM-DD-short-title` for each presentation folder so that events are sorted chronologically.

## Shared assets
Place reusable images in `assets/images/`. Update `assets/meta.yaml` with a short description so that automated tools can understand the file contents.

## GitHub Pages
This repository is intended to be published via GitHub Pages. Point your static site generator to the `slides/` directory to build each presentation into an HTML slide deck.
