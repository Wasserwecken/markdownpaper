<header>
This here defines the header content for all pages.
</header>

<footer>
This here defines the footer content for all pages.
</footer>


<!-- REFERENCES -->
<ref id="markdown" type="citation">
*Markdown syntax*,
John Gruber,
*Markdown is a text-to-HTML conversion tool for web writers.*,
2004,
https://daringfireball.net/projects/markdown/
</ref>

<ref id="markdownpaper" type="citation">
*markdownpaper*,
Eric Dolch,
*Display markdown into paper style HTML site*,
2025,
https://github.com/Wasserwecken/markdownpaper
</ref>

<ref id="mathjax" type="citation">
*MathJax*,
MathJax Team,
*Beautiful and accessible math in all browsers*,
2025,
https://www.mathjax.org/
</ref>

<ref id="mdMarked" type="citation">
*Marked.js*
Christopher Jeffrey, Josh Bruce, Steven, Jamie Davis, Tony Brix, Trevor Buckner
*A markdown parser and compiler. Built for speed*,
2025,
https://marked.js.org/
</ref>



<!-- CONTENT -->
# markdownpaper
Use markdown[markdown] syntax to create beautiful documentations, scientific scripts or papers, through a single static HTML file without runtime dependencies or build processes. Its plain HTML, CSS and Javascript, which does all the workload.

There is no need for NPM, Ruby, Python, Perl Envirnment, Docker container, Java runtime, online dependencies or subscription. It runs offline *(if your really want to)*, it runs anywhere without any installation, and uses a simple syntax *(markdown)* to define content.


## Introduction

### Motivation
Since I have a small lecture at my local university in addition to my full-time job as a software developer, I wanted to provide my students with an engaging script to follow throughout the course. I was looking for a simple stright forward tool.

I love the idear of LaTeX, writing content and do not care about the document layout. But the steep learning curve of LaTeX and the usage of another required runtime *(Perl)*, which installation is NOT straight forward at all, prevented me from using it. But I am used to write markdown for readme's, personal notes, todo's or meeting's. It always appeard to me like a LaTeX-Lite version.

I am sick of installing hundreds of megabytes just to complete a simple task. I don't want to get into another syntax, learn the build process or manage abstractions for content. Ever single tool I checked out for converting markdown to a pretty paper styled PDF had their own complexities.

Thus I created this simple tool to write and edit my script easily and on any device or platform.

### Installation
Requirements:
- Any modern browser of your choice
- Any text editor of your choice

Quickstart:
- Download the `index.html` from the repository
- Create a file `content.md` in the same directory
- Start writing markdown inside `content.md`
- Load the `index.html` in your browser

### Customisation
If you dont like the current styling or choice for font, feel free to edit the embedded stylsheets. If you want to use a CSS framework of your choice for special formatting, just add their CDN link.

If you want to embedd more complex objects or renderning, add your JavaScript library of choice to the header. If you want to change the behaviour of how markdown elements are processed, have a look at the embedded JavaScript code. Its is not minified and should be well documented through comments.

The restriction is that you can use only static compiled resources libraries, there is no support for NPM modules or TypeScript, except you are adding this support by yourself.

### Printing
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.

### Dependencies
This projects stands on the following javascript libraries, they are required and loaded from CDN to handle your markdown content:
- [marked.js](https://github.com/markedjs/marked) - A low-level markdown to HTML parser.
- [MathJax](https://www.mathjax.org/) - For rendering mathematical notations.

If you need to run this tool in a complete offline environment, you can download the required libraries and include them locally.

### Contributing
Feel free to make this tool valuable for your needs and other people. Please contribute your ideas, improvements, or fixes by pull requests.
Please keep following guidelines for contributions:
- The `index.html` should stay the only file required to run the tool, do not add additional files or folders as dependencies. I want this too to be as lightweight and accessable as possible.
- Do not add a CSS framework. All styling made should be included in the `index.html` file. The formatting should be kept simple and minimal, everything else is the choice of the user and can be added by themself.

## Writing markdown
The library `marked.js`[mdMarked] is used for parsing and compiling markdown. Thus all common markdown syntax is supported. The following sections show the apeareance of standard markdown elements. Have a look at the markdown documentation for the basic syntax here <https://www.markdownguide.org/cheat-sheet/>.

### Headings
Headlines are automatically enumerated by their level, with `#` for *H1*, `##` for *H2*, and so on. The heading `#` *H1* is special because it defines the title of the document and its's content.

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


### Paragraphs
Paragraphs are separated by a blank line. The text will be wrapped automatically. Do not indent your text, otherwise it will be interpreted as a code block.

```
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
```
---

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.


### Lists
Lists should behave exactly as expected.

```
- Item
- Item
    1. Sub
    1. Sub
- Item

1 Item
1 Item
    - Sub
    - Sub
1 Item
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

### Links
Links can be created using markdown syntax or HTML tags. Both will be rendered as clickable hyperlinks. They are always rendered italic, and without text or color decoration.

```
[Markdown Guide](https://www.markdownguide.org/)

<https://github.com/Wasserwecken/markdownpaper>

<a href="https://daringfireball.net/projects/markdown/">Markdown Project</a>
```
---

[Markdown Guide](https://www.markdownguide.org/)

<a href="https://daringfireball.net/projects/markdown/">Markdown Paper</a>

<https://github.com/Wasserwecken/markdownpaper>

### Quotes
Quotes can be created using the `>` character at the beginning of a line. It will be rendered as a blockquote.

```
> "The only limit to our realization of tomorrow will be our doubts of today." - Franklin D. Roosevelt
```
---

> "The only limit to our realization of tomorrow will be our doubts of today." - Franklin D. Roosevelt

### Code
Code blocks can be created using triple backticks (```) or by indenting lines with four spaces. They will be rendered in a monospaced font.

```
function helloWorld() {
    console.log("Hello, world!");
}
```

### Tables
Tables can be created using pipes (`|`) and hyphens (`-`). They will be rendered as HTML tables.

```
| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered   |   $12 |
| col 3 is | right-aligned |    $1 |
| this is just | just a very wide | column |
```
---

| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered   |   $12 |
| col 3 is | right-aligned |    $1 |
| this is just | just a very wide | column |

### Extensions
There are several tags and behaviours to extend the markdown definitions. You may want to created citings or sublines to Figures and formulars.

#### Math formulas
Math formulas can be included in the markdown file using the `$` syntax for inline formulas and `$$` for block formulas. The projects uses the `MathJax`[mathjax] library to render these formulas and the syntax is very simillar to LaTeX. Notherless there are some limitation, which can be read at their documentation, as well as the basic usage: <https://docs.mathjax.org/en/latest/>

```
This is a line holding a nested formular, $a^2 * b^2 = c^2$, to show of the inlining.

$$\pi^* = v_{\pi^*}(s) = \max_{a \in A} \sum_{s',r} p(s',r|s,a) [r+\gamma v(s')]$$
```
---
This is a line holding, $a^2 * b^2 = c^2$, a nested formular to show of the inlining.

$$\pi^* = v_{\pi^*}(s) = \max_{a \in A} \sum_{s',r} p(s',r|s,a) [r+\gamma v(s')]$$


#### Header & Footer
A global annotation for all pages, visible the very top and bottom of each page, can be defined anywhere with a `<header>` and `<footer>` tag. You can define them multiple times, but only the content of the very last will be used.

```
<header>
This here defines the header content for all pages.
</header>

<footer>
This here defines the footer content for all pages.
</footer>
```
---
Look at the top and bottom of each page to see the result.


#### References & sublines
Images, formulars, quotes and tables often need additional context or a label to refer from the paragraphs. To encode the label, enumerate the references and attatch them propertly to the corresponding elements, the `<ref>` tag can be used.

Write the `<ref>` tag directly after the element you want to label. Any element like lists, figures or tables can be labeled this way. The tag required two attributes to be configured:
- **`id`** For the reference label, which can be used to refer to this subline.
- **`type`** Specifies the display label of the referenced element.

When parsed, a enumerated label of the specified type is generated and all refers are replaced with that label.

```
> "This is my personal Quote, may stating something important!"

<ref id="myQuote" type="quote">
If there is important context to this quote, it could be included here as subtext.
</ref>

This paragraph can now refer to the quote[myQuote] by using the quote id.
```
---
> "This is my personal Quote, may stating something important!"

<ref id="myQuote" type="quote">
If there would be some important context to this quote, it could be included here.
</ref>

Any paragraph can now refer to the quote[myQuote] by using the quote id.


#### Wide content
TODO TODO

#### Footnotes
TODO TODO

#### Column & page break
TODO TODO

#### Table of contents
TODO TODO

#### Layout configuration
TODO TODO
