+++
title = 'Components'
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
and corner radius as a form.

{{< example >}}
<article class="card">
  <hgroup>
    <header>
      <h3>Example card</h3>
      <button>Button</button>
    </header>
    <p>A summary with an action. Use a card to group related content.</p>
  </hgroup>
</article>
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
