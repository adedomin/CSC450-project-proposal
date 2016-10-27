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

1. Background
=============

1.1 Related Works
-----------------

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

1.2 Process
-----------
