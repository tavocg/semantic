+++
title = 'Tasks'
description = 'Small steps, shared momentum. A sample task board.'
weight = 20
+++

<hgroup><header><h2>Today, together</h2><button type="button" commandfor="new-task" command="show-modal">New task</button></header><p>Spring release · all work is sample data.</p></hgroup>
<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,16rem),1fr));gap:1rem"><article class="card"><strong>Review navigation patterns</strong><p>In progress · Maya</p><label><input type="checkbox"> Review complete</label></article><article class="card"><strong>Write the launch checklist</strong><p>To do · Sam</p><label><input type="checkbox"> Checklist complete</label></article><article class="card"><strong>Test on a small screen</strong><p>To do · Jules</p><label><input type="checkbox"> Testing complete</label></article></div>
<dialog id="new-task"><header><h2>A new small step</h2><button type="button" commandfor="new-task" command="close" aria-label="Close">×</button></header><form><label>Task name<input name="task" required maxlength="100" placeholder="What needs to happen?"></label><footer><button type="button" class="outline" commandfor="new-task" command="close">Cancel</button><button type="button">Add task</button></footer></form></dialog>
