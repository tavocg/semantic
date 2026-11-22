+++
title = 'Semantic CSS'
+++

<section style="margin-block:2rem 4rem">
  <h2>A good place to start.</h2><p class="mute">Useful defaults for the things you build every day.</p>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,16rem),1fr));gap:1rem">
    <div class="card"><h3>Start with HTML</h3><p>Headings, links, forms, and tables get their styles from the elements you already use. Add classes for cards, tags, and a few useful variations.</p><a href="{{< relref "/docs/typography" >}}">Explore the typography →</a></div>
    <div class="card"><h3>Keep it simple</h3><p>Include one CSS file. Use native controls, dialogs, and details elements without a component library or a JavaScript runtime.</p><a href="{{< relref "/docs/components" >}}">Browse the components →</a></div>
    <div class="card"><h3>Make it yours</h3><p>Choose a primary color and let the shared palette handle the rest. Built-in themes adapt to light and dark preferences.</p><a href="{{< relref "/docs/themes" >}}">Meet the themes →</a></div>
  </div>
  <p>A page with a heading, a short form, and a table is enough to see how the defaults work together and where your project needs its own styles.</p>
</section>

<section id="get-started" style="margin-block:4rem">
  <h2>One file. A fresh start.</h2><p class="mute">Download the stylesheet, add it to your page, and write your HTML.</p>

{{< stylesheet-example >}}

  <p>You can keep building with the tools you already use. The examples on this site use the same stylesheet you download here.</p>
  <p>Put the link in your document's <code>&lt;head&gt;</code> so the browser can discover the stylesheet as it reads the page.</p>
  <p><span class="tag blue">Blue</span> <span class="tag green">Green</span> <span class="tag violet">Violet</span> <span class="tag red">Red</span> <span class="tag orange">Orange</span></p>
  <a class="button outline" href="{{< relref "/docs/themes" >}}">Customize your theme</a>
</section>

<section style="margin-block:4rem">

## Add it to an existing site

Pick one page that already has a form or a table and add Semantic CSS there first. Load your existing stylesheet after it, and compare the page on a narrow screen and with keyboard navigation. Check that table headers still line up with their columns, form labels are easy to match to their fields, and focus is visible as you tab through the page.

Keep your layout and any styles specific to your project. Once you've seen which defaults work for that page, you can remove any local rules they already cover and try the same setup on another page.

</section>

<section style="margin-block:4rem">

## Why Semantic CSS?

Semantic CSS helps you supercharge HTML with a single lightweight stylesheet. Start with the elements that already describe your page. A `<label>` names a form field, a `<button>` provides keyboard interaction, and `<details>` with `<summary>` gives you a disclosure the browser can open and close on its own.

The stylesheet gives those elements consistent defaults for spacing, type, and color. You can keep the markup small, skip extra wrappers and classes for everyday elements, and save JavaScript for behavior specific to your site.

A small data table is a good example. Its `<caption>` tells readers what the table contains, and its `<th>` cells mark the headers. That same markup gives the stylesheet elements it can style directly and gives assistive technology information about the table's structure.

</section>

<section style="margin-block:4rem">

## See what plain HTML can do

<section class="card">
  <header>
    <h3>Try the release preview</h3>
    <button type="button" commandfor="release-preview" command="show-modal">Open preview</button>
  </header>
  <p class="mute">Review a draft release and see how Semantic CSS styles its status and notes.</p>
</section>

<dialog id="release-preview" aria-labelledby="release-preview-title">
  <header>
    <h3 id="release-preview-title">Release preview</h3>
    <button type="button" commandfor="release-preview" command="close" aria-label="Close">×</button>
  </header>
  <p><span class="tag info">Draft</span> <span class="tag warn">In review</span></p>
  <blockquote class="info"><strong>What's new</strong><p>The release includes updated form styles and examples.</p></blockquote>
  <blockquote class="tip"><strong>Before publishing</strong><p>Preview the release on a narrow screen.</p></blockquote>
  <footer>
    <button type="button" class="outline" commandfor="release-preview" command="close">Close</button>
    <button type="button" aria-busy="true">Publishing…</button>
  </footer>
</dialog>

<p>See the <a href="{{< relref "/docs/components#modals" >}}">component documentation for modals</a>.</p>

</section>

<section style="margin-block:4rem">

## The TCP initial congestion window

On a new TCP connection, the initial congestion window limits how much data the sender can have in flight before it receives acknowledgments. With a window of ten segments carrying 1,460 bytes each, the first burst can carry up to 14,600 bytes of TCP payload. After HTTP and TLS overhead, the compressed HTML has a little less room. That's where the roughly 14 kB rule of thumb comes from.[^endtimes-14kb]

If your HTML and the styles needed for the first render fit in that first burst, the browser can receive them without waiting for another round trip for the rest of the response. That matters most on high-latency connections. Keep the opening content and critical CSS small, and let the rest load as needed.

To see how much your page sends, reload it with caching disabled in your browser's Network panel. Look at the transferred size of the document, then check which styles, fonts, and images the browser needs before it can display the main content.

</section>

<section style="margin-block:4rem">

## What fits in the first response?

Measured from a local production build of this homepage with `gzip -n -9`, the HTML response body is about **10.3 kB**. It includes the stylesheet, the interactive example, and the SVG previews in the gallery. The logo is a separate **0.6 kB** SVG file before compression. The page also declares a **5.1 kB** Apple touch icon that supported clients can request. The standalone stylesheet is **3.4 kB** gzipped and is fetched separately when you click **Download**.

These figures measure the files. The first TCP window also has to carry response headers and TLS overhead. Keeping the styles and the first piece of content in the HTML puts them in the same response, where the browser can start using them as they arrive.

</section>

<section id="examples" style="margin-block:4rem">
  <h2>Small stylesheet. Plenty of possibilities.</h2><p class="mute">A project workspace, a financial dashboard, a journal, and a control room. Four visual examples built from the same elements.</p>
  <p>Compare how each example gives the same elements a different job. The workspace uses forms to organize tasks, the journal gives long-form text room to breathe, and the dashboards put figures and status updates up front.</p>

{{< example-gallery section="/examples" >}}

<p>Ready to try it on your own page? <a href="{{< relref "/docs" >}}">Read the Semantic CSS documentation</a>.</p>

</section>

[^endtimes-14kb]: Nathaniel, [Why your website should be under 14kB in size](https://endtimes.dev/why-your-website-should-be-under-14kb-in-size/). See also [RFC 6928, Increasing TCP's Initial Window](https://www.rfc-editor.org/rfc/rfc6928.html#section-2).
