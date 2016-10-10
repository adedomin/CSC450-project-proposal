1. Background
=============

Shells are the primary interface into a POSIX system.
As a result, many tools and utilities rely on shells to handle and process files and their data.
However, shells have one strong limitation in them;
the data they work with is not strongly structured.
As a result, sysadmins and programmers make use of confusing and massive awk scripts and shell pipelines to derive valuable information.
Even variables like \$IFS can completely alter how this byte[] stream is parsed.

If any changes were to occur in coreutils, it could break numerous tools and scripts.
Even using different coreutils can lead to issues.
For instance, many of GNU's coreutils, such as their implementation of grep and df, add features not strictly standardized by POSIX.
scripts and other shell invoked utilities make use of what can best be described as, named parameters.
These named parameters, known as arguments, can be hard to remember using short, single letter identifiers.

1.1. Other Attempts
-------------------

an OCaml library called shcaml added a functional composer called shtreams which allows for transforming byte streams into structured documents [@shcaml].
Some developers have tried to add other structures to shell input, such as Scheme Shell and other implementations [@lispsh].
They aimed to bring S-Expression syntax to shells. Ideally to add closure property and variadic expressivness.
It also helps with metaprogramming, since it allows one to develop Domain specific languages and high order functions to abstract away certain logic.
Where they fall short is they don't solve the core issues of shells, which is they don't structure data [@shcaml].

An older attempt to address some of these problems was using filesystem abstractions to mimic object oriented principles [@oosh]. They would spawn named pipes and shell scripts to mimic sending and retrieving values and results. This ultimately missed the point since it still relies on the same data structure problem. it also requires numerous, though not busy, while loops which consumes threads.

1.2. Objective
--------------

Ultimately I want to take what has been learned and make a completely modern shell.
A shell that has the concepts of clean, true objects.
A shell that has mechanisms to structure data streams so they can be easiliy accessed using simple dot notation.
A shell that supports modern data structures like hashmaps and structured documents like JSON, YAML, XML, TOML and various others.

2. Methodology
==============

Ultimately the goal is to build, not onlt a new shell, but basically an entire langauge.
To do this is a multilevel step.
In most cases its usually, build a lexical analyser, a parser which generates an abstract syntax tree and some kind of interpreter or compiler or virtual machine to execute that abstract syntax tree.

2.1. Lexical Analysis
---------------------

This is general the first step of building a new language.
The key of this step is to take strings and to add a token identifier to them.
generally errors aren't caught here, other than invalid identifier names.

2.2. Grammars (and Actions)
---------------------------

The key of this step is to take emitted tokens from the lexical analyser and to check them against a set of rules.
Depending on the parser style depends on the kind of and quality of errors.
In many cases, most users use domain specific languages like GNU bison or YACC to generate the logic behind their grammars for them.
The other ways to build a parser is to do a recursive decent parser or a functional combinators composed of parsers.

The second phase of this is to apply grammars to actions. 
Actions are basically the logic to apply when a grammer matches.
In this case, the actions could be interpreter actions or in most cases, building an abstract syntax tree.

2.3. Abstract Syntax Tree
-------------------------

For the sake of simplicity, optimizations will not take place.
This is the area where optimizers will run, such as null code path trimming.

2.4. Interpreter
----------------

Due to the dynamic nature of a shell, it only make sense that the new language be interpreted.
This is where the problem can get a bit more complex.

### 2.4.1. Planning & Implementation

General software engineering practices like diagraming should be employed to ensure a clear and concise understanding and modelling of the system.
This phase is to determine what languages I want to use to implement all of the above.

2.5. Timeline
-------------

  * 2016-10-22: Finish all grammars for the new shell language.
  * 2016-10-28: build lexical analyser, parser and generate abstract syntax tree of the language.
  * 2016-10-29: Finish presentation of above works.
  * 2016-11-04: Execution of ls command showing basic features.
  * 2016-11-18: Most features for an ls invocation.
  * 2016-11-20: presentation should be complete.
  * til 2017: polish or add more features. make it complete and finish a comphrensive write up of what I learned and what was discovered.

3. Qualifications
=================

I have a ton of experience using and writing shell scripts, both professionally and for fun.
These scripts range from generic information gathering to the extremely inane, such as a web server written using bash.
through these experiences I've come to appreciate what a shell is for and it's many shortfalls.
With my independent studies into Domain Specific Languages, I lerned a lot about the process of designing a langauge.
On numerous occasions, I've had to deal with structured data and parsing unstructured data.

More Formally, I've taken a class in compuer languages in pursuit of my undergraduate degree.
In that class I had to work with tools like flex and bison; these are common tools for making computer languages.
I also had to learn about the principles of designing context free and regular langauge grammars.
At Cigna, I had to make use of POSIX utilities, like vmstat, to monitor servers.
To make the information useful it had to be parsed into structued forms.
I also had to learn to work with tools like jq, while working; it is a tool to pull data from json documents in a shell environment.

I feel with all these experiences I am more than capable of building a simple language that will mimick most shells at the minimum.

4. Expected Outcome
===================

