+++
title = 'htmz'
weight = 50
+++

Load HTML fragments with ordinary links and forms using `target="htmz"`. The shared layout includes htmz and the six extensions shown below. The Aside example continues to use normal page links.

These examples run on the static site. Their HTML responses are available under `htmz/`, relative to the site root. Paths below are relative to this documentation page, so they also work when the site is hosted in a subdirectory.

Each Reset link restores only its example through htmz. The reset response uses `<template><slot>…</slot></template>` to put the original markup back inside the demo container, without reloading the page.

## Basic replacement

The URL fragment identifies the element to replace. Include the same ID in the response to keep that destination available for future requests.

<a class="button outline" href="../../htmz/reset-basic.html#demo-basic" target="htmz">Reset</a>
<a class="button" href="../../htmz/basic.html#basic-result" target="htmz">Load a paragraph</a>
<div id="demo-basic">
  <p id="basic-result" role="status">The response will replace this paragraph.</p>
</div>

```html
<a class="button outline" href="../../htmz/reset-basic.html#demo-basic" target="htmz">Reset</a>
<a class="button" href="../../htmz/basic.html#basic-result" target="htmz">Load a paragraph</a>
<div id="demo-basic">
  <p id="basic-result" role="status">The response will replace this paragraph.</p>
</div>
```

Response:

```html
<p id="basic-result" role="status">This paragraph was loaded without reloading the page.</p>
```

## Loader with aria-busy

When a request starts, the initiating control and destination receive `aria-busy="true"`. The attributes are removed when the response has been processed. Buttons and button links use the stylesheet's existing spinner; no `.loader` class is needed. On a fast connection the spinner may appear only briefly.

<a class="button outline" href="../../htmz/reset-loader.html#demo-loader" target="htmz">Reset</a>
<a class="button" href="../../htmz/loader.html#loader-result" target="htmz">Load content</a>
<div id="demo-loader">
  <p id="loader-result" role="status">Waiting for a response.</p>
</div>

```html
<a class="button outline" href="../../htmz/reset-loader.html#demo-loader" target="htmz">Reset</a>
<a class="button" href="../../htmz/loader.html#loader-result" target="htmz">Load content</a>
<div id="demo-loader">
  <p id="loader-result" role="status">Waiting for a response.</p>
</div>
```

During the request, htmz adds the following state automatically:

```html
<a class="button" href="../../htmz/loader.html#loader-result" target="htmz" aria-busy="true">Load content</a>
<p id="loader-result" role="status" aria-busy="true">Waiting for a response.</p>
```

## Multitarget

Elements in the response replace existing elements with matching IDs. A single response can update several destinations without putting multiple selectors in the URL. Nested elements are extracted first, so the notice in this response reaches its separate destination.

<a class="button outline" href="../../htmz/reset-multitarget.html#demo-multitarget" target="htmz">Reset</a>
<a class="button" href="../../htmz/multitarget.html#multi-result" target="htmz">Update both destinations</a>
<div id="demo-multitarget">
  <p id="multi-result">Main destination.</p>
  <p id="multi-notice" role="status">Notice destination.</p>
</div>

```html
<a class="button outline" href="../../htmz/reset-multitarget.html#demo-multitarget" target="htmz">Reset</a>
<a class="button" href="../../htmz/multitarget.html#multi-result" target="htmz">Update both destinations</a>
<div id="demo-multitarget">
  <p id="multi-result">Main destination.</p>
  <p id="multi-notice" role="status">Notice destination.</p>
</div>
```

Response:

```html
<p id="multi-result">
  <span id="multi-notice" role="status">Both destinations were updated.</span>
  This is the main response. The notice moves to its matching ID elsewhere on the page.
</p>
```

## No-history

After each response, htmz removes and reattaches its hidden iframe. This clears the iframe's history entries. Switch between these messages: the main page URL stays the same and the browser's Back button still leaves this page.

<p>
  <a class="button outline" href="../../htmz/reset-history.html#demo-history" target="htmz">Reset</a>
  <a class="button" href="../../htmz/history-one.html#history-result" target="htmz">First message</a>
  <a class="button" href="../../htmz/history-two.html#history-result" target="htmz">Second message</a>
</p>
<div id="demo-history">
  <p id="history-result" role="status">Choose a message.</p>
</div>

```html
<p>
  <a class="button outline" href="../../htmz/reset-history.html#demo-history" target="htmz">Reset</a>
  <a class="button" href="../../htmz/history-one.html#history-result" target="htmz">First message</a>
  <a class="button" href="../../htmz/history-two.html#history-result" target="htmz">Second message</a>
</p>
<div id="demo-history">
  <p id="history-result" role="status">Choose a message.</p>
</div>
```

This extension is enabled for all htmz requests. Normal links, including the Aside links, retain ordinary browser navigation and history.

## Repeat-gets

Resetting the iframe also lets the same GET URL load again. Edit the field, load the response, edit it again, and click the same link: the response replaces the field each time. Browser HTTP caching rules still apply.

<a class="button outline" href="../../htmz/reset-repeat.html#demo-repeat" target="htmz">Reset</a>
<a class="button" href="../../htmz/repeat.html#repeat-result" target="htmz">Reload the field</a>
<div id="demo-repeat">
  <input id="repeat-result" type="text" value="Edit me, then reload" aria-label="Editable response">
</div>

```html
<a class="button outline" href="../../htmz/reset-repeat.html#demo-repeat" target="htmz">Reset</a>
<a class="button" href="../../htmz/repeat.html#repeat-result" target="htmz">Reload the field</a>
<div id="demo-repeat">
  <input id="repeat-result" type="text" value="Edit me, then reload" aria-label="Editable response">
</div>
```

Response:

```html
<input id="repeat-result" type="text" value="Loaded again" aria-label="Editable response">
```

## Unwrap-template

Wrap context-sensitive HTML, such as table rows, in a top-level `<template>`. This preserves the rows while the browser parses the response. htmz unwraps the template and replaces the placeholder row with its contents.

<a class="button outline" href="../../htmz/reset-rows.html#demo-rows" target="htmz">Reset</a>
<a class="button" href="../../htmz/rows.html#rows-placeholder" target="htmz">Load rows</a>
<div id="demo-rows">
  <table>
    <thead><tr><th>Scientist</th><th>Field</th></tr></thead>
    <tbody>
      <tr id="rows-placeholder">
        <td colspan="2">Rows will load here.</td>
      </tr>
    </tbody>
  </table>
</div>

```html
<a class="button outline" href="../../htmz/reset-rows.html#demo-rows" target="htmz">Reset</a>
<a class="button" href="../../htmz/rows.html#rows-placeholder" target="htmz">Load rows</a>
<div id="demo-rows">
  <table>
    <thead><tr><th>Scientist</th><th>Field</th></tr></thead>
    <tbody>
      <tr id="rows-placeholder">
        <td colspan="2">Rows will load here.</td>
      </tr>
    </tbody>
  </table>
</div>
```

Response:

```html
<template>
  <tr><td>Albert Einstein</td><td>Physics</td></tr>
  <tr><td>Isaac Newton</td><td>Physics and mathematics</td></tr>
</template>
```

## Swap-template

Use a top-level `<template>` with a `<slot>` to keep an existing element or its children. These operations move the original nodes, preserving typed values and attached event listeners.

### Preserve an element

Type in the input, then wrap it. An empty `<slot>` represents the original element, including its current value.

<a class="button outline" href="../../htmz/reset-preserve.html#demo-preserve" target="htmz">Reset</a>
<a class="button" href="../../htmz/preserve.html#swap-preserve" target="htmz">Wrap the input</a>
<div id="demo-preserve">
  <input id="swap-preserve" type="text" value="Your value stays here" aria-label="Input to preserve">
</div>

```html
<a class="button outline" href="../../htmz/reset-preserve.html#demo-preserve" target="htmz">Reset</a>
<a class="button" href="../../htmz/preserve.html#swap-preserve" target="htmz">Wrap the input</a>
<div id="demo-preserve">
  <input id="swap-preserve" type="text" value="Your value stays here" aria-label="Input to preserve">
</div>
```

Response:

```html
<template><section><p>The original input now lives inside this section.</p><slot></slot></section></template>
```

### Replace children while preserving their parent

A `<slot>` containing new HTML represents the original element with new children.

<a class="button outline" href="../../htmz/reset-replace-children.html#demo-content" target="htmz">Reset</a>
<a class="button" href="../../htmz/replace-children.html#swap-content" target="htmz">Replace the contents</a>
<div id="demo-content">
  <section id="swap-content"><p>Original content.</p></section>
</div>

```html
<a class="button outline" href="../../htmz/reset-replace-children.html#demo-content" target="htmz">Reset</a>
<a class="button" href="../../htmz/replace-children.html#swap-content" target="htmz">Replace the contents</a>
<div id="demo-content">
  <section id="swap-content"><p>Original content.</p></section>
</div>
```

Response:

```html
<template><slot><p>New content, inside the original element.</p></slot></template>
```

### Preserve children in a new container

Type in the input, then replace its container. `<slot name="children">` moves the original children into the new HTML.

<a class="button outline" href="../../htmz/reset-preserve-children.html#demo-children" target="htmz">Reset</a>
<a class="button" href="../../htmz/preserve-children.html#swap-children" target="htmz">Replace the container</a>
<div id="demo-children">
  <div id="swap-children">
    <label>Preserved input <input type="text" value="Edit this value" aria-label="Child to preserve"></label>
  </div>
</div>

```html
<a class="button outline" href="../../htmz/reset-preserve-children.html#demo-children" target="htmz">Reset</a>
<a class="button" href="../../htmz/preserve-children.html#swap-children" target="htmz">Replace the container</a>
<div id="demo-children">
  <div id="swap-children">
    <label>Preserved input <input type="text" value="Edit this value" aria-label="Child to preserve"></label>
  </div>
</div>
```

Response:

```html
<template><section id="swap-children"><h3>A new container</h3><slot name="children"></slot></section></template>
```

### Delete an element

An empty template removes the destination.

<a class="button outline" href="../../htmz/reset-delete.html#demo-delete" target="htmz">Reset</a>
<a class="button" href="../../htmz/delete.html#swap-delete" target="htmz">Delete the paragraph</a>
<div id="demo-delete">
  <p id="swap-delete">This paragraph can be removed.</p>
</div>

```html
<a class="button outline" href="../../htmz/reset-delete.html#demo-delete" target="htmz">Reset</a>
<a class="button" href="../../htmz/delete.html#swap-delete" target="htmz">Delete the paragraph</a>
<div id="demo-delete">
  <p id="swap-delete">This paragraph can be removed.</p>
</div>
```

Response:

```html
<template></template>
```

See the [original htmz documentation](https://leanrada.com/htmz/) and [extension examples](https://leanrada.com/htmz/extensions/).
