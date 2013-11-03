playingcards
============

Latex macros to create "Happy Families" cards.

Usage
=====
To create cards for a family with 3 members, each with a picture in `pics/`, use:
```latex
\documentclass[preview,border=4mm,multi=true]{standalone}
\usepackage{lmodern}
\usepackage{xcolor}

\usepackage{cardfamily}
\standaloneenv{tikzpicture}

\begin{document}
\createfamily{Family}{magenta,80,}
 {
  {Member1,picture1.png},
  {Member2,picture2.png},
  {Member3,picture3.png}
 }
\playingcardfamily{Family}
\end{document}
```

The code above would result in 3 cards looking like this:
![Example cards](examples/cards.png)


The syntax for creating a family is:

```latex

\createfamily{Familyname}{color,dingsymbolnumber,\fontsize}
 {
  {Member name, picture_name},
  {Another name, picture_another_name},
  ...
  {Last name, picture_last_name}
 }
```

* `dingsymbolnumber` is a number from the [pifont reference table](http://willbenton.com/wb-images/pifont.pdf).
* `color` is a color like `blue`, `green` etc or an [`xcolor`](http://www.ctan.org/tex-archive/macros/latex/contrib/xcolor).
* `\fontsize` scales the family title and can be `\tiny`, `\normalsize` etc. Left out by default.
* `Member name` is the name of a member in the family.
* `picture_name` is the name of the corresponding picture in `pic/`.


References
==========
The following [tex.stackexchange.com](http://tex.stackexchange.com/) posts were very useful:

* [Creating playing cards using TikZ](http://tex.stackexchange.com/questions/47924/creating-playing-cards-using-tikz)
* [Creating playing cards using TikZ, part 2](http://tex.stackexchange.com/questions/48061/creating-playing-cards-using-tikz-part-2)
* [Processing a sequence of pairs](http://tex.stackexchange.com/questions/141875/processing-a-sequence-of-pairs)
