+++
title = 'Aside'
weight = 40
layout = 'aside'
sidebar = '''
<h2>Getting started</h2>
<nav>
  <ul>
    <li><a href="#overview">Overview</a></li>
    <li><a href="#layout">Layout</a></li>
    <li><a href="https://example.com">Example</a></li>
  </ul>
</nav>
<h2>Elements</h2>
<nav>
  <ul>
    <li><a href="#text">Text</a></li>
    <li><a href="#inputs">Inputs</a></li>
  </ul>
</nav>
<h2>Components</h2>
<nav>
  <ul>
    <li><a href="#table">Table</a></li>
    <li><a href="#accordion">Accordion</a></li>
  </ul>
</nav>
'''
+++

<style>
/* Match each URL fragment to its sidebar link. */
body:not(:has(> main > section[id]:target)) > aside a[href="#overview"],
body:has(> main > #overview:target) > aside a[href="#overview"],
body:has(> main > #layout:target) > aside a[href="#layout"],
body:has(> main > #text:target) > aside a[href="#text"],
body:has(> main > #inputs:target) > aside a[href="#inputs"],
body:has(> main > #table:target) > aside a[href="#table"],
body:has(> main > #accordion:target) > aside a[href="#accordion"] {
  background-color: var(--cbs);
  border-color: var(--c-border);
}
</style>

<section id="overview">
  <h2>Overview</h2>
  <p>Choose an item in the sidebar to display its content. Each section has its own URL fragment, so you can bookmark it or use the browser's Back button.</p>
  {{< lorem >}}
</section>

<section id="layout">
  <h2>Layout</h2>
  <p>A direct child aside creates a left sidebar. Header, main, and footer stay on the right.</p>
  <p>On small screens, use the menu button to open the sidebar. Click outside or press Escape to close it.</p>
  <aside><p>This aside is inside main and stays in the normal content flow.</p></aside>
</section>

<section id="text">
  <h2>Text</h2>
  <p>Use <strong>strong text</strong>, <em>emphasis</em>, or <mark>highlighted text</mark>.</p>
  {{< lorem >}}
</section>

<section id="inputs">
  <h2>Inputs</h2>
  <label>
    <span>Name</span>
    <input type="text" name="name" placeholder="Your name">
  </label>
  <label><input type="checkbox" name="updates"> Receive updates</label>
</section>

<section id="table">
  <h2>Table</h2>
  <table>
    <thead><tr><th>Scientist</th><th>Field</th></tr></thead>
    <tbody>
      <tr><td>Albert Einstein</td><td>Physics</td></tr>
      <tr><td>Isaac Newton</td><td>Physics and mathematics</td></tr>
    </tbody>
  </table>
</section>

<section id="accordion">
  <h2>Accordion</h2>
  <details>
    <summary>More information</summary>
    <p>{{< lorem sentence >}}</p>
  </details>
</section>
