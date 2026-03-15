## My CV and Resume
 [![Build LaTeX PDF status](https://github.com/jc12011/cv/actions/workflows/build_latex.yml/badge.svg)][workflow-status]

[workflow-status]: https://github.com/jc12011/cv/actions

## General Commands Manual
https://mirror-hk.koddos.net/CTAN/support/latexmk/latexmk.pdf

## My CV
The CV template is based on [dcetin/Simple-CV] under MIT license and studied from [ccwang002/cv], with modifications below.\\
I admired ccwang002's CV simplity style.\\
Style changes:
- Remove Leadership
- Rename Projects to "Project & Creation"
- Modified first page header's margin on the Contact Information
- Added Configuration tour in Readme.md
- Tested building both documents, command work. 

[dcetin/Simple-CV]: https://github.com/dcetin/Simple-CV
[ccwang002/cv]: https://github.com/ccwang002/cv


## My Resume
My resume is inspired from [sansquoi/PlushCV] under Apache License 2.0 and studied from [ccwang002/cv]

[sansquoi/PlushCV]: https://github.com/sansquoi/PlushCV
[ccwang002/cv]: https://github.com/ccwang002/cv


## Dependencies
Fonts in use are included in the repo:

- [Source Serif 4] (SIL Open Font License 1.1)
- [Source Sans 3] (SIL Open Font License 1.1)

[Source Serif 4]: https://github.com/adobe-fonts/source-serif
[Source Sans 3]: https://github.com/adobe-fonts/source-sans


## Configuration
You can modify the subtitle and order in the personal_info.tex


## Installation
On macOS:

    brew install basictex
    sudo tlmgr install \
        latexmk \
        biber biblatex biblatex-nature \
        titlesec enumitem lastpage \
        fancyhdr csquotes \
        datetime2 datetime2-english \
        tracklang fmtcount

## Build

Build only CV or Resume by LuaLaTex.

    latexmk -lualatex cv.tex
    latexmk -luatatex resume.tex

Build both documents by LuaLaTeX.

    latexmk -lualatex cv.tex resume.tex

To clean up the intermediates build files:

    latexmk -c  # remove intermediate files
    latexmk -C  # also remove the compiled documents

This template also sets up a GitHub Workflow that automatically builds PDF online when the badge status shows it's passing.
