# LaTeX files for Graham Boyd's "Rebuild the economy"
Files for the ebook version of a book written by Graham Boyd,
and commisioned to me for epub conversion.

**Beware** that is process is mainly automated,
but requires some manual intervention here and there.
Also, the generated HTML is messy and ugly.

# General building process
In the future there'll be a Makefile in the repo that'll make this easier,
for now the building process is as follows.

The general idea is to convert TeX files to HTML
and then use the Calibre ebook manager to convert to EPUB3 (or MOBI).
A diagram:
```
TeX --(make4ht)--> HTML --(Calibre)--> EPUB3
```

As the diagram suggests, the HTML conversion is done with the make4ht tool,
commonly distributed in TeXlive and other LaTeX distros.

# Building
I suggest to first check that the TeX files compile normally with pdflatex
(using latexmk, for example)
and then proceed with this.

First we convert to HTML,
```
make4ht -uf html5 MasterEinstein-Picasso-1.tex
```
then add the HTML to calibre as a book and use the GUI conversion to epub.

# Fixes or customizations

Describe custom css or related things used to get a decent look.
