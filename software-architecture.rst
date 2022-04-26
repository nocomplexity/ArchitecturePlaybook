Software Architecture
======================

Architecture SHOULD be simple and have a clear purpose. Good software architecture methods are hard to find.
Often it is too high level (TOGAF based with archimate diagrams). Often with no or very little value for software developers and managers. Or software architecture diagrams are a random collection of code-snippets and UML diagrams. Often only created since creating documentation was requested. 

When you create an application, its architecture must do two things:

-    Provide an easy way to communicate to **ALL** stakeholders.

-    Enable various stakeholders to see different levels of granularity.

- Make sure that even you understand the working and key dependencies a few years later!


The C4 model for visualising software architecture
----------------------------------------------------

C4 stands for context, containers, components, and code . It is a great way to create a good software architecture. And it is an open method. A full training can be found on: https://s3.amazonaws.com/static.codingthearchitecture.com/presentations/bcsspa2019-the-lost-art-of-software-design.pdf 

The C4 model was created as a way to help software development teams describe and communicate software architecture, both during up-front design sessions and when retrospectively documenting an existing codebase. It's a way to create maps of your code, at various levels of detail, in the same way you would use something like Google Maps to zoom in and out of an area you are interested in. 

By using the C4 model for software architecture, you can capture just enough architecture to communicate to stakeholders and enable team understanding without having to define details that will change as your architecture changes.

Source and more info on: https://c4model.com/ 

arc42 software architectures
-----------------------------

- arc42 is based on practical experience of many systems in various domains, from information and web systems, real-time and embedded to business intelligence and data warehouses.

- arc42 provides a template for documentation and communication of software and system architectures.

- arc42 supports arbitrary technologies and tools.

- arc42 is completely process-agnostic, and especially well-suited for lean and agile development approaches.

- arc42 is open-source and can be used free of charge, in commercial and private situations. 

All arc42 templates can be found on: https://github.com/arc42/arc42-template Or check the arc42 download page on: https://arc42.org/download 


The Bounded Context Canvas
---------------------------

Great FOSS tool that helps with your software design. Source code and instruction on:
https://github.com/ddd-crew/bounded-context-canvas 

The Bounded Context Canvas is a collaborative tool for designing and documenting the design of a single bounded context.

A bounded context is a sub-system in a software architecture aligned to a part of your domain.

The canvas guides you through the process of designing a bounded context by requiring you to consider and make choices about the key elements of its design, from naming to responsibilities, to its public interface and dependencies.

Systemizer
---------------

Systemizer is a system design tool used to create and simulate large scale distributed systems. 

Landing page: https://honzaap.github.io/Systemizer/


Repository on github: https://github.com/honzaap/Systemizer