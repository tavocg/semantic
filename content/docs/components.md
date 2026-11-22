+++
title = 'Components'
footerTitle = 'UI components'
weight = 30
+++

## Nav

{{< example >}}
<nav>
  <ul>
    <li><a href="#" aria-current="page">First tab</a></li>
    <li><a href="#">Second tab</a></li>
    <li><a href="#">Third tab</a></li>
  </ul>
</nav>
{{< /example >}}

---

## Cards

Use `.card` to group related content with the same surface, padding, border,
and corner radius as a form. In a `header`, the first element expands to fill
the space available beside the other items.

{{< example >}}
<article class="card">
  <header>
    <h3>Example card</h3>
    <button>Button</button>
  </header>
  <p class="mute">A summary with an action. Use a card to group related content.</p>
</article>
{{< /example >}}

---

## Tags and blockquotes

Use `span.tag` for short labels. Tags use the current primary color (`--p`),
while blockquotes use the text color (`--f`) by default, including their border
and subtle background. Add `.info` for information (blue), `.tip` for
advice (green), `.alert` for errors or destructive actions (red),
`.warn` for warnings (orange), and `.important` for
important details (violet). These variants adapt to light and dark mode.
Color classes such as `.blue`, `.green`, and `.violet` are also available.

{{< example >}}
<p>
  <span class="tag">Default</span>
  <span class="tag blue">New</span>
  <span class="tag info">Information</span>
  <span class="tag tip">Tip</span>
  <span class="tag violet">In review</span>
  <span class="tag alert">Blocked</span>
  <span class="tag warn">Needs attention</span>
  <span class="tag important">Important</span>
</p>
<blockquote>A note using the default text color.</blockquote>
<blockquote class="info">Your next statement will be available tomorrow.</blockquote>
<blockquote class="tip">Use the search field to quickly find a transaction.</blockquote>
<blockquote class="warn">Review these changes before continuing.</blockquote>
<blockquote class="alert">The service is unavailable. Try again later.</blockquote>
<blockquote class="important">Save your recovery codes before continuing.</blockquote>
{{< /example >}}

---

## Tables

### Small table

{{< example >}}
<table>
  <thead>
    <tr><th>Scientist</th><th>Field</th></tr>
  </thead>
  <tbody>
    <tr><td>Albert Einstein</td><td>Physics</td></tr>
    <tr><td>Isaac Newton</td><td>Physics and mathematics</td></tr>
    <tr><td>James Clerk Maxwell</td><td>Physics</td></tr>
  </tbody>
</table>
{{< /example >}}

### Wide table

| Scientist | Field | Contribution | Key concepts | Applications |
| --- | --- | --- | --- | --- |
| Albert Einstein | Theoretical physics | Special and general relativity | Spacetime, mass-energy equivalence, gravity | Cosmology and relativistic corrections in satellite navigation |
| Isaac Newton | Physics and mathematics | Laws of motion and universal gravitation | Force, acceleration, momentum, gravitational attraction | Classical mechanics, engineering, and orbital calculations |
| James Clerk Maxwell | Mathematical physics | Classical theory of electromagnetism | Electric and magnetic fields, electromagnetic waves | Radio communication, optics, and electrical engineering |

---

## Progress

Progress bars use the theme's primary color. Set `value` and `max` to show
how much of a task is complete.

{{< example >}}
<label>Upload progress<progress value="65" max="100">65%</progress></label>
{{< /example >}}

---

## Meter

Use `meter` for a measurement within `min` and `max`. The browser evaluates
`value` against `low`, `high`, and `optimum`: green indicates the optimal range,
orange a less favorable range, and red the least favorable range. These colors
reuse the green, orange, and red palettes and adapt to light and dark mode.
Set `optimum` near `max` when higher values are better, or near `min` when lower
values are better.

{{< example >}}
<label>Storage usage<meter max="100" low="60" high="85" optimum="0" value="40">40%</meter></label>
<label>Storage filling up<meter max="100" low="60" high="85" optimum="0" value="75">75%</meter></label>
<label>Storage nearly full<meter max="100" low="60" high="85" optimum="0" value="95">95%</meter></label>
<label>Battery level<meter max="100" low="20" high="60" optimum="100" value="80">80%</meter></label>
{{< /example >}}

---

## Modals

{{< example >}}
<button commandfor="modal" command="show-modal">Open modal</button>
<dialog id="modal">
  <header>
    <h2>Example modal</h2>
    <button commandfor="modal" command="close">×</button>
  </header>
  <p>Modal content.</p>
  <footer>
    <button class="outline" commandfor="modal" command="close">Cancel</button>
    <button>Confirm</button>
  </footer>
</dialog>
{{< /example >}}

---

## Accordions

{{< example >}}
<details open>
  <summary>First section</summary>
  <p>Content for the first section.</p>
</details>

<details>
  <summary>Second section</summary>
  <p>Content for the second section.</p>
</details>
{{< /example >}}

Add `open` to show a section expanded by default.
