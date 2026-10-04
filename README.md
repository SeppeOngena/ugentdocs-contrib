<h1 align="center">The ugentdocs-contrib $\LaTeX$ package</h1>
<h3 align="center">A curated collection of customizations and extensions for the ugentdocs package</h3>

Overview
--

This package provides a `ugentdocs-contrib.sty` file, which can be used in your document through

    \usepackage[<options>]{ugentdocs-contrib}
    
Currently implemented options for extensions / customizations are:

- `supplementary`: Adds supplementary information styling for the `ugentreport` (or other) classes.
   Provides `\supplementarymaterial`, which can be used instead of `\appendix`, 
   or in the preamble (before `\begin{document}`), which overrides the cover page.
-  `fullcitationlinks`: by default, BibLaTeX only uses the year of a citation as a link.
   This option sets the whole citation as a link.
-  `ugentdocspdfmeta`: Adds ``LaTeX with the ugentdocs package'' as PDF creator to the metadata,
    and provides a `\addugentdocsfootnote`, which adds the same text as a footnote.
-  `rotatedpage`: Adds a new environment of the same name with support for the `thumbs` and `crop` package

Installation
--
>[!WARNING]
> The [`ugentdocs` package](https://github.com/SeppeOngena/ugentdocs/) is required to be installed, of course.

Copy the `ugentdocs-contrib.sty` file into your document folder or clone the repository
and use the [l3build](https://ctan.org/pkg/l3build) package:

    git clone https://github.com/SeppeOngena/ugentdocs-contrib.git
    cd ugentdocs
    l3build install

This installs the current version for your user account.
Undo it with `l3build uninstall`.
