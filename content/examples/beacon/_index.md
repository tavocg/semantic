+++
title = 'Beacon'
weight = 40
layout = 'app'
landing = true
theme = 'blue'
sidebar = true
art = 'beacon'
category = 'Control panel'
eyebrow = 'A calmer control room'
headline = 'Keep an eye on everything. Focus on what matters.'
description = 'Service health, recent activity, and the controls your team needs, in one place.'
start = '/examples/beacon/overview'
action = 'Open console'
[cascade]
layout = 'app'
theme = 'blue'
+++

<section id="features"><hgroup><h2>One clear picture of your systems.</h2><p>Enough detail to act. Enough space to think.</p></hgroup><div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,16rem),1fr));gap:1rem"><article class="card"><h3>See the signal</h3><p>Readable service health and a compact overview of recent activity.</p></article><article class="card"><h3>Make deliberate changes</h3><p>A visual layout for service switches and notification preferences.</p></article><article class="card"><h3>Keep the team informed</h3><p>A shared activity log connects the change to the person who made it.</p></article></div></section>
<section style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,16rem),1fr));gap:1rem"><article class="card"><p class="primary">Fictional infrastructure</p><strong>99.98%</strong><p>Illustrative uptime across six sample regions.</p><a class="button" href="{{< relref "/examples/beacon/overview" >}}">Open the control room</a></article><article><h2>Calm is a feature.</h2><p>Clear labels, familiar switches, and actions that explain what happened. A control panel should help you decide, not make you decode.</p><a href="{{< relref "/examples/beacon/settings" >}}">Explore notification settings →</a></article></section>
<section><h2>Built to be understood.</h2><details><summary>Will these controls change a real service?</summary><p>No. All services and metrics are fictional. Controls and statuses illustrate a control panel; they do not change services or save settings.</p></details><details><summary>Does the layout work on mobile?</summary><p>Cards collapse into one column, navigation tabs scroll horizontally, and tables retain their own horizontal scroll.</p></details></section>
