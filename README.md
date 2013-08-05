tikz2pdf
========

As illustrated by [this gallery](http://www.texample.net/tikz/examples/all/), [TikZ](http://sourceforge.net/projects/pgf/) is a package for TeX with which you 
can create beautiful figures. Simply put, TikZ is for print what [D3](http://d3js.org/) is for web.

`tikz2pdf` is there to help you create those beatiful figures.
It is written in Python and only requires a [working TeX system](http://en.wikibooks.org/wiki/LaTeX/Installation). 

Usage
-----

Let's say we have a file named `hello.tikz`, which contains the following:

```latex
\begin{tikzpicture}
    \node[rectangle, draw=red, dotted, thick, rotate=15] {Hello World!};
\end{tikzpicture}
```

Invoke `tikz2pdf hello.tikz` from the command-line in order to create a PDF file named `hello.pdf`.

Templates
---------

The following is the minimal template that is used when no template is specified:

```latex
\documentclass{article}
\usepackage{tikz}
\pagestyle{empty}
\usepackage[active,tightpage]{preview}
\PreviewEnvironment[]{tikzpicture}
\PreviewEnvironment[]{tabular}
\begin{document}
%tikz2pdf-tikz
\end{document}
```

The string `%tikz2pdf-tikz` is replaced with the actual TikZ code.



Command-line options
--------------------

From `tikz2pdf --help`:

    positional arguments:
      TIKZ                  TikZ file(s)
    
    optional arguments:
      -h, --help            show this help message and exit
      -b BIN, --bin BIN     binary to use for compiling (default: pdflatex)
      -d, --debug           print debug information
      -e, --edit            open TikZ file in default editor
      -i, --interactive     start interactive session (same as -evw)
      -c INCLUDE_DIR, --include-dir INCLUDE_DIR
                            additional directory to add to TEXINPUTS
      -n N, --number N      number of iterations to compile (default: 1)
      -o [PDF [PDF ...]], --output [PDF [PDF ...]]
                            output PDF file or directory (with trailing slash)
      -p, --pdflatex        use pdflatex as compiler
      -q, --quiet           suppress compiler output
      -t TEX, --template TEX
                            LaTeX file to use as template
      -v, --view            open PDF file in default viewer
      -w, --watch           recompile when TikZ file or template has changed
      -x, --xelatex         use xelatex as compiler


Configuration
-------------


License
-------

BSD




[XeLaTeX]()
