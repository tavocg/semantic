+++
title = 'Forms'
weight = 20
+++

<form>
  <hgroup>
    <h2>Sign in</h2>
    <p>This is a form example.</p>
  </hgroup>
  <label>
    Email
    <input type="email" id="email" placeholder="john@doe.com">
  </label>
  <label>
    Password
    <input type="password" id="password">
  </label>
  <label for="session">
    <input type="checkbox" id="session" checked="">
    Remember me
  </label>
  <footer>
    <button type="reset" class="outline" onclick="event.preventDefault()">Reset</button>
    <button type="submit" aria-busy="true" onclick="event.preventDefault()">Submit</button>
  </footer>
</form>

## Heading groups

The heading can also be an `h1`–`h6`. The second child can be an input, button,
link, status label, paragraph, or any other element. Every child after the
second spans both columns below the first row.

{{< example >}}
<hgroup>
  <header>
    <label for="example-setting"><strong>Example setting</strong></label>
    <input type="checkbox" id="example-setting" role="switch">
  </header>
  <p>Useful for describing switches.</p>
</hgroup>

<hgroup>
  <header>
    <strong>Choose color</strong>
    <input type="color" value="#62a6ff" aria-label="Choose color">
  </header>
  <p>Example description of this setting.</p>
</hgroup>
{{< /example >}}

## Text fields

Use `type="search"`, `type="file"`, `type="date"`, `type="time"`, or `type="color"` for other input types.

{{< example >}}
<label>
  <span>Name</span>
  <input type="text" placeholder="John Doe">
</label>
<label>
  <span>Phone number</span>
  <input type="tel" placeholder="888 8888 8888">
</label>
<label>
  <span>Message</span>
  <textarea placeholder="Message"></textarea>
</label>
{{< /example >}}

## Select

{{< example >}}
<label>
  <span>Choose an option</span>
  <select name="choice">
    <option>First</option>
    <option>Second</option>
  </select>
</label>
{{< /example >}}

## Slider

{{< example >}}
<label>
  <span>Volume</span>
  <input type="range" name="volume" min="0" max="100" value="50">
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

## Spinner

{{< example >}}
<div class="card" aria-busy="true">
  Loading...
</div>
{{< /example >}}
