+++
title = '3. Components'
+++

## Tables

### Small table

| Scientist | Field |
| --- | --- |
| Albert Einstein | Physics |
| Isaac Newton | Physics and mathematics |
| James Clerk Maxwell | Physics |

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
    <button class="outline" commandfor="modal-1" command="close">×</button>
  </header>
  {{< lorem >}}
</dialog>

## Accordions

<details open>
  <summary>First section</summary>
  <p>{{< lorem sentence >}}</p>
</details>

<details>
  <summary>Second section</summary>
  <p>{{< lorem sentence 2 >}}</p>
</details>
