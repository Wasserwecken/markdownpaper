# markdownpaper
Write content, focus on content. Layout ain't your problem.

There is no need for NPM, Ruby, Python, Perl Environment, Docker container, Java runtime, online services or subscription. It runs anywhere without any installation and creates a print ready HTML layout.

Do not expect that every single markdown will render correctly. The focus is on academic and printing content. Rendering elements that are larger than a single page are not supported (e.g. large code sections, endless lists, etc.). There are other tools to checkout for converting markdown into presentable HTML like [MkDocs](https://www.mkdocs.org/).


## Extended Markdown
- [x] Sublines for figures, tables, etc.
- [x] Citations
- [x] Footnotes
- [x] Diagrams
- [x] Table of contents
- [x] Multi column Layout
- [x] Per page layout settings



## Documentation & Demo & Service
- [Documentation](https://feralex.github.io/markdownpaper/)
- [Service](https://wasserwecken.github.io/markdownpaper/)
- [Demo](https://feralex.github.io/markdownpaper/)



## Installation & Usage
Requirements:
- Any modern browser of your choice
- Any text editor of your choice

QuickStart 1:
- Download the `index.html` from the repository.
- Load the `index.html` locally in your browser.
- Drag & Drop your markdown file to render.

QuickStart 2:
- Go to <https://wasserwecken.github.io/markdownpaper/>
- Drag & Drop your markdown file to render.



## Motivation
Since I have a small lecture at my local university in addition to my full-time job as a software developer, I wanted to provide my students with an engaging script to follow throughout the course. I was looking for a simple straight forward tool.

I love the idea of LaTeX, writing content and do not care about the document layout. But the steep learning curve of LaTeX and the usage of another required runtime *(Perl)*, which installation is NOT straight forward at all, prevented me from using it. But I am used to write markdown for readme's, personal notes, todo's or meeting's. It always appeared to me like a LaTeX-Lite version.

I am sick of installing hundreds of megabytes just to complete a simple task. I don't want to get into another syntax, learn the build process or manage abstractions for content. Ever single tool I checked out for converting markdown to a pretty paper styled PDF had their own complexities.

Thus I created this simple tool to write and edit my script easily and on any device or platform.



### Customization
Because the tool is just a static HTML file, any customizations can be made immediately. The default paper style and behavior is embedded directly in the `index.html`. There are options to define basic layout and appearance by the `<Config>` tag, which is documented in detail in the section '<a href="#h3-5">3.5. Layout configuration</a>'.

If the standard or extended markdown elements do not fit your needs, any almost any CSS framework and JavaScript library can be added to the `index.html`. The only restriction is the use of static resources, there is no support for NPM modules or TypeScript out of the box.

The restriction is that you can use only static compiled resources libraries, there is no support for NPM modules or TypeScript, except you are adding this support by yourself.



### Contributing
Feel free to make this tool valuable for your needs and other people. Please contribute your ideas, improvements, or fixes by pull requests. Feel free to create issues for formatting errors, documentation improvements and feature requests.

Please keep following guidelines for contributions:
- The `index.html` should stay the only file required to run the tool, do not add additional files or folders as dependencies. I want this too to be as lightweight and accessible as possible.
- Do not add a CSS framework. All styling made should be included in the `index.html` file. The formatting should be kept simple and minimal, everything else is the choice of the user and can be added by themself.
