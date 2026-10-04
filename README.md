<h1 align="center">The ugentdocs-contrib $\LaTeX$ package</h1>
<h3 align="center">A curated collection of community-built customizations and extensions for the ugentdocs package</h3>

Overview
--

This package is aimed at extensions or customizations that are not part of the official house style 
(and thus find no place in the `ugentdocs` package) but might be commonly used.
This can include alternative styles (e.g., supplementary information)
or code for specific packages not required by `ugentdocs` (e.g., BibLaTeX).

This package provides a `ugentdocs-contrib.sty` file, which can be used in your document through

    \usepackage[<options>]{ugentdocs-contrib}
    
Currently available options for extensions / customizations are:

- `supplementary`: Adds supplementary information styling for `ugentreport` (or other classes),
   adding an "S"-prefix, e.g., "Figure S1".
   Provides `\supplementarymaterial`, which can be used instead of `\appendix`, 
   or in the preamble (before `\begin{document}`), which overrides the cover page as well.
-  `fullcitationlinks`: by default, BibLaTeX only uses the year of a citation as a link.
   This option sets the whole citation as a link.
-  `ugentdocspdfmeta`: Adds "LaTeX with the ugentdocs package" to the PDF creator metadata field,
    and provides a `\addugentdocsfootnote`, which adds the same text as a footnote when used.
-  `rotatedpage`: Adds a new environment of the same name with support for the `thumbs` and `crop` package.
    This allows landscape pages while keeping the thumbs and header/footer properly oriented.
    The rotation is disabled when the cameraready option is set.

Installation
--
>[!WARNING]
> The [`ugentdocs` package](https://github.com/SeppeOngena/ugentdocs/) is required to be installed, of course.

Copy the `ugentdocs-contrib.sty` file into your document folder or clone the repository
and use the [l3build](https://ctan.org/pkg/l3build) package:

    git clone https://github.com/SeppeOngena/ugentdocs-contrib.git
    cd ugentdocs-contrib
    l3build install

This installs the current version for your user account.
Undo it with `l3build uninstall`.
