+++
title = 'Semantic CSS'
description = "A drop-in, beautiful, hand-crafted stylesheet for semantic HTML under 10kb (3.3kb gz'd)."
+++

<section style="margin-block:2rem 4rem">
  <hgroup><h2>A good place to start.</h2><p>Useful defaults for the things you build every day.</p></hgroup>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,16rem),1fr));gap:1rem">
    <div class="card"><h3>Start with HTML</h3><p>Headings, links, forms, and tables get their styles from the elements you already use. Add classes for cards, tags, and a few useful variations.</p><a href="{{< relref "/docs/typography" >}}">Explore the typography →</a></div>
    <div class="card"><h3>Keep it simple</h3><p>Include one CSS file. Use native controls, dialogs, and details elements without a component library or a JavaScript runtime.</p><a href="{{< relref "/docs/components" >}}">Browse the components →</a></div>
    <div class="card"><h3>Make it yours</h3><p>Choose a primary color and let the shared palette handle the rest. Built-in themes adapt to light and dark preferences.</p><a href="{{< relref "/docs/themes" >}}">Meet the themes →</a></div>
  </div>
</section>

<section id="get-started" style="margin-block:4rem">
  <hgroup><h2>One file. A fresh start.</h2><p>Download the stylesheet, add it to your page, and write your HTML.</p></hgroup>
  <pre><code>&lt;link rel="stylesheet" href="semantic.css"&gt;</code></pre>
  <p>You can keep building with the tools you already use. The examples on this site use the same stylesheet you download here.</p>
  <p><span class="tag blue">Blue</span> <span class="tag green">Green</span> <span class="tag violet">Violet</span> <span class="tag red">Red</span> <span class="tag orange">Orange</span></p>
  <a class="button outline" href="{{< relref "/docs/themes" >}}">Customize your theme</a>
</section>

<section id="examples" style="margin-block:4rem">
  <hgroup><h2>Small stylesheet. Plenty of possibilities.</h2><p>A project workspace, a financial dashboard, a journal, and a control room. Four visual examples built from the same elements.</p></hgroup>

{{< example-gallery section="/examples" >}}

</section>
