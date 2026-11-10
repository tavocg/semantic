+++
title = 'Components'
weight = 30
+++

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
</dialog>

```html
<button commandfor="modal-1" command="show-modal">Open modal</button>
<dialog id="modal-1">
  <header>
    <h2>Modal title</h2>
    <button commandfor="modal-1" command="close">×</button>
  </header>
  <p>Modal content.</p>
</dialog>
```

## Accordions

<details open>
  <summary>First section</summary>
  <p>{{< lorem sentence >}}</p>
</details>

<details>
  <summary>Second section</summary>
  <p>{{< lorem sentence 2 >}}</p>
</details>

```html
<details>
  <summary>Section title</summary>
  <p>Section content.</p>
</details>
```

Add `open` to show a section expanded by default.
