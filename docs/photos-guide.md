# Photos Guide

The photos page (`/photos`) reads page resources from `content/photos/`.

## Add a photo

Put an image (jpg/png/webp) into `content/photos/`. Use the name format
`<city>-<country>-NN.jpg`:

```
content/photos/leh-india-01.jpg
```

The gallery sorts photos by file name, A to Z.

## Layout

The page puts photos in two grids:

- **Landscape**: the photo is wider than it is tall (or square). 3 columns.
- **Portrait**: the photo is taller than it is wide. 4 columns.

Each grid crops tiles to one aspect ratio (3:2 or 2:3). The viewer shows
the full photo without a crop.

## Place, caption, and alt text

All fields are optional. Add a `[[resources]]` block in
`content/photos/_index.md` with the same file name:

```toml
[[resources]]
  src = 'leh-india-01.jpg'
  [resources.params]
    city = 'Leh'
    country = 'India'
    alt = 'Blue lake below brown mountains'
    caption = 'Pangong, first light'
```

- `country` and `city` show on the tile when you hover over it, and as the
  title in the viewer.
- `caption` shows below the photo in the viewer. If it is empty, the
  viewer shows `alt`.
- `alt` is the text for screen readers. If it is empty, Hugo uses the file
  name.

## Image sizes

Hugo makes WebP thumbnails at 480, 800, and 1200 px wide for the grid.
The browser selects the smallest size that stays sharp.

If the original is wider than 2400 px, Hugo makes a 2400 px copy for the
viewer. Export at approximately 2000–2400 px on the long edge to keep the
repository small.

## Viewer

Click a tile to open the viewer. To move between photos, use the arrow
buttons, the left and right arrow keys, or swipe. To close the viewer,
push Escape, click Close, or click outside the photo.
