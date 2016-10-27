---
# The build requires the following dependencies:
#    TeXLive
#    pandoc 
#    pandoc-citeproc

title: Research Proposal - Object Oriented Shells
#author: Anthony DeDominic
abstract: |
    *The purpose of this document is to layout my plan to build my own shell which will attempt to offer a new spin to an old tool.*
    *It will dicuss the limitations in current shells for handling structured data.*
    *Second section describes the process of creating a new language as whole, defining grammars and so on.*
    *I will then layout why I believe I am qualified to see this project to completion based on my previous experiences.*
    *At the end I'll explain what I expect to create and what problems will be solvable with it.*

papersize: letter
geometry: margin=2cm
fontfamily: mathpazo
fontsize: 10pt
header-includes:
- \hyphenpenalty 10000
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{DeDominic - Proposal}
- \fancyfoot[C]{CSC450 01 - \the\year}
- \fancyfoot[R]{\thepage}
- \twocolumn
- \author{DeDominic, Anthony\\Eastern Connecticut State University\\Willimantic, USA\\dedominica@my.easternct.edu}

link-citations: Yes
references:
- title: 'Caml-Shcaml: An OCaml Library for UNIX Shell Programming'
  DOI: 10.1145/1411304.1411316
  publisher: ACM
  author:
  - family: Heller
    given: Alec
  - family: Tov
    given: Jesse
  id: shcaml
  type: article-journal
  issued:
    year: 2008

- title: A LISP SHELL
  DOI: 10.1145/947639.947642
  publisher: ACM
  author:
  - family: Ellis
    given: John
  id: lispsh
  type: article-journal
  issued:
    year: 1980

- title: 'A New Object-Oriented Programming Language: sh'
  URL: https://www.usenix.org/legacy/publications/library/proceedings/bos94/full_papers/haemer.ps
  publisher: USENIX
  author:
  - family: Haemer
    given: Jeffrey
  id: oosh
  type: article-journal
  issued:
    year: 1994

- title: 'Staged parser combinators for efficient data processing'
  DOI: 10.1145/2660193.2660241
  publisher: ACM OOPSLA
  author:
  - family: Jonnalagedda
    given: Manohar
  - family: Coppey
    given: Thierry 
  - family: et al.
  id: parsecomb
  type: article-journal
  issued:
    year: 2014
---
