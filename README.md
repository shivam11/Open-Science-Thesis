## Open-Science-Thesis

### About

The Open-Science-Thesis
[repository](https://github.com/cpfaff/Open-Science-Thesis) contains a LaTeX
document which is thought to be forked and used for scientific thesis writing
on GitHub. The document combines the typesetting capabilities of LaTeX with the
R programming language for statistics, using the
[Knitr](http://yihui.name/knitr/) package. This combination allows for the
creation of executable documents that enhance the reproducibility of your
research documents.

The Open-Science-Thesis offers a clean and logical folder structure and lots of
examples of typical typesetting requirements to help you typeset your thesis.
It comes with a makefile that helps you to compile, clean and archive the
document. For an example see the PDF file inside of the repository or have a
look into the impressions section below.

### Development Note

This repository is still in development and the commands, environments and the
layout provided by the LaTeX class are subject to change. You might also find
the current version in master branch in unstable state so a compilation to PDF
is not possible!

### Use LaTeX-Class only

If you do not like to use the the document scaffold presented here you can also
use the LaTeX-Class with your own documents. Just
[download](https://github.com/cpfaff/Open-Science-Thesis/blob/master/ost/subdocuments/open_science_thesis.cls)
the class and include it and load it in your preamble with:

```
\documentclass[options]{open_science_thesis}
...
```


## Appetizer

### Titlepages

You can change the titlepage layout to four predefined styles via a class
option:

```
\documentclass[titlepagetheme=vertical]{open_science_thesis}
```

An set the contents for all titlepages with:

```
\ostSetTitle{My own title}
\ostSetSubtitle{The subtitle}
\ostSetAuthor{Author}
\ostSetDate{10.10.1983}
\ostSetAdvisorOne{Advisor: \\ Markus Muggel\\ Hogstreet 1\\ Telephone 1234234}
\ostSetAdvisorTwo{Alexus Quercus\\ Hogstreet 1\\ Telephone 1234234}
```

- vertical

```
% set the text on the bar
\ostSetTextOnBar{Text on vertical bar}
```

![vertical](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/titlepage_vertical_blue.png)

- horizontal

![horizontal](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/titlepage_horizontal_blue.png)

- image

```
% set image
\ostSetBackgroundPic{ostTitlePageBackground.pdf}

% adjust image horizontaly and vertically
\ostSetLength{\ostLenghtBackgroundPicVoffset}{5\baselineskip}
\ostSetLength{\ostLenghtBackgroundPicHoffset}{5mm}

% set opacity of overlay for better reading of title content
% set between 0-1
\ostSetTitleOverlayOpacity{0.7}

% set color of overlay
\ostSetColor{ostColorTitleOverlay}{gray}
```

![image](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/titlepage_image_blue.png)

- plain

![plain](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/titlepage_plain_blue.png)

#### Colors and fonts

You can set the font shapes sizes and colors on the title page:

* colors

```
\ostSetColor{ostColorTitle}{SteelBlue}
\ostSetColor{ostColorSubtitle}{SteelBlue}
\ostSetColor{ostColorAuthor}{SteelBlue}
\ostSetColor{ostColorDate}{SteelBlue}
\ostSetColor{ostColorAdvisor}{SteelBlue}
```

* fonts

```
\ostSetFont{\ostFontTitle}{\Huge}
\ostSetFont{\ostFontSubtitle}{\Large\textbf}
\ostSetFont{\ostFontAuthor}{...}
\ostSetFont{\ostFontDate}{...}
\ostSetFont{\ostFontAdvisor}{...}
```

### Table of Contents

- fancy main tocs

![fancytoc](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/toc_fancy_blue.png)

- Nice formatted parts and partial tocs either on part

```
\documentclass[toctosection=part]{open_science_thesis}
```

![parttocs](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/overview_parttoc.png)

- or chapter sections

```
\documentclass[toctosection=chapter]{open_science_thesis}
```

![chaptertocs](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/overview_chaptertoc.png)

### Lettrines + coloring

The class comes with four predefined color schemes. You can choose by class option:

```
\documentclass[colortheme=orange]{open_science_thesis}
```

* orange

![orange](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/overview_colortheme_orange.png)

* blue

![blue](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/overview_colortheme_blue.png)

* green

![green](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/overview_colortheme_green.png)

* red

![red](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/overview_colortheme_red.png)

#### Own color theme

You can set the color of almost any element in the document. The most prominent
elements that follow the color theme are the title page elements, sections and
the label for the captions. You can set your own colortheme by setting the
following elements colors in your preamble:

```
\ostSetColor{ostColorTitle}{DarkOrange}
\ostSetColor{ostColorSubtitle}{DarkOrange}
\ostSetColor{ostColorChapterHeader}{DarkOrange}
\ostSetColor{ostColorSectionHeader}{DarkOrange}
\ostSetColor{ostColorSubsectionHeader}{DarkOrange}
\ostSetColor{ostColorSubSubsectionHeader}{DarkOrange}
\ostSetColor{ostColorParagraphHeader}{DarkOrange}
\ostSetColor{ostColorCaptionLabel}{DarkOrange}
```

### Quotations

![quotations](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/focus_quotation_orange.png)

### Frames for images

![imageframed](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/focus_image_framed_orange.png)

### Tables (booktabs)

![table](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/focus_table_orange.png)


### Code Listings (in solarized color theme)

![code](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/oneside_color_orange_listing.png)


### Revisions

Set up revisors:

```
\ostSetRevisor{Claas}
```

Then you can comment using revisor name in the document.

```
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum \Claas{This is so nice}
```

You can compile the document in revision mode. This will set up the page to be
larger but keeps the typesetting area the same. Additionally linenumbers are
enabled and comments from revisors (see above) are shown as side notes. If you
remove the option again then the comments of revisors are ignored.

```
\documentclass[revision=true]{open_science_thesis}
```

* Displays

![revision](https://raw.github.com/wiki/cpfaff/Open-Science-Thesis/figures/revision_example_note.png)

## See also

The Open-Science-Thesis is one of a series of document classes. You might also
be interested in one of the following repositories.

- [Open-Science-Paper](https://github.com/cpfaff/Open-Science-Paper)
- [Open-Science-Poster](https://github.com/cpfaff/Open-Science-Poster)

## Self-promotion

Do you like the Open-Science-Thesis repository? You are welcome to follow me on
[GitHub](https://github.com/cpfaff) and or
[Twitter](http://twitter.com/ctpfaff).

## License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by-nc-sa/3.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/">Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License</a>.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/cpfaff/open-science-thesis/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

