# Semantic CSS

A drop-in, beautiful, hand-crafted stylesheet for semantic HTML.

## Build

The Pages workflow generates the PNG social card from its SVG source after building the site.
For a local production build, install `rsvg-convert` and DejaVu Sans, then run:

```sh
hugo build --minify
rsvg-convert public/social-card.svg --output public/social-card.png
```

Keep control and button styles in `19-forms.css`, including contextual and busy
states. Navigation links belong in `09-nav.css`; text links belong in
`03-typography.css`. Shared keyframes and reduced-motion settings live in
`animations.css`. Component files apply those animations where needed.

## License

Licensed under the [GNU General Public License](LICENSE), version 3 or any later version.

Tailwind CSS Preflight retains its original [MIT license](licenses/preflight.txt).

The htmz extensions retain their original [MIT license](licenses/htmz.txt).
