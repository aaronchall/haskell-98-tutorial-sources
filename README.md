# haskell-98-tutorial-sources

A Gentle Introduction to Haskell, Version 98 - and climbing?

This is supposedly the source for the official Haskell tutorial.

I have been taking notes from it, but I'm worried parts may be obsolete,
and I want to track the changes and perhaps accepts updates. Perhaps
this version can be used to update the tutorial at 
https://www.haskell.org/tutorial/

If there is a more official repo, please let me know.

Both Paul Hudak and John Peterson are deceased.

Perhaps I should attempt to contact Joseph Fasel or Reuben Thomas.

From the index.html:

> This is the master ~~HTML~~ version of the Gentle Introduction To 
Haskell, version 98. Revised June, 2000 by Reuben Thomas.

> All code in this tutorial, with additional commentary, is found in the
code directory packaged with this tutorial. We suggest that you inspect, 
run, and modify this code as you read the tutorial. This code has been 
tested on Hugs 98.

> Premission is granted to correct, improve, or enhance this document. 
If you wish to publish updated versions of the tutorial on haskell.org 
please contact John Peterson.

> Copyright (C) 1999 Paul Hudak, John Peterson and Joseph Fasel

> Permission is hereby granted, free of charge, to any person obtaining a 
copy of "A Gentle Introduction to Haskell" (the Text), to deal in the Text 
without restriction, including without limitation the rights to use, copy, 
modify, merge, publish, distribute, sublicense, and/or sell copies of the 
Text, and to permit persons to whom the Text is furnished to do so, subject 
to the following condition: The above copyright notice and this permission 
notice shall be included in all copies or substantial portions of the Text.

## Notes and Todo list


- *.verb -> a sort-of markdown/LaTeX that -> LaTeX
- *.tex -> result of *.verb
- tex.hs: preprocessor Latex/verbatim -> HTML 
  (cribbed from Haskell Report)
  Do we abandon LaTeX/verbatim source? - ACH
- verbatim.lex: used to translate verb to latex
- fig1.gif (fibonnaci viz, static)
- fig2.gif (init -> client ->reqs resps<- Server, static)
- title.gif (A Gentle Introduction to Haskell Version 98, static)
- fig1.eps fig2.eps - coreldraw sources for respective gifs
- code/*.lhs: literate Haskell, supplements to the tutorial
  index.html maps semantic Sections (starting with 2, 2.1...) 
  to the .lhs (starting with part1.lhs, part2.lhs...)
  Should we rename these parts to their semantic names?
- haskell-tutorial.aux (an organization of the latex - autogen?)
- haskell-tutorial.bbl (bibliography)
- haskell-tutorial.log (latex log, think we can delete)
- haskell-tutorial.tex (organizes, latex source, verb -> tex?)
- haskell-tutorial.verb (probably source for ^.tex)
- haskell.aux (from Haskell 98 Report source?- autogen?)
- html.config (parameters used by tex.hs)
- index.html - main html page
- make-html - shell script #!/bin/bash 
- makefile - makes the pdf outputs (dvi/ps)
- report-refs.tex - used (imported?) by haskell-tutorial.verb
- reportrefs - referenced by html.config, morerefs=reportrefs
- tutrefs - used by html.config, refs=tutrefs 


Probably should git rm:

- code/index.html~ 
- haskell-tutorial.log
 

What's important:

- don't lose existing functionality/features
  - e.g. right arrow in the LaTeX
  - ...

Things we might should do:

- translate source to modern markdown.
  - pros: source readable, maintainable, result more readable?
  - cons: who has the time?
  - how? copy .verb -> .text (pandoc markdown) and edit
- update images, modernize (fig1.gif, fig2.gif)
- left justify all code in the pdf (instead of centering)
- remove extra whitespace from code examples, that is, like this:

```haskell
add :: Integer -> Integer -> Integer
add x y = x + y
```
not this:
```haskell
add                   :: Integer -> Integer -> Integer
add x y                = x + y
```

- Solicit more contributions from the Haskell community.

## Contributors to the Revision (hosted on github)

- Aaron Hall
- D Kurilo




