# LaTeX IEEE Template

## Introduction

This is a custom IEEE conference paper template based on the original LateX example provided by [IEEE](http://ctan.imsc.res.in/macros/latex/contrib/IEEEtran/IEEEtran_HOWTO.pdf) and [Overleaf](https://www.overleaf.com/latex/templates/ieee-conference-template/grfzhhncsfqn) template. Use with IntelliJ IDEA by JetBrains&reg;.

## Requirements

A working ```LaTeX``` distribution (i.e. [TeX Live](https://www.tug.org/texlive/)) and [TeXiFy IDEA](https://plugins.jetbrains.com/plugin/9473-texify-idea) plugin pre-installed in the editor.

## Important Files & Folders

```shell
.
├── bib
│   └── document.bib            # Bibliography (BibTeX) example
├── figures
│   └── figure01.png            # Example graphical figure.
├── LaTeX-IEEE-Template.iml
├── out                         # Output directory. (Generated PDF file will be here.)
├── README.md
├── sections                    # (Optional) Separate folder for sections in the document. 
│   └── introduction.tex        # Example section.
└── src
    ├── document.tex            # Main document.
    └── IEEEtran.cls            # IEEEtran Class file.

```

## Usage

Run ```Generate document``` configuration from toolbar or execute these commands in order.
```shell
> pdflatex -file-line-error -interaction=nonstopmode -synctex=1 -output-format=pdf -output-directory=/home/anjalo/Documents/GitHub/AnjaloHettiarachchi/LaTeX-IEEE-Template/out document.tex
> cd out ; bibtex document
> cd .. ; pdflatex -file-line-error -interaction=nonstopmode -synctex=1 -output-format=pdf -output-directory=/home/anjalo/Documents/GitHub/AnjaloHettiarachchi/LaTeX-IEEE-Template/out document.tex
> pdflatex -file-line-error -interaction=nonstopmode -synctex=1 -output-format=pdf -output-directory=/home/anjalo/Documents/GitHub/AnjaloHettiarachchi/LaTeX-IEEE-Template/out document.tex
```