+++
title = 'Forms'
weight = 20
+++

<form>
  <hgroup>
    <h2>My form</h2>
    <p>Form that sends data.</p>
  </hgroup>
  <label for="search">Search</label>
  <input type="search" id="search" name="search" placeholder="Search">
  <label for="text">Text</label>
  <input type="text" id="text" name="text" placeholder="Text">
  <label for="select">Select</label>
  <select id="select" name="select" required="">
    <option value="" selected="">Select…</option>
    <option>…</option>
  </select>
  <label for="file">
    <span>File browser</span>
    <input type="file" id="file" name="file">
  </label>
  <label for="range">
    <span>Range slider</span>
    <input type="range" min="0" max="100" value="50" id="range" name="range">
  </label>
  <div class="grid">
    <label for="valid">
      <span>Valid</span>
      <input type="text" id="valid" name="valid" placeholder="Valid" aria-invalid="false">
    </label>
    <label for="invalid">
      <span>Invalid</span>
      <input type="text" id="invalid" name="invalid" placeholder="Invalid" aria-invalid="true">
    </label>
    <label for="disabled">
      <span>Disabled</span>
      <input type="text" id="disabled" name="disabled" placeholder="Disabled" disabled="">
    </label>
  </div>
  <div class="grid">
    <label for="date">
      <span>Date</span>
      <input type="date" id="date" name="date">
    </label>
    <label for="time">
      <span>Time</span>
      <input type="time" id="time" name="time">
    </label>
    <label for="color">
      <span>Color</span>
      <input type="color" id="color" name="color" value="#0eaaaa">
    </label>
  </div>
  <div class="grid">
    <fieldset>
      <legend>Checkboxes</legend>
      <label for="checkbox-1">
        <input type="checkbox" id="checkbox-1" name="checkbox-1" checked="">
        Checkbox
      </label>
      <label for="checkbox-2">
        <input type="checkbox" id="checkbox-2" name="checkbox-2">
        Checkbox
      </label>
    </fieldset>
    <fieldset>
      <legend>Radio buttons</legend>
      <label for="radio-1">
        <input type="radio" id="radio-1" name="radio" value="radio-1" checked="">
        Radio button
      </label>
      <label for="radio-2">
        <input type="radio" id="radio-2" name="radio" value="radio-2">
        Radio button
      </label>
    </fieldset>
    <fieldset>
      <legend>Switches</legend>
      <label for="switch-1">
        <input type="checkbox" id="switch-1" name="switch-1" role="switch" checked="">
        Switch
      </label>
      <label for="switch-2">
        <input type="checkbox" id="switch-2" name="switch-2" role="switch">
        Switch
      </label>
    </fieldset>
  </div>
  <footer>
    <button type="reset" onclick="event.preventDefault()">Reset</button>
    <button type="submit" aria-busy="true" onclick="event.preventDefault()">Submit</button>
  </footer>
</form>

## Heading groups

The first child of an `hgroup` sits on the left, and the second child aligns
on the right, regardless of its element type. Put supporting text third so
it spans both columns underneath and keeps the secondary text color.

<hgroup>
  <strong>Email notifications</strong>
  <input type="checkbox" role="switch" aria-label="Email notifications" checked>
  <p>Receive a short summary of project updates and upcoming milestones.</p>
</hgroup>

```html
<hgroup>
  <strong>Email notifications</strong>
  <input type="checkbox" role="switch" aria-label="Email notifications" checked>
  <p>Receive a short summary of project updates and upcoming milestones.</p>
</hgroup>
```

The heading can also be an `h1`–`h6`. The second child can be an input, button,
link, status label, paragraph, or any other element. Every child after the
second spans both columns below the first row.

<hgroup>
  <h3>Project status</h3>
  <span>Up to date</span>
  <p>All changes are saved.</p>
</hgroup>

```html
<hgroup>
  <h3>Project status</h3>
  <span>Up to date</span>
  <p>All changes are saved.</p>
</hgroup>
```

## Text fields

```html
<label>
  <span>Name</span>
  <input type="text" name="name" placeholder="Your name">
</label>
```

Use `type="search"`, `type="file"`, `type="date"`, `type="time"`, or `type="color"` for other input types.

## Select

```html
<label>
  <span>Choice</span>
  <select name="choice">
    <option>First option</option>
    <option>Second option</option>
  </select>
</label>
```

## Slider

```html
<label>
  <span>Volume</span>
  <input type="range" name="volume" min="0" max="100" value="50">
</label>
```

## Validation

```html
<label>
  <span>Valid</span>
  <input type="text" aria-invalid="false">
</label>
<label>
  <span>Invalid</span>
  <input type="text" aria-invalid="true">
</label>
```

## Checkboxes

```html
<label><input type="checkbox" name="updates" checked> Receive updates</label>
```

## Radio buttons

```html
<label><input type="radio" name="choice" value="one" checked> One</label>
<label><input type="radio" name="choice" value="two"> Two</label>
```

## Switches

```html
<label><input type="checkbox" name="notifications" role="switch"> Notifications</label>
```

## Buttons

```html
<button>Button</button>
<button class="outline">Outline</button>
<button class="plain">Plain</button>
<button type="reset">Reset</button>
<button type="submit">Submit</button>
<a class="button" href="/docs/">Documentation</a>
```

## Busy and disabled states

```html
<button aria-busy="true">Loading</button>
<button disabled>Disabled</button>
<input type="text" disabled>
```

## Spinner

```html
<span class="spinner" role="status" aria-label="Loading"></span>
```
