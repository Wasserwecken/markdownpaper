<Config columns=2 padding="16mm" fontSize="9pt" hyphens="auto" textAlign="justify" fontFamily="'LMRoman10', Georgia, serif" CornellSize="0mm"></Config>

<Header>
This here defines the header content for all pages.
</Header>

<Footer>
This here defines the footer content for all pages.
</Footer>


<Ref id="markdownpaper" type="citation">
*markdownpaper*,
Eric Dolch,
*Display markdown into paper style HTML site*,
2025,
https://github.com/Wasserwecken/markdownpaper
</Ref>

<Ref id="mathjax" type="citation">
*MathJax*,
MathJax Team,
*Beautiful and accessible math in all browsers*,
2025,
https://www.mathjax.org/
</Ref>

<Ref id="mdMarked" type="citation">
*Marked.js*
Christopher Jeffrey, Josh Bruce, Steven, Jamie Davis, Tony Brix, Trevor Buckner
*A markdown parser and compiler. Built for speed*,
2025,
https://marked.js.org/
</Ref>



# markdownpaper
Use markdown[markdown] syntax to create beautiful documentations, scientific scripts or papers, through a single static HTML file without runtime dependencies or build processes.

There is no need for NPM, Ruby, Python, Perl Environment, Docker container, Java runtime, online services or subscription. It runs anywhere without any installation and creates a print ready HTML layout.

Write content, focus on content. Layout ain't your problem.

Do not expect that every single markdown will render correctly. The focus is on academic and printing content. Rendering elements that are larger than a single page are not supported (e.g. large code sections, endless lists, etc.). There are other tools to checkout for converting markdown into presentable HTML like [MkDocs](https://www.mkdocs.org/).



<TableOfContents>
## Content
</TableOfContents>


<ColumnBreak></ColumnBreak>

## Introduction
This is the documentation about *markdownpaper* and its usage. It covers all configuration options as well as the extended syntax, enabling important features like Citations and math formulas.



<div>

### Content source
There are three approaches to render markdown content:
1. Open the `index.html` locally and drag & drop your markdown file to render.
1. Host the `index.html` as static Website with a markdown file on the webserver. The default path is `./contend.md`.
1. Embed markdown content directly into `index.html` by editing the first script tag with the id `mdContent` and removing the `src` attribute.

The root path of any media defined in the markdown is the location of the `index.html`. The actual location of the content is NOT respected. Make sure that all resources, like images, use the root path of the `index.html`.

Loading the markdown content automatically works only if the `index.html` is hosted, because the browser blocks fetching from local file paths. The default loading path can be changed by editing the `src` attribute in the first script tag with the id `mdContent`.

*IMHO:* My setup is [VSCode](https://code.visualstudio.com/) with the extension [Live Preview](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server). This will host the `index.html` locally without headache and enables a live preview of the content.

</div>



<div>

### Printing
The main purpose of this tool is to create a PDF through the browsers print option. Thus all pages are exactly shaped as A4 in portrait orientation, because this is the common format for documentations or papers. This trick and the browser printing have some limitations that cannot be avoided, because JavaScript is not allowed to modify printing options.

If there is the need of another paper size like A5, the sizes has to be edited in the embedded style sheets of the `index.html`. When printing the document, the custom page size should also be set in the printing options again, this can be done automatically as well as enabling printing background images and colors!

When printing, any padding of the page should be removed. The printing border is already handled by the page layout, allowing for individual configuration.

</div>


<ColumnBreak></ColumnBreak>

## Writing markdown
The library marked.js[mdMarked] is used for parsing and compiling markdown. Thus all common markdown syntax is supported. The following sections show the appearance of standard markdown elements.

<div>



### Headings
Headlines are automatically enumerated by their level, with `#` for *H1*, `##` for *H2*, and so on. The heading `#` *H1* is special because it defines the title of the document and its's content, it is not enumerated and will not appear in the table of contents.

```
# Heading 1

## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
---

<div style="margin: 0; font-size: 3.0rem; font-weight: bold;">Heading 1</div>
<div style="margin: 0; font-size: 1.8rem; font-weight: bold;">1. Heading 2</div>
<div style="margin: 0; font-size: 1.5rem; font-weight: bold;">1. 1. Heading 3</div>
<div style="margin: 0; font-size: 1.3rem; font-weight: bold;">1. 1. 1. Heading 4</div>
<div style="margin: 0; font-size: 1.1rem; font-weight: bold;">1. 1. 1. 1. Heading 5</div>
<div style="margin: 0; font-size: 1.0rem; font-weight: bold;">1. 1. 1. 1. 1. Heading 6</div>

</div>



<div>

### Paragraphs
Paragraphs are separated by a blank line. The text will be wrapped automatically. Do not indent your text, otherwise it will be interpreted as a code block.

```
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
```
---

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.

</div>



<div>

### Lists
Lists can be created using the `-` or `1.` characters for unordered lists, and numbers followed by a period for ordered lists. Sub-items are supported as well and can be created by indenting the sub-items.

```
- Item
- Item
    1. Sub
    1. Sub
- Item

1. Item
1. Item
    - Sub
    - Sub
1. Item
```
---

- Item
- Item
    1. Sub
    1. Sub
- Item

1. Item
1. Item
    - Sub
    - Sub
1. Item

</div>



<div>

### Images
Images can be included in the markdown file, and will be displayed in the HTML output. You can use the HTML image tag, or use the markdown syntax. All examples result in the same output.

```
[img]: ./.doc/sailboat.bmp
![img]
![](./.doc/sailboat.bmp)
<img src="./.doc/sailboat.bmp"/>
```
---

<img src="./.doc/sailboat.bmp"/>

</div>



<div>

### Links
Links can be created using markdown syntax or HTML tags. Both will be rendered as clickable hyperlinks. They are always rendered italic, and without text or color decoration.

```
[Markdown Guide](https://www.markdownguide.org/)

<https://github.com/Wasserwecken/markdownpaper>

<a href="https://daringfireball.net/projects/markdown/">Markdown Project</a>
```
---

[Markdown Guide](https://www.markdownguide.org/)

<a href="https://daringfireball.net/projects/markdown/">Markdown Source</a>

<https://github.com/Wasserwecken/markdownpaper>

</div>



<div>

### Quotes
Quotes can be created using the `>` character at the beginning of a line. It will be rendered as a blockquote.

```
> "The only limit to our realization of tomorrow will be our doubts of today." - Franklin D. Roosevelt
```
---

> "The only limit to our realization of tomorrow will be our doubts of today." - Franklin D. Roosevelt

</div>



<div>

### Code
Code blocks can be created using triple backticks (```) or by indenting lines with four spaces. They will be rendered in a monospaced font with a gray background.

```
function helloWorld() {
    console.log("Hello, world!");
}
```

</div>



<div>

### Tables
Tables can be created using pipes (`|`) and hyphens (`-`). They will be rendered as HTML tables.

```
| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 |  left-aligned | $1600 |
| col 2 |    centered   |   $12 |
| col 3 | right-aligned |    $1 |
| Lorem | Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. | ipsum |
```
---

| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 |  left-aligned | $1600 |
| col 2 |    centered   |   $12 |
| col 3 | right-aligned |    $1 |
| Lorem | Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. | ipsum |

</div>



## Markdown Extensions
There are several tags and behaviours to extend the markdown definitions. These extensions are the key of writing serious scripts with proper citations, sublines or table of contents.



<div>

### Math formulas
Math formulas can be included in the markdown file using the `$` syntax for inline formulas and `$$` for block formulas. The projects uses the MathJax[mathjax] library to render these formulas and the syntax is very simillar to LaTeX. Notherless there are some limitation, which can be read at their documentation, as well as the basic usage: <https://docs.mathjax.org/en/latest/>

```
This is a line holding a nested formular, $a^2 * b^2 = c^2$, to show of the inlining.

$$\pi^* = v_{\pi^*}(s) = \max_{a \in A} \sum_{s',r} p(s',r|s,a) [r+\gamma v(s')]$$
```
---
This is a line holding, $a^2 * b^2 = c^2$, a nested formular to show of the inlining.

$$\pi^* = v_{\pi^*}(s) = \max_{a \in A} \sum_{s',r} p(s',r|s,a) [r+\gamma v(s')]$$

</div>



<div>

### Header & Footer
A global annotation for all pages, visible the very top and bottom of each page, can be defined anywhere with a `<Header>` and `<Footer>` tag. You can define them multiple times, but only the content of the very last will be used.

```
<Header>
This here defines the header content for all pages.
</Header>

<Footer>
This here defines the footer content for all pages.
</Footer>
```
---
Look at the top and bottom of each page to see the result.

</div>



<div>

### Grouping
Elements can be grouped together to avoid a split on page or column breaks. Group does not force a page or column break, but the content will stay in the same column. Elements can be grouped together by using the `<div>` tag and content to be grouped should be placed inside the `<div>` tag.

Content should not be indented at all, and there must be an empty line before and after the `<div>` tag to be recognized correctly. This behaviour breaks if the grouped content is bigger than the page size to fit in.

```
<div>

## Heading in a div
This is my important content.

</div>

```
---
All sections content is grouped together, no section should spread over multiple columns or pages.

</div>



### References & Sublines
Images, formulars, quotes and tables often need additional context or a label to refer from the paragraphs. Use the `<ref>` tag to define citations, references or footnotes.

The tag requires to attributes to be set:
- **id** - Used to create internal references by using brackets.
- **type** - Determines the behaviour and label for the reference.


<div>

#### Citations
Citations give credit to the original authors of ideas and information, help readers verify information and explore sources further. Set the `type` attribute to `citation` and place the information inside the tag anywhere in your document. The tag is not rendered inplace, but will be added to the reference list.

Use the tag `<References>` to render the list of citations where you need to show them. All content inside the reference list tag will be rendered first and all citations are then listed below.

```
<Ref id="markdown" type="citation">
*Markdown syntax*,
John Gruber,
*Markdown is a text-to-HTML conversion tool for web writers.*,
2004,
https://daringfireball.net/projects/markdown/
</Ref>

<References>
## References
</References>
```
---
<Ref id="markdown" type="citation">
*Markdown syntax*,
John Gruber,
*Markdown is a text-to-HTML conversion tool for web writers.*,
2004,
https://daringfireball.net/projects/markdown/
</Ref>

<References>
## References
</References>

</div>



<div>

#### Footnotes
To add small numbered notes with additional information at the bottom of a page. Set the `type` attribute to `footnote` and place the information inside the tag anywhere in your document. The tag is not rendered inplace, but will be rendered at the bottom of the page where the reference is refered to.

```
<Ref id="myFoot" type="footnote">
In geometry, a **straight** line, usually abbreviated line, is an infinitely long object with no width, depth, or curvature, an idealization of such physical objects as a straightedge, a taut string, or a ray of light.
</Ref>

This line[myFoot] has an annotation to some additional information.
```
---
<Ref id="myFoot" type="footnote">
In geometry, a **straight** line, usually abbreviated line, is an infinitely long object with no width, depth, or curvature, an idealization of such physical objects as a straightedge, a taut string, or a ray of light.
</Ref>

This line[myFoot] has a annotation to some additional information.


</div>



<div>

#### Sublines
The `<ref>` is also used to annotate and label any element in the document. The element placed before the `ref` tag is then used as target for the annotation. Any element like lists, figures or tables can be labeled this way. Set the `type` attribute to anything else than `footnote` or `citation`, the given type name is then used as label for the subline and will be enumerated.

```
> "This is my personal Quote, may stating something important!"

<ref id="myQuote" type="quote">
This is an important addition to the quote.
</ref>

<img src="./.doc/sailboat.bmp"/>

<ref id="myFig" type="figure">
I did not expect using Lorem Ipsum that much after I knew about it.
</ref>

This paragraph can now refer to the quote[myQuote] by using the quote id and also to the [myFig] showing off the linking.
```
---
> "This is my personal Quote, may stating something important!"

<ref id="myQuote" type="quote">
An addition to the quote would not improve the conclusion.
</ref>

<img src="./.doc/plot.png"/>

<ref id="myFig" type="figure">
There is a wobbly line in the figure to express something important.
</ref>

</div>



<div>

### Layout configuration
The general look and feel of the renderer can be adjusted with ease by using the `<Config>` tag. Several attributes are supported:
- **Columns**: Defines the columns per page as integer. Recommended is 2 or 1.
- **Padding**: Defines the print border of each page. Any CSS value can be used like '2rem' or '1.5cm'.
- **Hyphens**: Specifies how words should be hyphenated when text wraps across multiple lines. [Use any valid CSS hyphens value](https://developer.mozilla.org/en-US/docs/Web/CSS/hyphens).
- **TextAlign**: Sets the horizontal alignment of the inline-level content. [Use any valid CSS text-align value](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align).
- **FontFamily**: Specifies a prioritized list of one or more font family names and/or generic family names. [Use any valid CSS font-family value](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family).
- **FontSize**: Sets the base size of the font, headings and other special elements are in relation to this size. [Use any valid CSS font-size value](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size).
- **CornellSize**: Defines an extra right padding of the content, providing space for custom notes by the reader. This is also known as the 'cornell method'. Any CSS size value is accepted.


```

<Config columns=2 padding="16mm" fontSize="9pt" hyphens="auto" textAlign="justify" fontFamily="'Linux Libertine O', math, Georgia, serif" CornellSize="0mm"></Config>

```
---
The look and feel of this document is equivalent to the shown config.

</div>



<div>

### Column & Page break
Sometimes it is required to control the flow and content seperation by column or page breaks. Us the tags `<PageBreak>` or `<ColumnBreak>` to force a new page or column for the following content.

If the layout specifies only a single column for each page, tjhe behaviour of `<ColumnBreak>` is equivalent to `<PageBreak>`.

The `<PageBreak>` does not only force a new page, but can also later the look and feel for all following pages, enabling for alternating styles within a single document. All attributes of `<Config>` are supported.

```
<ColumnBreak></ColumnBreak>

<PageBreak Columns=1></PageBreak>
```


</div>



<div>

### Table of contents
To render a table of contents, place the `<TableOfContents>` tag anywhere it is desired. Only enumerated headings of h2 or lower are included. Any markdown content provided within the tag is placed before any content list item.

```
<TableOfContents>
## Content
</TableOfContents>
```
---
The table of contents at the beginning of this document is renderd by the shown example.

</div>


### Column span
TODO TODO



<div>

### Diagrams
Diagrams from `https://app.diagrams.net/` can be embedded directly into the document with the `drawio` tag.

The diagram data can be provided either via an URL that can be set as `src` attribute in the tag. If this attribute is not defined, the content of the tag is expected to hold the diagram data.

```
<drawio src="./.doc/graph.drawio"></drawio>

```
---
<drawio src="./.doc/graph.drawio"></drawio>

</div>



<div>

### Complex content
Because markdown is converted to HTML elements, any HTML structure can be embedded into the markdown. Almost any content style can be created this way.

```
<div style="position: relative; height: 16rem;">
    <div style="background-color: white; position: absolute; transform: rotate(-15deg);">
        <iframe src="https://www.example.com" style="border: 5px dashed #1C6EA4; overflow: hidden; height: 14rem;"></iframe>
    </div>
</div>
```
---
<div style="position: relative; height: 16rem;">
    <div style="background-color: white; position: absolute; transform: rotate(-15deg);">
        <iframe src="https://www.example.com" style="border: 5px dashed #1C6EA4; overflow: hidden; height: 14rem;"></iframe>
    </div>
</div>

</div>
