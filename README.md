playingcards
============

Latex macros to create "Happy Families" cards.

Usage
=====
To create cards for a family with 3 members, use:
```latex
\documentclass[preview,border=4mm,multi=true]{standalone}
\usepackage{lmodern}

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

The syntax for creating a family is
```latex

\createfamily{Familyname}{color,dingsymbolnumber,\fontsize}
 {
  {Member name, picture_name},
  ...
 }
```

Example
=======
The code above would result in 3 cards looking like this:
![Example cards](examples/cards.png)

References
==========
The following [tex.stackexchange.com](http://tex.stackexchange.com/) posts were very useful:

[Creating playing cards using TikZ, part 2](http://tex.stackexchange.com/questions/48061/creating-playing-cards-using-tikz-part-2)

[Processing a sequence of pairs](http://tex.stackexchange.com/questions/141875/processing-a-sequence-of-pairs)
