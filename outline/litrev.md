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

1.1 Related Works
-----------------

Object Oriented shells isn't an etirely new concept.
As others have shown, many projects, some more serious than others, attempted to solve this issue [@shcaml] [@oosh].

The power of shells is well understood.
Most programming languages have some kind of system() or shell invocation mechanism.
Some, such as the developers of shcaml attempted to take it further by including functional combinators;
these combinators allowed for slipping in native ocaml code and objects.
As a result these code pieces could be parsers, that could take known shell commands, and structure their data into key-value trees [@shcaml].

Purely object oriented attempts ultimately result in new instances of bash and explicit message passing with named pipes [@oosh].


1.1 SOA
-------

Service Oriented Architectures, or SOA, are the modern way to construct, highly available, data rich web applications.
In short, a service oriented architecture is a way for applications to share state and provide services over middleware and structured, serialized objects.
[@understandsoa]
One way of transacting states between services is through Representational state transfer, or REST.
With REST, services are able to share well structured data through document structures like JSON, XML, etc. [@semanticrest]

Currently popular shells have no built-in feature complete way of transacting or using structured documents.
As a result, working with web oriented services becomes a hassle;
A hassle that involves very long and contrived text pipelines full of tools like: sed, grep, awk, xargs, tr, paste, cut, tee, and so on.
What results is some sort of string tokenized parser.

In order to unify the web and systems management, tools like ansible were created.
Ansible, ends up using a general purpose language like python which can natively handle these structures.
Projects like powershell are built on the .NET runtime and can thus utilize class like features and functions.
The streaming pipelines in Powershell are merely .NET classes which allow for some structural correctness and parsing [@monadshell].
As a result, Microsoft prefers to call more than just a shell, but a whole "automation and configuration management framework."
One that is capable of handling structured data such as JSON, XML, CSV, etc, REST APIs, and object models.
As a result, the conventional UNIX shell is becoming marginalized by various general purpose languages and domain specific languages.

1.2 Process
-----------
