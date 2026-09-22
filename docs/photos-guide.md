# Photos Guide

The photos page (`/photos`) reads page resources straight out of
`content/photos/`. There's no front-matter array to maintain — add a file,
rebuild, done.

## Adding a photo

Drop an image (jpg/png/webp) into `content/photos/`:

```
content/photos/2026-03-14-ladakh-01.jpg
```

Prefix the filename with a date so newest photos sort first — the gallery
sorts resources by filename, descending.

## Captions

Captions are optional. To add one, match the filename in a `[[resources]]`
block in `content/photos/_index.md`:

```toml
[[resources]]
  src = '2026-03-14-ladakh-01.jpg'
  title = 'Pangong, first light'
```

Photos without a matching block render without a caption; alt text falls
back to a humanized version of the filename.

## Display

Photos render at their original resolution — no thumbnail or resized
variant is generated. The file you drop in is the file the browser
downloads, so export at the size you actually want served (long edge
~2000px is plenty for the grid) before adding it. Clicking a photo opens
that same original on its own, unconstrained by the grid.
