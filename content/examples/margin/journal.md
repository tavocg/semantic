+++
title = 'Journal'
description = 'A few good things to read, with space to think in between.'
weight = 10
+++

<section>
<header>
  <search><input type="search" placeholder="Search design, places, or rituals"></search>
  <button class="outline" commandfor="story-dialog" command="show-modal">Add story</button>
</header>
<dialog id="story-dialog" aria-labelledby="story-title">
  <header><h2 id="story-title">Add story</h2><button commandfor="story-dialog" command="close" aria-label="Close">×</button></header>
  <form method="dialog">
    <label>Title<input name="title" required></label>
    <label>Summary<textarea name="summary" required></textarea></label>
    <footer><button type="button" class="outline" commandfor="story-dialog" command="close">Cancel</button><button>Add story</button></footer>
  </form>
</dialog>
<p class="mute">3 results</p><div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,16rem),1fr));gap:1rem"><article class="card"><p class="primary">Design · 6 min read</p><h2><a href="{{< relref "/examples/margin/empty-page" >}}">The quiet usefulness of an empty page</a></h2><p>Making room before deciding what belongs there.</p></article><article class="card"><p class="primary">Places · Field note</p><h2>The city before breakfast</h2><p>At six in the morning, familiar streets have a different rhythm. A notebook entry about noticing the details we usually pass by.</p><details><summary>Read the field note</summary><p>The bakery lights were on before the first bus arrived. Someone swept the same doorstep they swept yesterday. A city is also a collection of small, repeated acts of care.</p></details></article><article class="card"><p class="primary">Rituals · Short read</p><h2>A shelf for unfinished things</h2><p>Not every project needs a deadline. Some ideas need a place to wait.</p><details><summary>Read the reflection</summary><p>Leave one shelf unorganized. Let it hold a half-read book, a sketch, a question. Unfinished does not always mean forgotten; sometimes it means still becoming.</p></details></article></div></section>
