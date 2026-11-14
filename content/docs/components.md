+++
title = 'Components'
weight = 30
+++

## Nav

<nav>
  <ul>
    <li><a href="#" aria-current="page">First tab</a></li>
    <li><a href="#">Second tab</a></li>
    <li><a href="#">Third tab</a></li>
  </ul>
</nav>

## Cards

Use `.card` to group related content with the same surface, padding, border,
and corner radius as a form.

<article class="card">
  <header>
    <hgroup>
      <h3>Example card</h3>
      <p>A summary with an action.</p>
    </hgroup>
    <button type="button" commandfor="modal-1" command="show-modal">Details</button>
  </header>
  <p>Use a card to group related content.</p>
</article>

```html
<article class="card">
  <header>
    <hgroup>
      <h3>Example card</h3>
      <p>A summary with an action.</p>
    </hgroup>
    <button type="button" commandfor="modal-1" command="show-modal">Details</button>
  </header>
  <p>Use a card to group related content.</p>
</article>
```

The Details button opens the example modal below. The class also works on
elements such as `<div>` and `<section>`.

## Tables

### Small table

| Scientist | Field |
| --- | --- |
| Albert Einstein | Physics |
| Isaac Newton | Physics and mathematics |
| James Clerk Maxwell | Physics |

```html
<table>
  <thead>
    <tr><th>Scientist</th><th>Field</th></tr>
  </thead>
  <tbody>
    <tr><td>Albert Einstein</td><td>Physics</td></tr>
    <tr><td>Isaac Newton</td><td>Physics and mathematics</td></tr>
  </tbody>
</table>
```

### Wide table

| Scientist | Field | Contribution | Key concepts | Applications |
| --- | --- | --- | --- | --- |
| Albert Einstein | Theoretical physics | Special and general relativity | Spacetime, mass-energy equivalence, gravity | Cosmology and relativistic corrections in satellite navigation |
| Isaac Newton | Physics and mathematics | Laws of motion and universal gravitation | Force, acceleration, momentum, gravitational attraction | Classical mechanics, engineering, and orbital calculations |
| James Clerk Maxwell | Mathematical physics | Classical theory of electromagnetism | Electric and magnetic fields, electromagnetic waves | Radio communication, optics, and electrical engineering |

## Modals

<button commandfor="modal-1" command="show-modal">Open modal</button>

<dialog id="modal-1">
  <header>
    <h2>Example modal</h2>
    <button commandfor="modal-1" command="close">×</button>
  </header>
  {{< lorem >}}
  <footer>
    <button type="button" class="outline" onclick="this.closest('dialog').close()">Cancel</button>
    <button type="button" onclick="this.closest('dialog').close()">Confirm</button>
  </footer>
</dialog>

```html
<button commandfor="modal-1" command="show-modal">Open modal</button>
<dialog id="modal-1">
  <header>
    <h2>Modal title</h2>
    <button commandfor="modal-1" command="close">×</button>
  </header>
  <p>Modal content.</p>
  <footer>
    <button type="button" class="outline" onclick="this.closest('dialog').close()">Cancel</button>
    <button type="button" onclick="this.closest('dialog').close()">Confirm</button>
  </footer>
</dialog>
```

## Accordions

<details open>
  <summary>First section</summary>
  {{< lorem >}}
</details>

<details>
  <summary>Second section</summary>
  {{< lorem >}}
</details>

```html
<details>
  <summary>Section title</summary>
  <p>{{< lorem inline >}}</p>
</details>
```

Add `open` to show a section expanded by default.
