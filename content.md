<header>
This here defines the header content for all pages.
</header>

<footer>
This here defines the footer content for all pages.
</footer>


<!-- REFERENCES -->
<src id="markdown">
John Gruber,
*Markdown is a text-to-HTML conversion tool for web writers.*,
2004,
https://daringfireball.net/projects/markdown/
</src>

<src id="markdownpaper">
Eric Dolch,
*Display markdown into paper style HTML site*,
2025,
https://github.com/Wasserwecken/markdownpaper
</src>


<!-- CONTENT -->
# markdownpaper
Use markdown[markdown] to create scientifc scripts or papers, through a single HTML file without runtime dependencies or build process.
Its plain HTML, CSS and Javascript, which does all the workload.

There is no need for NPM, Ruby, Python, Perl Envirnment, Docker container, Java runtime, online dependencies or subscription.
It runs offline *(if your really want to)*, it runs anywhere without any installation, and uses a simple syntax *(markdown)* to define content.

This aims to be as simple as possible for use on any computer at any time and with minimal dependencies as possible.

## Introduction
Some common explanations about the project.

### Intention
I love the idear of LaTeX, writing content and do not care about the document layout. But the steep learning curve of LaTeX and the usage of another required runtime *(Perl)*, which installation is NOT straight forward at all, prevented me from using it.

But as a software engineer I am used to markdown for writing readme's, taking personal notes of projects, todo's or meeting's. It always appeard to me like a LaTeX-Lite version.

I am sick of installing hundreds of megabytes just to complete a simple task. I don't want to get into another syntax, learn the build process or manage abstractions for content. Ever single tool I checked out for converting markdown to a pretty paper styled PDF had their own complexities.


### Installation
Requirements:
- Any modern browser of your choice
- Any text editor of your choice

Quickstart:
- Download the `index.html` from the repository
- Create a file `content.md` in the same directory
- Start writing markdown inside `content.md`
- Load the `index.html` in your browser



### Limitations
Because this project aim's to be simple in code and use and runs within a limited environment *(your browser)*, there are some limitation what you can achive with this.

#### Styling
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.

#### Printing
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.

### Contributing
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.

### Markdown
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.


## Writing markdown
Using plain markdown will already work and alomst every feature is supported. THe following shows the usage of standard markdown elements and their apeareance.

### Headings
Headlines are automatically enumerated by their level, with `#` for H1, `##` for H2, and so on.
The heading `#` *H1* is special because it defines the title of the document and its's content.

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
<div style="margin: 0; font-size: 1.6rem; font-weight: bold;">1. 1. Heading 3</div>
<div style="margin: 0; font-size: 1.4rem; font-weight: bold;">1. 1. 1. Heading 4</div>
<div style="margin: 0; font-size: 1.2rem; font-weight: bold;">1. 1. 1. 1. Heading 5</div>
<div style="margin: 0; font-size: 1.0rem; font-weight: bold;">1. 1. 1. 1. 1. Heading 6</div>


### Paragraphs
Paragraphs are separated by a blank line. The text will be wrapped automatically.
Do not indent your text, otherwise it will be interpreted as a code block.

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
- Item

1 Item
1 Item
    - Sub
1 Item
```
---
- Item
- Item
    1. Sub
- Item

1. Item
1. Item
    - Sub
1. Item

### Images
Images can be included in the markdown file, and will be displayed in the HTML output.
You can use the HTML image tag, or use the markdown syntax. All examples result in the same output.

```
[img]: ./.doc/sailboat.bmp

![img]
![](./.doc/sailboat.bmp)
<img src="./.doc/sailboat.bmp"/>
```
---
<img src="./.doc/sailboat.bmp"/>

### Links


### Quotes
### Code
### Tables

### Extensions
#### Math formulas
#### Header & Footer
#### Internal References
#### External References
#### Wide section


<img src="./.doc/sailboat.bmp"/>
<ref id="sail" type="figure">
Als Künstliche Intelligenz (KI) werden Systeme bezeichnet die Probleme und Aufgaben lösen können die menschliche Intelligenz benötigen oder diese sogar übersteigen.
</ref>

Das Thema der Künstlichen Intelligenz $a = b$ gibt es bereits seit den 50er Jahren. Allerdings waren das alles aber nur theoretische und mathematische Konzepte. Mit den 2000er Jahren kam das Internet in der Gesellschaft an, und die ersten Datenmengen. [sail] Auch die Leistung der Computerhardware wurde mit jedem Jahr leistungsstärker so dass die frühen Konzepte tatsächlich Anwendbar und Wirtschaftlich wurden. Das Interesse die Forschung, und die Ausbildungen dahin sind seit jeher angestiegen und es gab immer neue Durchbrüche, wie z.B. neuronale Netze. Und seit 2020 / 2021 hat es die Aufmerksamkeit der breiten Bevölkerung, angestoßen durch die Veröffentlichung von ChatGPT und DALLE durch OpenAI. Auf einmal konnte jeder ohne technischen Vorkenntnisse Text und Bilder generieren, nur durch die Eingabe von ganz normalem Text, auch natürliche Sprache genannt. Die Möglichkeit das System natürliche Sprache erst seit kurzem verarbeiten und verstehen können.

$$\pi^* = v_{\pi^*}(s) = \max_{a \in A} \sum_{s',r} p(s',r|s,a) [r+\gamma v(s')]$$
