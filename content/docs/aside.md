+++
title = 'Aside'
weight = 40
layout = 'aside'
sidebar = 'Supporting information goes here.'
+++

Place an `<aside>` directly inside `<body>` to create a left sidebar. Add an optional header button to open it on small screens.

```html
<body>
  <aside id="site-aside" popover>Supporting information.</aside>
  <header>
    <button popovertarget="site-aside">Menu</button>
  </header>
  <main>
    <p>Main content.</p>
    <footer>Footer</footer>
  </main>
</body>
```

## Main content

{{< lorem >}}

<aside>
  <p>This aside is inside main, so it stays in the normal content flow.</p>
</aside>

The menu button is hidden on large screens. Below 48rem, it opens the sidebar; click outside or press Escape to close it.

On large screens, the sidebar stays visible at the viewport height while the page scrolls. Long sidebar content scrolls independently.
