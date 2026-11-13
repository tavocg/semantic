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

Component spacing uses `--space` (default: `1rem`) from `01-theme.css`.
Margins, padding, and gaps use this unit or multiples and fractions of it;
override `--space` to adjust the theme's spacing throughout.

## Color themes

`semantic.css` includes five built-in palettes: `blue` (the default), `green`,
`violet`, `red`, and `orange`. Set `data-theme` on `<html>` to choose one:

```html
<html lang="en" data-theme="green">
  <head>
    <link rel="stylesheet" href="semantic.css">
  </head>
  <body>...</body>
</html>
```

Each palette changes the background, text, and accent colors. Derived surfaces,
including the sidebar, follow the palette. Each theme follows the system's light
or dark preference through
`color-scheme: light dark`. Omit the attribute to use the default palette.
Use `<html>` so the theme variables apply to the whole document.

With Hugo, set `theme: green` in a page's frontmatter to choose its palette.
Use `params.theme` in the site configuration for a site-wide default.
The base template writes the selected value to `<html data-theme="…">`;
page frontmatter takes precedence over the site parameter. All palettes use
the same stylesheet and can be previewed with the selector in Themes.

## License

Licensed under the [GNU General Public License](LICENSE), version 3 or any later version.

Tailwind CSS Preflight retains its original [MIT license](licenses/preflight.txt).

The htmz extensions retain their original [MIT license](licenses/htmz.txt).
