# RADiQL Documentation
This repository contains the official RADiQL documentation set.

# About RADiQL and Ultra Agile

RADiQL is a toolset that combines Rapid Application Development with 
Flow-based Programming (J. Paul Morrison) and Clean Architecture
(Robert C. Martin).

RADiQL enables and promotes an ultra-agile approach to software 
development by focussing on the essencial value delivered by a software
system. Namely:

- The Data Entities used by the system
- The User Stories (or Use Cases) that manipulate Data Entities

Data Entities and User Stories/Use Cases are treated as the 
first class citizens by RADiQL. Frameworks, boiler-plate code,
database technologies, messaging technologies and user interface
technologies are treated as "bolt-on" implementation detail that 
can abstracted away. There is therefore no direct dependency on
any underlying framework and therefore far less code to write 
and test.

## Pure Data and Pure Business Logic (First Class Citizens)

Data Entities define the pure **structure** and **types** of data and can 
include a declarative specification for how that data may be validated.

On the other hand, Use Cases and User Stories define the **behaviour** 
of the system when receiving, processing or creating Data Entities. 

The pure programmatic business logic of a Use Case or User Story is described 
by an **Interactor**. Interactors implement the behaviour of the pure 
business logic (and nothing more).

Data Entities are passed between Interactors in
the form of messages. These messages contain the same structure as the 
Data Entities themselves. Furthermore, the programatic interfaces of
each Interactor are defined in terms of those same Data Entities.

Interactors implement the Interactor interface. This has one operation
named Process(), which takes no input parameters and returns no result.
Interactors are stateless and in themselves exhibit no side effects. This
means that Interactors (and thus Use Case or User Story realizations) are
easily testable.

## The Practical Fruits of Minimalism

It's important to understand the significance of this. There are no
testable method signatures. Testing is instead conducted entirely with 
input and output data in the form of messages sent to and received from 
the Interactor via asynchronous channels. 

By reducing the implementation of a system to pure data, pure business 
logic behaviour and streams of messages, tests can be defined by
data alone, without the need for mocking frameworks or for many of the 
features that come with such frameworks. This is true of 
both unit testing (where Interactors are tested individually) and
Integration testing (where Interactors are assembled into networks of
interconnected Interactors).

Furthermore, the implementation technology of one or more Interactors may
be changed entirely (from Java to Rust, let's say, or from JavaScript 
to Golang) without any need to rewrite the test code for the essential
business logic of the system. Indeed it's very straightforward to combine
Interactors implemented with different technologies in the same system
without changing the tests at all.

The fruits of minimalism are business agility and flexibility. Less code
to write means less code to test. In turn this leads to greater velocity
of the development team. The team delivers business value more quickly 
and more precisely. The business value is distilled into a limited number 
of application-specific Interactors and Data Entity data structures. These
relationships can be represented graphically. This makes the application 
far easier to understand, to evolve and to maintain.

It's important to appreciate the value of this minimalist approach. In 
essence this permits the system to be easy to understand and largely self-
documenting. Furthermore, the simplicity and rigid structure of Interactors 
and Data Entity data types lends itself to development of advanced visual 
tooling and automation of the software development process. This powers a
leap forward in development productivity and an order of magnitude reduction
in software development costs.

# RADiQL Clean Architecture (RADiQL CA)

In his book on Clean Architure ("Clean Architecture - A Craftsman's Guide to
Software Structure and Design" - Prentice Hall), Robert C. Martin 
(aka "Uncle Bob") stated:

*“the goal of software architecture is to minimize the human resources 
required to build and maintain the required system”*

The thrust of Clean Architecture is to focus on development of the core 
business logic and data that, between them, provide the fundamental value 
of a system. Clean Architecture when followed through to its logical conclusion
eliminates the dependency of this core system (the pure data and pure business 
logic behaviour) on specific technologies, user interface libraries and database 
selection. 

With Clean Architecture, components such as the database and graphical user 
interface are treated as implementation details that may change over time as 
technology evolves. For example, a relational database may be swapped out 
for a NoSQL database or a message stream with materializable views. 

RADiQL CA builds upon Clean Architecture by ensuring that Interactors are
asynchronous message-driven components that exhibit very low coupling to 
other Interactors. In RADiQL CA there are no method signatures present 
that would permit two Interactors to know about each other. Instead they are
connected by the application designer using message-based channels where 
output port of the sending Interactor uses exactly the same message type as 
the input port of the receiving Interactor.

This means, in effect, that both Interactors are forced to implement their
interfaces by referencing a common message data type, thereby guaranteeing
their compatibility. This makes it easy to "wire up" Interactor components.

# Flow-based Programming (FBP) with RADiQL

A defining characteristic of FBP is that it placed data structure of messages
at the heart of the system. FBP is used to wire FBP components together in a
network of data flows. Data flows are implemented with messages which, in FBP 
terminology, are referred to as Information Packets (or IPs). IP, in this 
context, should not be confused with "Internet Protocol" as used in "IP address".
They're very different things!

IPs permit substreams of messages within another stream of messages. Or messages 
may be passed between FBP components in data structures known as "IP trees". 
Furthermore, FBP components may be decomposed into a subnet of FBP components.
These may be "lower level" components but are not necessarily "lower level". They
could, for example, be a proxy for remote FBP components in a distributed system.

It's important to understand that, in principal, FBP components may run in the
same address space (the same executable binary) or be executed as part of a 
remote process in a different address space (a different executable binary not
necessarily running on the same physical computer, in the same data centre, 
on the same continent or even on the same planet).

RADiQL CA supports all of these features. This permits and promotes rapid 
prototyping and evolution of production-quality FBP components as part of a 
Rapid Application Development (RAD) or Joint Application Development(JAD)
process.

# Programming Automation

Although not a prerequisite, RADiQL is compatible with template-based 
code generation features of programming languages such as Go (Golang). Indeed,
as is the case with Go (at least version 1.x) where there is no support for
Generics, go:generate is the usual means of achieving the same end. In other
words using Generic templates to implement application type-specific data structures
that exibit Generic data structure properties and behaviour.

Although many may frown on "code generation" in practice it's used everywhere
under the covers, from generation of gRPC service and message stubs to 
optimised database access. The use of code generation is often used to avoid 
the runtime performance hit of techniques such as type reflection, where the data
type of a data structure or class is examined to determine what to do next.
Many languages are transpiled into JavaScript (which basically means
code generation, in effect) including later versions of JavaScript that are not
yet supported by the Browser or NodeJS.

Although Programming Automation and code generation, if not done properly, 
can result in a large, clunky, machine-generated codebase, when done properly 
it can produce higher quality and more consistent code than most human 
developers will be capable of producing. This is especially true of boilerplate 
code, where human developers are notorious for getting bored and making mistakes 
or taking shortcuts. And since we've mentioned short cuts, IDEs and advanced
text editors automate programming tasks all the time with autocomplete
and code template features. Code generation is no different and comes with 
the same benefits and drawbacks.

Code Generation should be seen as a productivity-enhancing automation step
for highly-repetitive and well-understood programming tasks. It's robotic
execution of well-defined tasks, in exactly the same way that a robot 
will spot-weld the body panels of a vehicle in an automobile factory. When used
appropriately, it produces a higher quality result that's far cheaper and faster
than hand-coding.

RADiQL does not currently use code generation to define Entity Data types
nor application-specific Interactors. However, AppStratum's own implemention 
of RADiQL (called
Harmony) does automatically generate (and if necessary remove) 
code for Composite Interactors in response to design choices made by a 
human software designer. This level of automation greatly reduces the 
amount of work that is required to develop and test software built
using RADiQL.

Finally it's worth mentioning that Appstratum Harmony uses Machine Learning (ML) 
and Artificial Intelligence (AI) to augment productivity of software designers
and software developers and to optimise and adaptively tune the performance of
software sytems built with RADiQL.

# Summary of the Benefits of RADiQL

RADiQL provides a toolset that promotes rapid development of functionally
complete production quality software systems with the following characteristics:

- a greatly reduced development effort
- significantly reduced development costs
- significantly quicker time to market
- substantially reduced financial risks
- greater code reuse and thus higher returns on investment
- a substantially lower level of defects
- lower application deployment and hosting costs
- substantially lower maintenance costs
- better runtime performance on modern multi-core CPU architectures
- a small memory footprint
- cross-platform implementations

Furthermore, the adoption of RADiQL ensures:

- high availability
- high reliability
- high maintainability
- high scalability
- high extensiblity
- high portability
- high flexibility
- high levels of security

RADiQL is designed for easy deployment into a cloud using Docker, Kubernetes 
and a distributed data centre operating system such as Mesosphere DC/OS.



