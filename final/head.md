
---
# Copyright (C) 2016 Anthony DeDominic
#
# Permission is granted to copy, distribute and/or modify this document
# under the terms of the GNU Free Documentation License, Version 1.3
# or any later version published by the Free Software Foundation;
# with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
# A copy of the license is included in the section entitled "GNU
# Free Documentation License".

# The build requires the following dependencies:
#    TeXLive
#    pandoc 
#    pandoc-citeproc

title: "jcom: A JavaScript Object Shell"
abstract: |
    *With the proliferation of JSON representation of data, shells struggle to make use of them; Currently, shell users rely on tools like jq to handle these structured documents.*
    *This paper will discuss an attempt to bring object-like variables to a new shell, jcom.*
    *The purpose is to allow for shells to natively deserialize json-like documents and to work with them using dot-like notation.*
    *This resulted in a cleaner way of working with json-like documents.*
    *It also led to less characters being required to solve certain problems.*
    *This research suggests shells, like bash, can greatly benefit by providing such structures in later revisions.*
papersize: letter
geometry: margin=2cm
fontfamily: mathpazo
fontsize: 10pt
header-includes:
- \hyphenpenalty 10000
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{DeDominic - jcom}
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
  URL: http://https://www.usenix.org/legacy/publications/library/proceedings/bos94/full_papers/haemer.ps
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

- title: On Certain Formal Properties of Grammars
  DOI: 10.1016/S0019-9958(59)90362-6
  publisher: Elsevier, Information and Control
  issued: 
    year: 1959
  author:
  - family: Chomsky
    given: Noam
  id: formalgram

- title: Synthesizing Context Free Grammars from Sample Strings Based on Inductive CYK Algorithm
  DOI: 10.1007/978-3-540-45257-7_15
  publisher: 'Springer, Grammatical Inference: Algorithms and Applications'
  issued:
    year: 2000
  author:
  - family: Nakamura
    given: Katsuhiko
  - family: Ishiwata
    given: Takashi
  id: synthcfg

- title: 'MaltParser: A Data-Driven Parser-Generator for Dependency Parsing'
  publisher: 'Proceedings of LREC'
  issued:
    year: 2006
  author:
  - family: Nivre
    given: Joakim
  - family: Hall
    given: Johan
  - family: Nilsson
    given: Jens
  id: maltparse

- title: Understanding SOA with Web services
  author:
  - family: Newcomer
    given: Eric 
  - family: Lomow
    given: Greg
  issued: 
    year: 2005
  publisher: Addison-Wesley
  id: understandsoa

- title: 'Bridging the semantic Web and Web 2.0 with representational state transfer (REST)'
  DOI: 10.1016/j.websem.2007.11.002
  publisher: 'Springer, Grammatical Inference: Algorithms and Applications'
  author: 
  - family: Battle
    given: Robert 
  - family: Benson
    given: Edward
  issued: 
    year: 2008
  publisher: Elsevier
  id: semanticrest

- title: Monad Manifesto
  URL: http://www.jsnover.com/Docs/MonadManifesto.pdf
  publisher: Microsoft
  author:
  - family: Snover
    given: Jeffrey
  issued:
    month: Aug
    year: 2002
  id: monadshell

- title: Service-oriented architecture 
  DOI: 10.1109/SAINTW.2003.1210138
  publisher: IEEE
  author:
  - family: Perrey 
  - family: Lycett
  issued:
    month: Jan
    year: 2003
  id: soa

- title: A Systematic Approach to Domain-Specific Language Design Using UML 
  publisher: IEEE
  DOI: 10.1109/ISORC.2007.10
  author:
  - family: Selic
    given: Bran
  issued:
    month: May
    year: 2007 
  id: dsldes
---
