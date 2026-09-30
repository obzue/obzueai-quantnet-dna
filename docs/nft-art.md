# NFT art skill set

Public generators were read. None of them are installed in this repository, and none of their sample layers or prompts are copied. Installing those trees would vendor other people's art assets and a Node canvas pipeline that does not run inside this website.

## What was read

| Repository | Stars (about) | What it does | What the desk kept |
| --- | --- | --- | --- |
| [HashLips/hashlips_art_engine](https://github.com/HashLips/hashlips_art_engine) | 7.2k | Layer folders, canvas compositing, rarity suffixes `_r` and `_sr` | Ordered visual rules and a single seed. No PNG trait folders. |
| [HashLips/generative-art-node](https://github.com/HashLips/generative-art-node) | 2.1k | Earlier canvas generator. Points at the art engine. | Same idea, not the code. |
| [NotLuksus/nft-art-generator](https://github.com/NotLuksus/nft-art-generator) | 1.6k | Weighted traits, duplicate removal, OpenSea-style metadata | A stored prompt, theme, style, and seed. Not their CLI. |
| [hashlips-lab/hashlips-lab](https://github.com/hashlips-lab/hashlips-lab/tree/main/packages/art-engine) art-engine | lab package | Plugin split: inputs, generators, renderers, exporters | One in-browser painter, plus an optional image render. |

Smaller forks of the HashLips engine (for example layer copies with no extra idea) were not added. Cloning them would not change the desk.

## How a plate is made

1. Pick a theme. Each theme is a five-color palette and a short note.
2. Pick a style. Styles are drawing procedures: layered portrait, field, trait card, ink, pixel, glass, poster, oil, brutal plate, crest.
3. A seed (31-bit) drives the random choices. The same seed, theme, and style redraw the same canvas.
4. Launchpad stores theme, style, seed, and an optional https image link on the listing.
5. Render image is a separate button. It is capped at six rendered images per account per hour. If the image account has no credits, the sketch still works.

The picture is a desk asset. It is not a mint, not a token URI on a public chain, and not a claim on the collection floors shown from the marketplace feed.
