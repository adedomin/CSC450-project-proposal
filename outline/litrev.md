---
# Copyright (C) 2016  Anthony DeDominic
#
# Permission is granted to copy, distribute and/or modify this document
# under the terms of the GNU Free Documentation License, Version 1.3
# or any later version published by the Free Software Foundation;
# with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
# A copy of the license is included in the section entitled "GNU
# Free Documentation License".
---

1. Introduction
===============

Currently popular shells have no built-in feature complete way of transacting or using structured documents.
As a result, working with web oriented services becomes a hassle;
A hassle that involves very long and contrived text pipelines full of tools like: sed, grep, awk, xargs, tr, paste, cut, tee, and so on.
What results is some sort of string tokenized parser.
An example of the problem can be seen below.

```sh
# snippet from https://github.com/GeneralUnRest/neo8ball-irc/blob/master/lib/search.sh
# gets an html webpage from duckduckgo, processes it into "url - page description" lines 
# removes ad links
# and only preserves the first three
RES=$( curl "${SEARCH_ENGINE}$(rawurlencode "${4}")" 2>/dev/null | \
    html2 2>/dev/null | \
    grep -A 2 "@class=result__a" | \
    sed '/^--$/d' | \
    sed '/@class/d' | \
    grep -Po '(?<=\/a(=|\/)).*' | \
    paste -d " " - - | \
    sed 's/\(@href\|b\)=//g' | \
    sed '/r\.search\.yahoo\.com/d' | \
    head -n 3 )
```

1.1. Related Works
------------------

Object Oriented shells isn't an etirely new concept.
As others have shown, many projects, some more serious than others, attempted to solve this issue [@shcaml] [@oosh].

The power of shells is well understood.
Most programming languages have some kind of system() or shell invocation mechanism.
Some, such as the developers of shcaml attempted to take it further by including functional combinators;
these combinators allowed for slipping in native ocaml code and objects.
As a result these code pieces could be parsers, that could take known shell commands, and structure their data into key-value trees [@shcaml].

Purely object oriented attempts ultimately result in new instances of bash and explicit message passing with named pipes [@oosh].
Enen though offers powerful object-like abstractions it general comes with significant overhead.
It also incurs security risks since processes can write and listen to the object named pipes.

Projects like powershell are built on the .NET runtime and can thus utilize class like features and functions.
The streaming pipelines in Powershell are merely .NET classes which allow for some structural correctness and parsing [@shcaml][@monadshell].
As a result, Microsoft prefers to call more than just a shell, but a whole "automation and configuration management framework."
One that is capable of handling structured data such as JSON, XML, CSV, etc, REST APIs, and object models.

Tools like Ansible, aren't quite shells, but are domain specific languages which solve similar problems.
Ansible, et al, use code generation and a yaml playbook file to construct python code;
since python is a general purpose language, it handles structured and typed data much better than shell code.
As a result, powerful modules for system administration, configuration and interaction with web services have made it a formiddable automation tool.

1.1. Service-oriented Architecture
----------------------------------

Service-oriented Architectures, or SOA, are modern way to construct, highly available, data rich web applications.
In short, a service oriented architecture is a way for applications to share state and provide services over middleware and structured, serialized objects.
[@soa]
One way of transacting states between services is through Representational state transfer, or REST.
With REST, services are able to share well structured data through document structures like JSON, XML, etc. [@semanticrest]

POSIX-shells are completely out of this domain because of their limitations.
Generally when dealing with web apis it's recommended to build a general purpose language script instead.
is is simply because it's difficult to work with the structured web content.

1.2. Designing and Defining a Domain Specific Language
------------------------------------------------------


1.3. Events
-----------

