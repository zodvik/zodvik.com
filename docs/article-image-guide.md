# Article Image Guide

Use this when writing posts with images. The sample draft at `content/posts/designing-image-rich-articles/index.md` exercises these patterns without being included in production builds.

## Markdown

Default figure:

```md
![Alt text](/images/example.png "Caption text")
```

Wide figure for screenshots or images with detail:

```md
![Alt text](/images/example.png#wide "Caption text")
```

Bleed figure for a large scene-setting image:

```md
![Alt text](/images/example.png#bleed "Caption text")
```

Inset figure for compact diagrams:

```md
![Alt text](/images/example.png#inset "Caption text")
```

Plain figure for images that should not have a frame, background, or shadow:

```md
![Alt text](/images/example.png#inset#plain "Caption text")
```

Left-aligned caption:

```md
![Alt text](/images/example.png#wide#left "Caption text")
```

## Choosing The Size

Use `#inset` for a small diagram that supports the nearby paragraph.

Use the default size for ordinary photos and illustrations that belong inside the reading column.

Use `#wide` for screenshots, charts, maps, and dense images where the reader may need to inspect details.

Use `#bleed` sparingly for a major visual break or scene-setting image.

## Writing Captions

Alt text should describe the image. Captions should explain why the image is in the article.

A good caption answers one of these:

1. What should the reader notice?
2. What changed from the previous state?
3. What constraint does this image reveal?

Images automatically link to the original file and open in a new tab.
