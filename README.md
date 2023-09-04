# fitch.sty

# LaTeX macros for Fitch style natural deduction

Fitch-style natural deduction is a system for writing proofs in
propositional logic and predicate logic. We use it in our logic courses
at the University of Ottawa. This is a set of easy-to-use LaTeX macros
that I wrote for making handouts for my classes.

With these macros, one can typeset natural deduction proofs in Fitch
style, as in the following example:

![](fitchexample.png){border="0"}

```
\begin{nd}
  \hypo {1} {\forall y \neg P(y)}
  \open          
    \hypo {2} {\exists x P(x)}
    \open[u]       
      \hypo {3} {P(u)}
      \have {4}{\forall y \neg P(y)}  \r{1}
      \have {5} {\neg P(u)}           \Ae{4}
      \have {6} {\bot}                \ne{3,5}
    \close
    \have {6a} {\bot}                 \Ee{2,3-6}
  \close
  \have {7} {\neg \exists x P(x)}     \ni{2-6a}
\end{nd}         
```

The output is shown above, and the corresponding LaTeX code below.

## News

**Version 0.5, Feb 8, 2005.** The ability to handle multi-line formulas
was added.

## Download

-   Complete source: [fitch-0.5.tgz](fitch-0.5.tgz).
-   The documentation: [ps](fitchdoc.ps), [pdf](fitchdoc.pdf).
-   The macros: [fitch.sty](fitch.sty).

## Version

Version 0.5, Feb 8, 2005

## Author

Peter Selinger, University of Ottawa

## Web links

A similar package by another author is

-   [Johan Klüwer\'s Fitch Style
    Package](http://folk.uio.no/johanw/FitchSty.html).

## LICENSE

Copyright (C) 2002-2005 Peter Selinger

This program is free software; you can redistribute it and/or modify it
under the terms of the GNU General Public License as published by the
Free Software Foundation; either version 2, or (at your option) any
later version.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
Public License for more details.

You should have received a copy of the GNU General Public License along
with this program; if not, write to the Free Software Foundation, Inc.,
59 Temple Place, Suite 330, Boston, MA 02111-1307, USA.
