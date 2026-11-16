+++
title = 'Settings'
description = 'Make the control room work the way your team does.'
weight = 30
+++

<form><fieldset><legend>Workspace</legend><label>Workspace name<input name="workspace" value="Studio North / Production" required></label><label>Default region<select name="region"><option>Central US</option><option>Western Europe</option><option>Asia Pacific</option></select></label></fieldset><fieldset><legend>Notifications</legend><label><input type="checkbox" role="switch" checked> Service interruptions</label><label><input type="checkbox" role="switch" checked> Deployment summaries</label><label><input type="checkbox" role="switch"> Weekly usage digest</label></fieldset><fieldset><legend>Alert delivery</legend><label><input type="radio" name="delivery" value="important" checked> Important events only</label><label><input type="radio" name="delivery" value="all"> Every event</label></fieldset><footer><button type="reset" class="outline">Reset</button><button type="button">Save preferences</button></footer></form>
