+++
title = 'Themes'
weight = 50
+++

Semantic includes six themes: **blue** (the default), **cyan**, **green**,
**violet**, **red**, and **orange**. Each changes the page background, text,
accent, and derived surfaces such as the sidebar. Spacing and validation colors
stay consistent across themes.

{{< theme-preview >}}

<p><a href="#usage">Example text link</a></p>
<button type="button">Primary action</button>
<button type="button" class="outline">Secondary action</button>

<form>
  <label for="theme-name">Name</label>
  <input id="theme-name" name="name" type="text" placeholder="Your name">
  <label for="theme-choice">Choice</label>
  <select id="theme-choice" name="choice">
    <option>First option</option>
    <option>Second option</option>
  </select>
</form>

## Usage

Set `data-theme` on the root `<html>` element:

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
An unrecognized value also falls back to blue.

Place the attribute on `<html>`, rather than `<body>`, so the root variables are
available throughout the document. Use the standard custom-data attribute
`data-theme` instead of a custom `theme` attribute.

## Hugo

Select the theme for a page in its frontmatter:

```yaml
---
title: Example page
theme: cyan
---
```

`baseof.html` adds `data-theme="cyan"` to `<html>`, so the entire page uses the
selected theme from the first render. Pages without a theme use the site
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
