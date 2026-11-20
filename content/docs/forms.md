+++
title = 'Forms'
weight = 20
+++

<form>
  <h2>Sign in</h2>
  <p class="mute">This is a form example.</p>
  <label>
    Email
    <input type="email" placeholder="john@doe.com">
  </label>
  <label>
    Password
    <input type="password">
  </label>
  <label>
    <input type="checkbox" checked>
    Remember me
  </label>
  <footer>
    <a href="#" onclick="event.preventDefault()">Already have an account?</a>
    <button aria-busy="true" onclick="event.preventDefault()">Sign in</button>
  </footer>
</form>

## Text fields

Use `type="search"`, `type="file"`, `type="date"`, `type="time"`, or `type="color"` for other input types.

{{< example >}}
<label>
  <span>Name</span>
  <input placeholder="John Doe">
</label>
<label>
  <span>Phone number</span>
  <input type="tel" placeholder="888 8888 8888">
</label>
<label>
  <span>Message</span>
  <textarea placeholder="Message"></textarea>
</label>
<label>Choose color<input type="color" value="#62a6ff"></label>
{{< /example >}}

## Select

{{< example >}}
<label>
  <span>Choose an option</span>
  <select>
    <option>First</option>
    <option>Second</option>
  </select>
</label>
{{< /example >}}

## Slider

{{< example >}}
<label>
  <span>Volume</span>
  <input type="range">
</label>
{{< /example >}}

## Validation

{{< example >}}
<label>
  <span>Valid</span>
  <input type="email" aria-invalid="false" value="incorrect@email.com">
</label>
<label>
  <span>Invalid</span>
  <input type="email" aria-invalid="true" value="correct@email.com">
</label>
{{< /example >}}

## Checkboxes

{{< example >}}
<label><input type="checkbox">Receive updates</label>
<label><input type="checkbox">Share anonymous info</label>
<label><input type="checkbox">Enable something</label>
{{< /example >}}

## Radio buttons

{{< example >}}
<label><input type="radio" name="radio" value="one" checked>One</label>
<label><input type="radio" name="radio" value="two">Two</label>
{{< /example >}}

## Switches

{{< example >}}
<label><input type="checkbox" role="switch">Notify me</label>
{{< /example >}}

## Buttons

{{< example >}}
<button class="plain">Plain</button>
<button class="outline">Outline</button>
<button disabled>Disabled</button>
<button>Button</button>
<button aria-busy="true">Loading</button>
{{< /example >}}

Use `.info` for information, `.alert` for destructive actions, and `.warn` for
actions that need caution. Use `.important` (violet) for important actions and
`.tip` (green) for advice.
These variants also work with `.outline`, `.plain`, and links styled as `.button`.
Their colors adapt to light and dark mode.

### Blue — info

{{< example >}}
<button class="info">View details</button>
<button class="info outline">More information</button>
<button class="info plain">View information</button>
{{< /example >}}

### Green — tip

{{< example >}}
<button class="tip">Show tip</button>
<button class="tip outline">View suggestions</button>
<button class="tip plain">Show shortcut</button>
{{< /example >}}

### Violet — important

{{< example >}}
<button class="important">Save recovery codes</button>
<button class="important outline">Review requirements</button>
<button class="important plain">View requirements</button>
{{< /example >}}

### Red — alert

{{< example >}}
<button class="alert">Delete account</button>
<button class="alert outline">Discard changes</button>
<button class="alert plain">Remove item</button>
{{< /example >}}

### Orange — warn

{{< example >}}
<button class="warn">Pause subscription</button>
<button class="warn outline">Retry payment</button>
<button class="warn plain">Review changes</button>
{{< /example >}}

## Spinner

{{< example >}}
<div class="card" aria-busy="true">
  Loading...
</div>
{{< /example >}}
