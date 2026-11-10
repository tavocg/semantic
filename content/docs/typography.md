+++
title = 'Typography'
weight = 10
+++

## Paragraphs

{{< lorem >}}

```html
<p>This is a paragraph.</p>
```

## Blockquotes

> "{{< lorem inline >}}"
>
> *Einstein*

```html
<blockquote>
  <p>A quotation.</p>
  <p><em>Author</em></p>
</blockquote>
```

## Images

![Lighthouse in Portland, United States](https://images.pexels.com/photos/37261855/pexels-photo-37261855.jpeg "Lighthouse in Portland, United States. By Brett A in Pexels.")

```html
<figure>
  <img src="image.jpg" alt="Image description">
  <figcaption>Image caption</figcaption>
</figure>
```

## Lists

- {{< lorem sentence 1 >}}
- {{< lorem sentence 2 >}}
- {{< lorem sentence 3 >}}

1. {{< lorem sentence 1 >}}
2. {{< lorem sentence 2 >}}
3. {{< lorem sentence 3 >}}

```html
<ul>
  <li>First item</li>
  <li>Second item</li>
</ul>
<ol>
  <li>First item</li>
  <li>Second item</li>
</ol>
```

## Inline text elements

<div style="display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:1rem">

  [Link](https://example.com)

  **Bold**

  *Italic*

  <u>Underline</u>

  ~~Deleted~~

  <ins>Inserted</ins>

  <s>Strikethrough</s>

  <small>Small</small>

  a<sup>Sup</sup>, b<sub>Sub</sub>

  <abbr title="Abbreviation">Abbr.</abbr>

  <kbd>Ctrl</kbd>+<kbd>k</kbd>

  <mark>Highlighted</mark>

</div>

```html
<a href="https://example.com">Link</a>
<strong>Bold</strong>
<em>Italic</em>
<u>Underline</u>
<del>Deleted</del>
<ins>Inserted</ins>
<s>Strikethrough</s>
<small>Small</small>
a<sup>2</sup>, b<sub>2</sub>
<abbr title="Abbreviation">Abbr.</abbr>
<kbd>Ctrl</kbd>+<kbd>K</kbd>
<mark>Highlighted</mark>
```

## Headings

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Heading 3

{{< lorem >}}

#### Heading 4

{{< lorem >}}

##### Heading 5

{{< lorem >}}

###### Heading 6

{{< lorem >}}
