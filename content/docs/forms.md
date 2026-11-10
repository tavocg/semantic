+++
title = '2. Forms'
+++

<form>
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
      <span>Inalid</span>
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
    <input type="reset" value="Reset" onclick="event.preventDefault()">
    <button type="submit" aria-busy="true" onclick="event.preventDefault()">Submit</button>
  </footer>
</form>
