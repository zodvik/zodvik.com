+++
title = 'Designing Image-Rich Articles'
date = 2026-05-05
draft = true
summary = 'A sample article for testing how prose, code, captions, and images should work together on this site.'
readTime = true
tags = ['design', 'publishing']
+++

Text gets most of the attention in a personal site because it is the thing we edit most often. Code gets a close second because technical writing quickly falls apart when snippets are hard to scan. Images need the same level of care. They are not decoration; they are arguments, evidence, pacing, and memory.

![A desk with a laptop, contact sheets, captions, and article layout notes](article-workbench.png#bleed "An image-heavy article needs a rhythm: prose explains, code specifies, images make the idea inspectable.")

The basic rule is simple: an image should earn its size. A small supporting diagram can sit inside the reading column. A screenshot with details should go wide. A hero-like visual can break the column entirely, but only when it gives the reader more information at that scale.

## Figure Scale

Most articles need three image sizes.

| Image role | Best size | Why |
| :-- | :-- | :-- |
| Supporting diagram | Inset | Keeps the reader in the sentence flow. |
| Screenshot or product state | Wide | Preserves detail without forcing zoom. |
| Scene-setting image | Bleed | Creates a chapter break and resets attention. |

This site uses tiny Markdown fragments to pick the treatment:

```md
![Alt text](/images/example.png "Default figure")
![Alt text](/images/example.png#wide "Wide figure")
![Alt text](/images/example.png#bleed "Bleed figure")
![Alt text](/images/example.png#inset#plain "Inset figure without frame")
```

That keeps the writing portable. The Markdown remains readable, the image still has alt text, and the renderer can handle layout decisions consistently.

![A screenshot-style mockup of an article with prose, code, an image, and a caption](layout-mockup.png#wide "Wide figures are for details the reader may need to inspect, such as interface states or dense screenshots.")

## Captions Are Part Of The Argument

A caption should not repeat the alt text. Alt text describes the image for readers who cannot see it. A caption explains why the image is here. The best captions answer one of these questions:

1. What should the reader notice?
2. What changed from the previous state?
3. What constraint does this image reveal?

The same thinking applies to code. The paragraph introduces the intent, the snippet shows the mechanics, and the next paragraph explains the consequence.

```html
<figure class="article-figure img-wide">
  <a class="figure-link" href="/images/article-state.png">
    <img src="/images/article-state.png" alt="Article layout with a wide screenshot">
  </a>
  <figcaption>Wide figures make interface details inspectable without leaving the page.</figcaption>
</figure>
```

The image links to its source, so a reader can open it at full size. That matters for screenshots, charts, maps, and any image where compression or column width hides important detail.

![A minimal diagram showing an image moving through a publishing pipeline](pipeline-diagram.png#inset#plain "A compact diagram belongs inside the reading column when it supports the surrounding paragraph rather than replacing it.")

## The Reading Experience

Good image support is mostly spacing. The figure needs enough room that it feels intentional, but not so much that the article becomes a gallery. Captions should be visually quieter than body copy. Frames and shadows should help separate screenshots from the page, while photographs can keep the same treatment for consistency.

When images, prose, and code share one article, the page should feel calm. The reader should understand where to look, what to inspect, and when to return to the text.
