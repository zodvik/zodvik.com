# zodvik.com

A minimal Hugo site for technical writing. `assets/css/reset.css` normalizes browser behavior; `assets/css/base.css` adds 18px system text, comfortable line spacing, a centered column, and basic navigation and article spacing. The column is at most 44rem wide including 1.25rem of padding on each side. Both files are bundled into one stylesheet. No theme submodule, JavaScript framework, package manager, or font service is needed.

## Local development

Use **Hugo extended 0.158.0 or later** (verified with 0.165.0).

```sh
hugo server --disableFastRender
```

To preview draft posts, including the image demonstration:

```sh
hugo server --buildDrafts --disableFastRender
```

Open `/posts/designing-image-rich-articles/` in the draft preview. That article stays out of production builds.

## Production

```sh
hugo --gc --minify --panicOnWarning
```

Deploy the generated `public/` directory to a static host. Enable Brotli or gzip on the host and cache the fingerprinted CSS and processed image URLs with a long lifetime. Keep HTML on a short cache lifetime so new posts appear promptly.

The default theme requests no JavaScript, web fonts, or third-party assets. It uses a single minified, fingerprinted stylesheet. Google Analytics is **disabled by default** for speed; the existing measurement ID is retained in `hugo.toml`. Set `params.analytics = true` to load it in production builds.

## Writing

```sh
hugo new content posts/my-post/index.md
```

Keep images alongside `index.md` and use ordinary Markdown. See the [article image guide](docs/article-image-guide.md) for responsive images and captions.

Fenced code blocks render as plain code. Articles include reading time and a native, collapsible contents list. Heading IDs support direct links. Images retain responsive WebP processing, lazy loading, dimensions, captions, and links to their originals. Image layout flags are preserved in the markup but have no visual effect until styling is added.

Set `toc = false`, `readTime = false`, or `hidePagination = true` in an article's front matter to override those defaults. Edit the author information, navigation, and other site defaults in `hugo.toml`; add projects in `content/projects/_index.md`.
