+++
title = '3. Components'
+++

## Tables

| Scientist | Field | Contribution |
| --- | --- | --- |
| Albert Einstein | Physics | Theory of relativity |
| Isaac Newton | Physics and mathematics | Laws of motion and universal gravitation |
| James Clerk Maxwell | Physics | Classical theory of electromagnetism |

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
