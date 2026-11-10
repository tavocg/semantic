# Semantic CSS

A drop-in, beautiful, hand-crafted stylesheet for semantic HTML.

## Build

The Pages workflow generates the PNG social card from its SVG source after building the site.
For a local production build, install `rsvg-convert` and DejaVu Sans, then run:

```sh
hugo build --minify
rsvg-convert public/social-card.svg --output public/social-card.png
```

## License

Licensed under the [GNU General Public License](LICENSE), version 3 or any later version.

Tailwind CSS Preflight retains its original [MIT license](licenses/preflight.txt).
