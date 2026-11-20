+++
title = 'Overview'
description = 'A sample financial snapshot for June. All amounts are fictional.'
weight = 10
+++

<section><nav aria-label="Finance sections"><ul><li><a href="#snapshot" aria-current="page">Snapshot</a></li><li><a href="#cashflow">Cash flow</a></li></ul></nav><button class="outline">Hide amounts</button></section>
<div id="snapshot" style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,16rem),1fr));gap:1rem"><dl class="card"><dt class="mute">Total balance</dt><dd><strong>$24,860</strong></dd><dd>Across three sample accounts</dd></dl><dl class="card"><dt class="mute">Income this period</dt><dd><strong>$6,420</strong></dd><dd>Salary and freelance work</dd></dl><dl class="card"><dt class="mute">Spending this period</dt><dd><strong>$3,180</strong></dd><dd>Within your sample plan</dd></dl></div>
<section id="cashflow" class="card"><header><h2>Cash flow</h2><label>Period<select><option>This month</option><option>This week</option></select></label></header><p class="mute">Illustrative trend; not live market data.</p><svg class="primary" viewBox="0 0 560 150" role="img" aria-label="Illustrative cash flow trend"><path d="M0 145H560M0 75H560" fill="none" stroke="currentColor" opacity=".15"/><polyline points="0,120 80,100 160,110 240,55 320,70 400,25 480,40 560,10" fill="none" stroke="currentColor" stroke-width="4" stroke-linejoin="round"/></svg></section>
<details><summary>What do these numbers mean?</summary><p>The overview uses a fixed fictional dataset. The period selector and privacy button are visual examples; the sample figures remain fixed.</p></details>

<details open>
  <summary>Budgets</summary>
  <table class="nowrap">
    <thead><tr><th>Name</th><th>Item number</th><th>Amount</th><th>Start</th><th>End</th></tr></thead>
    <tbody><tr><td>June services<span class="tag green">Active</span></td><td>101</td><td>$5,000.00</td><td><time datetime="2027-06-01">Jun 1, 2027</time></td><td><time datetime="2027-06-30">Jun 30, 2027</time></td></tr></tbody>
  </table>
  <footer><button class="outline" commandfor="budget-dialog" command="show-modal">New budget</button></footer>
  <dialog id="budget-dialog" aria-labelledby="budget-title">
    <header><h2 id="budget-title">New budget</h2><button commandfor="budget-dialog" command="close" aria-label="Close">×</button></header>
    <form method="dialog">
      <label>Name<input name="name" required maxlength="160"></label>
      <label>Item number<input name="item_number" inputmode="numeric" pattern="[0-9]+" required></label>
      <label>Amount ($)<input type="number" name="amount" min="0" step="0.01" required></label>
      <label>Start (UTC)<input type="datetime-local" name="starts_at" required></label>
      <label>End (UTC)<input type="datetime-local" name="ends_at" required></label>
      <footer><button type="button" class="outline" commandfor="budget-dialog" command="close">Cancel</button><button>Create</button></footer>
    </form>
  </dialog>
</details>
