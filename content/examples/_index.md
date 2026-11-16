+++
title = 'Examples'
weight = 60
layout = 'examples'
+++

Four small applications built with the same Semantic CSS components. Each has
its own landing page, linked sections, and a different built-in theme.
SVG illustrations and a few shared layout helpers keep the examples lightweight.

{{< example-gallery >}}

## Build your own

Use `layout = 'app'` for the example shell. Set `landing = true` to remove the
main content width limit and use a full-width hero. Set `width = '60rem'` in a
page's frontmatter to choose its content width, or in a section's `cascade` to
share it across pages. Without `width`, the app uses the stylesheet's default
of `72rem`. A section's `cascade` also propagates its layout
and theme to its pages. Layout styles live directly in the HTML.

All names, balances, transactions, and service metrics are fictional. These are
visual examples without JavaScript, filtering, saving, or account connections.
