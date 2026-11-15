+++
title = 'Themes'
weight = 50
+++

The `semantic.css` stylesheet includes five built-in themes: **blue** (the default),
**green**, **violet**, **red**, and **orange**. Each theme overrides only the
primary color, `--p`, with values for light and dark mode. Text, headings,
links, backgrounds, surfaces, and borders use the same shared formulas and
derive their colors from that primary. Layout, spacing, and corner radii stay
consistent across themes.

{{< theme-preview >}}

<p><a href="#usage">Example text link</a></p>
<button type="button" class="outline">Outline</button>
<button type="button">Primary</button>

<form>
  <hgroup>
    <h3>My form</h3>
    <p>Example form.</p>
  </hgroup>
  <label for="theme-name">Name</label>
  <input id="theme-name" name="name" type="text" placeholder="Your name">
  <label for="theme-choice">Choice</label>
  <select id="theme-choice" name="choice">
    <option>First option</option>
    <option>Second option</option>
  </select>
</form>

## Usage

Load `semantic.css` and set `data-theme` on the root `<html>` element:

```html
<!doctype html>
<html lang="en" data-theme="green">
  <head>
    <link rel="stylesheet" href="semantic.css">
  </head>
  <body>
    <!-- Your content -->
  </body>
</html>
```

Use `data-theme="blue"` or omit the attribute to use the default palette.
An unrecognized value also falls back to blue. All five themes are included
in the same stylesheet.

Place the attribute on `<html>`, rather than `<body>`, so the root variables are
available throughout the document. Use the standard custom-data attribute
`data-theme` instead of a custom `theme` attribute.

## Color tokens

The color definitions live in `theme.css`. A theme needs only one override:

```css
:root[data-theme="green"] {
  --p: light-dark(#086d4f, #4de6ac);
}
```

The shared tokens are `--f` for text, `--fs` for secondary text, `--h` for
headings, `--a` for links, `--b` for the page background, `--bs` for subtle
surfaces, and `--d` for borders. Changing `--p` updates these derived colors
without duplicating the rest of the palette.
Text and headings share one foreground color, and links use the primary color.
Only the foreground and page background need color mixes; the other tokens
reuse those colors or add transparency.

## Hugo

Select the theme for a page in its frontmatter:

```yaml
---
title: Example page
theme: green
---
```

`baseof.html` adds `data-theme="green"` to `<html>`, so the entire page uses
the selected theme from the first render. Pages without a theme use the site
parameter, or blue if no site parameter is set:

```toml
[params]
theme = 'blue'
```

A section can also supply the theme through Hugo's `cascade`. The top-level Hugo
setting `theme = 'semantic'` selects the Hugo theme itself.

## Light and dark modes

Palette selection is independent of light and dark mode. Each palette uses
`light-dark()` colors and follows the system preference through
`color-scheme: light dark`.

To force a mode, set `color-scheme` on the same root element:

```html
<html lang="en" data-theme="violet" style="color-scheme: dark">
```

To change the palette from JavaScript:

```js
document.documentElement.dataset.theme = "green";
```

All five themes are built in, so changing the attribute switches palettes
immediately using the same stylesheet.
