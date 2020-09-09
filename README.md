# RADiQL Documentation
This repository contains the official RADiQL documentation set.

# RADiQL Objectives

The primary goal of the RADiQL approach is to maximise the delivery of
business and organisational value with minimal effort and resources.

The mantra of RADiQL is: *"Minimal Output, Maximum Outcomes"* (MOMO).

In practice this means:

- rapid delivery of working software with minimal human involvement.
This minimises defects, costs, unnecessary testing and time to market.
- maximimal reuse of high quality software componentry (either open 
source or closed source)
- knowledge capture and retention for continual future reuse and
evolution
- no hard-wired dependencies on any particular technology
- all software can be recreated cheaply as new technology, frameworks
and platforms come to market.


# About RADiQL and Ultra Agile

RADiQL is a conceptual framework that combines the following:

- [Rapid Application Development](https://en.wikipedia.org/wiki/Rapid_application_development)
- [Communicating Sequential Processes (Tony Hoare et al)](https://en.wikipedia.org/wiki/Communicating_sequential_processes)
- [Flow-based Programming (J. Paul Morrison)](https://jpaulm.github.io/fbp/)
- [Clean Architecture (Robert C. Martin)](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Domain-driven Design (Eric Evans)](https://en.wikipedia.org/wiki/Domain-driven_design)
- [Data Centric Design (Dave McComb)](http://www.brcommunity.com/articles.php?id=b972)
- [Hypothesis-driven Delivery and Lean UX (Jeff Gothelf)](https://www.interaction-design.org/literature/article/a-simple-introduction-to-lean-ux)
- [Impact Mapping - Gojko Adzic](https://www.impactmapping.org/)
- [Normalized Systems Theory (NST - Herwig Mannaert, Jan Verelst, Peter De Bruyn)](https://ieeexplore.ieee.org/abstract/document/6759187/references#references)

Other Influences include: 

- concepts from Model-driven Design using Business Patterns (Pavel Hruby)
- concepts from Ontology-based Domain Driven Design (Pavel Hruby)
- User Research

In other words, RADiQL draws together the fruits of decades of 
knowledge, experience and wisdom in the field of designing complex
information systems into a conceptual framework that underpins a
simple, practical, ultra-agile approach to building such systems 
via knowledge capture in ontologies, user stories and use cases, 
collaborative working and extensive automation.

## How RADiQL differs from conventional Agile

Conventional Agile software development (at least as it's usually practiced)
splits work on larger enterprise across multiple software development teams.
Each team focusses on delivery of the epics and stories that are its 
responsibility to deliver. Although there may be (and usually is) communication
between teams - including through meetings such as a "scrum of scrums" - there
is a tendency for most members of the team to lose sight of the "bigger picture".
They're focussed on the lower level artefacts that their own team is to deliver
from stories, sub-stories and individual tasks. Building the potential for
easy reuse rarely figures in this process. The objective is simply to write
the minimum amount of code to meet the requirement of the current story at
hand and no more than that.

RADiQL starts from a different perspective: an overall enterprise business
model and creating descriptions of how everything within the context of the
business (or organisation) is related to each other and how these things
interact. Knowledge capture and retention in a codified and expressive form
is key to the way that RADiQL works.

Conventional Agile software development tends to involve human programmers 
and testers writing a great deal of code and a there's typically a heavy 
emphasis on test-driven development or behaviour-driven development. This 
is necessary because the "requirements" of the system are expressed loosely
in user stories (or use cases) and its necessary to codify the requirements
in the form of test cases.

RADiQL, on the other hand, starts from knowledge being captured in the form
of ontologies. Some of these ontologies capture knowledge about the outside 
world. Some of these ontologies - high level enterprise ontologies - capture 
more abstract knowledge about the business or organisation and the way it works. 
Story ontologies capture more detail and  knowledge about how to map these 
more abstract business and real-world concepts into a network of collaborative 
nanoservices that actually implement software functionality and build system tasks. 
Nanoservices are lower level reusable story component implementations that 
are described by their own ontologies. This is a layered higherarchy of
ontologies where the lower level "detailed" ontologies reference and import 
concepts from the higher level "abstract" ontologies.

This approach - which embodies reusability right at its core - vastly reduces 
the need for hand-crafted code and the necessary testing, debugging and maintenance 
that goes along with it. So while TDD and BDD are both practiced within a 
RADiQL environment, they are necessary only when and where new nanoservice 
components need to be created.

Typically, therefore, between 70 and 95% of code is reused from one RADiQL 
project to the next. Automated assembly of nanoservice components greatly
reduces risk and project costs while greatly enhancing software quality
when compared with conventional Agile software development, where software
development by human members of the team plays such an important and central
role.

RADiQL takes an industrial approach to manufacturing software systems from 
an extensive knowledge base (and publicly available research and software
implementation strategies expressed in ontologies) rather than relying on 
the work of (hopefully) skilled artesan programmers to write inevitably
more defect-prone software from scratch.

## How RADiQL differs from conventional RAD

Critisims of conventional Rapid Application Development often include:

- The risk of a new approach and new tools
- Lack of emphasis on non-functional requirements due to lack of visibility
during development
- Requires time of subject matter experts who may be scarce due to the 
need for them to be available to deal with day-to-day business responsibilities.
This may be more serious if general purpose developers with little or no domain
knowledge are trying to interact (and consume the valuable time of) the subject
matter expert.
- Less control of and discipline during the development process. The flexiblity 
of a RAD approach may prove costly in terms of the technical debt it may incur 
and the lack of adherence to standards. RAD has often been used in so-called
"End User Computing" teams to "knock up" quick apps for business users that
effectively become "throw-away" software due to their lack of engineering and
future-proofing.
- Poor design due to solutions being quickly prototyped and "hacked together"
as quickliy as possible.
- Lack of scalability due to non-functional requirements being ignored and/or
the limited scope of the software and the difficulty of expanding its functionality.
Many RAD application tools were designed for 2 tier client-server computing or
3 tier application server computing with a thick client (a desktop application,
for example). These types of application tend not to scale well, in practice, 
for a number of reasons and often incur significant maintenance costs going
forward.

RADiQL uses exisisting tools and technologies that have been around for over 
a decade in production use. These are used in systems such as those at the
very core of Google's search services, the most used and reliable services 
in the world today.

RADiQL places a heavy emphasis on knowledge capture and, more importantly, 
re-use of knowledge. Ontologies already exist for many vertical markets and
academic, professional and economic disciplines. There is, therefore, probably an
ontology out there that already captures much or most of the knowledge required
to build an application. Organisation-specific ontologies only need to add
organisation-specific knowledge to the more generic vertical market ontologies
that they reference. In other words, the organisation-specific customisations
that override or enhance a generic ontology for the organisation's specific 
purposes. Reuse of the knowledge that has already been captured in ontologies
greatly reduces the pressure to take valuable time from subject matter experts.
Furthermore, knowledge that is gathered from such subject matter experts is
immediately codified into an enterprise business ontology for reuse in the 
future.

RADiQL places great emphasis on control during the development process, but 
uses a type of Artificial Intelligence  in the form of automated reasoning 
to verify the consistency and correctness of the enterprise business model 
and capture of business rules in a precise, progressively more detailed, form.
The emphasis of RADiQL is on rapidly establishing and capturing 
the enterprise business model (reusing generic knowledge from existing
knowledge repositories) and generating visual artefacts from this rather than
prototyping user interfaces. RADiQL puts the correctness of data at the heart
of its activities and treats user interface technology as a plugin framework
in accordance with Clean Architecture principles. Furthermore, Machine Learning
(ML) can be applied to enhance productivity and reusability as part of this 
process of mapping high-level business concepts to deliverable software as
well as delivering excellent solutions to non-functional requirements.

RADiQL is implemented with a Clean Architecture and Story-based (or Use Case
based) Interactors (that are implemented as well-defined and self-documenting 
composite nanoservices. There is nothing "hacked together" in this process.
People work hand in hand with automated reasoners to ensure that the software
is well designed, of high quality and of lasting value.

With RADiQL, speed comes from automated re-use of knowledge captured in 
knowledge respositories (external and internal) rather than quick "hacks"
and a quick-but-shoddy "slap-dash" prototyping. Velocity is achieved through
automation rather than by taking cheap-but-nasty shortcuts.

With regard to scalability, RADiQL nanoservices are designed to be 
deployable into scalable microservices that can be replicated at web 
scale in the cloud. Furthermore, the baked-in support for the flow-based
programming paradigm means that concurrent processing support is of the
highest order, permitting full exploitation of the parallel processing 
capabilities of the latest generation of multi-core CPUs. The principles of
Communicating sequential processing (CSP) and Flow-based programming (FBP)
is the bedrock on which nanoservices are based.

## Delivery of Essential Value

RADiQL enables and promotes an ultra-agile approach to software 
development by focussing on the essencial value delivered by a software
system. Namely:

- timeless yet evolving models of business and organisational knowledge
that are of lasting value and that are used to automate software delivery
with little or no further human involvement
- cheap and rapid experimentation to incrementally and continuously 
deliver new value rapidly, at low risk and at low cost
- a shared vocabulary that can be used to drastically lower integration
costs and maximise business and organisational agility.

Domain Entities (Things) and User Stories/Use Cases (Processes) are 
treated as the  first class citizens by RADiQL. Frameworks, boiler-plate code,
database technologies, messaging technologies and user interface
technologies are treated as "bolt-on" implementation detail that 
can be abstracted away. There is therefore no direct dependency on
any underlying software framework and therefore far less code to write 
and test.

RADiQL accelerates the process of understanding, designing and building
domain-driven lo-code / no-code software through automation based
upon publicly-available ontologies that define domains of interest.
In other words, much of the data model that a system will use may
already have been analysed and built by third parties and formalised
into an ontology. An application or service designer can reuse and
leverage this knowledge and easily augment it or customise it to create
software without starting from scratch.

A software designer can rapidly pick and choose domain entities and
attributes of interest from ontologies for a particular vertical 
market or area of academic or professional expertise.
RADiQL can also leverage custom domain models that may or may not 
reference publicly-available ontologies.

## Clean Architecture

Note that Clean Architecture implicitly focusses on how best to 
cost-effectively deliver the essential value provided by a system with
minimal human resources. RADiQL uses and reuses ontologies 
and data models to concentrate effort on rapid delivery of essential 
value without getting lost in the implementation-specific details 
of programming languages, software architectures, user interface 
technologies or data-persistence technologies. Essential value
is a timeless concept, where as the implementation-specific details
and technologies will change over time.

Ontologies are frequently used in automation. RADiQL uses ontologies
to automate requirements capture, software specification via user 
stories, test case specification, documentation and software delivery.
RADiQL accelarates software delivery by reusing knowledge about 
domain entities, including actions performed on or by these
domain entities and the transformations of data that are involved.

RADiQL reuses timeless knowledge about what software does and solutions for 
achieving these design goals in order to build reusable software rapidly. 
RADiQL doesn't obsess about language-specific implementation or 
frameworks since these languages and frameworks come and go or 
limit future/backwards compatibility and therefore, by implication, 
deliver limited lasting and fundamental value. 

In any case,
virtualisation, containerization, service-oriented architecture and
microservice architectures change how we think about implementing,
building and integrating software with different programming languages,
platforms, frameworks and deployment models. More and more we're
being forced to consider functionality and the data model as more 
important than the underlying implementation technology selected
to realise software components. RADiQL merely focusses on meeting
these new challenges better than traditional tools that, by 
necessity, require far more human involvement and expense, both in 
terms of time, money and lost opportunity.

## No Source Code

RADiQL itself doesn't depend on any particular programming language,
operating system or database product. Software may be implemented in
any language, in whatever framework and on whatever operating system.

RADiQL concepts are defined in an abstract form using the non-proprietary
and fully open source [Resource Description Framework (RDF)](https://www.w3.org/RDF/)
and related semantic web technologies. These include:

- [RDF Schema (RDFS)](https://www.w3.org/TR/rdf-schema/)
- [Web Ontology Language (OWL)](https://www.w3.org/OWL/)
- [SPARQL 1.1 Query Langauge](https://www.w3.org/TR/sparql11-query/)
and 
- [Shapes Constraint Language (SHACL)](https://www.w3.org/TR/shacl/)


## Pure Data and Pure Business Logic (First Class Citizens)

Data Entities define the pure **structure** and **types** of data and can 
include a declarative specification for how that data may be validated.

On the other hand, Use Cases and User Stories define the **behaviour** 
of the system when receiving, processing or creating Data Entities. 

The pure programmatic business logic of a Use Case or User Story is described 
by a story **Interactor**. Interactors implement the behaviour of the pure 
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

Interactors are packaged as Nanoservices. More complicated and significant 
Story Interactors are almost always packaged as Composite Nanoservices: 
Nanoservices than are implemented with other low-level Nanoservices.

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
Interactors (or compare!) implemented with different technologies in the 
same system without changing the tests at all.

The fruits of minimalism are business agility and flexibility. Less code
to write means less code to test. In turn this leads to greater velocity
of the development team. The team delivers business value more quickly 
and more precisely. The business value is distilled into a limited number 
of application-specific Story Interactors and Data Entity data structures. 
These relationships can be represented graphically. This makes the application 
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

In RADiQL, message types are derived from definitions of classes (types of
Thing) in ontologies. Ontologies support a very flexible and extensive
class hierarchy that permits individual Things to be treated differently in
a different context. The object properties and data properties of each Thing
are formally defined by an ontology and may be further refined and detailed
by lower-level ontologies. The expressive ontology-based type system permits
RADiQL tools to compute how message types can be infered in a given context.
More importantly, deriving message types from an ontology permits RADiQL 
tool to match and connect resuable Nanoservices, automatically creating
interfaces and creating and injecting message type adapters between
Nanoservices where necessary.

This means, in effect, that both Interactors are forced to implement their
interfaces by referencing a common message data type or at least a compatible message
type, thereby guaranteeing their compatibility. This, along with the automated
support of creating and injecting message type adapters, makes it easy to 
"wire up" Interactor components in an automated fashion.

# Flow-based Programming (FBP) with RADiQL

A defining characteristic of FBP is that it places data structure of messages
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

# Graphical and Visual Tools

A key aim of FBP was to enable applications and components to be defined 
with either a simple FBP configuration file (or set of files) or using a
diagramming tool to generate such a file. The FBP configuration file would 
be easy to convert back into graph or a diagram. The FBP application would,
therefore, be self-documenting.

Many developers are suspicious of visual tools because they are perceived to
"mask" what the code is doing. Developers often want to see an underlying
text file "in the flesh". Now this sort of skepticism about visual tools is
understandable in conventional programming because certain ideas can in many
cases be expressed very concisely in mathematical notation or in code in
a suitable programming language. However, with Flow-based Programming this
skepticism is somewhat misplaced.

FBP permits developers to flip between a visual graphical view of an application
and code, depending on which view of the system is more natural and thus, more
productive.

## Nanoservices

Functionality in RADiQL is implemented in the form of Nanoservices. Nanoservices
implement features, tasks or processes and can be packaged individually or 
collectively as microservices or monolithic executable applications as desired.
Nanoservices may be colocated in the same microservice or monolithic application
or distributed across multiple microservices or applications, as non-functional
requirements dictate.

Nanoservices may be defined in any language and are designed to permit integration
into a flow-based programming network. They can be open source, closed source, 
commercial offerings or free to use.

Metadata for nanoservices is defined using the RADiQL nanoservice ontology. This 
is open source and free to use, including for commercial use. 

Nanoservices described using the RADiQL nanoservice ontology are automatically 
discoverable by RADiQL tools and services. They can be used as components in
authoring tools and automatically discovered, assembled and built into an
executable for deployment.

## Creating nanoservice components with a text editor

RADiQL encourages the use of a text editor when writing an application-specific
Interactor in a suitable programming language. The suitability of the language 
will depend on the context or purpose of the Interactor in question. However, 
Interactor implementations should be small, easily understood and re-usable 
wherever possible.

Interactors have well-defined input and output interfaces and can, therefore, 
easily be turned into a self-documenting component that can be configured, 
manipulated and assembled into an application or another higher level 
component. 

The original developer of a custom application-specific component will write
the component using a conventional programming language such as JavaScript, 
Rust, Go, Java or Kotlin. However, another developer may use incorporate this
component into another application using a visual tool. A business analyst may
adjust configuration parameters of such a component without need to reference
the original developer's code at all. 

RADiQL makes it easy to reuse components and to combine or re-combine them 
in different ways with a visual tool or a text editor. For the most part, though
the visual tool is more convenient when assembling applications our of 
existing Interactor components because it includes built in support for checking
the compatibility of interfaces, automatically running unit and integration tests
and developing test scripts.

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

Free Downloadable Tools

AppStratum provides a useful extension for Visual Studio Code to help develop and test RADiQL software components in the Rust programming language.

# Implementations of RADiQL

A commercial implementation of RADiQL is provided by AppStratum Harmony. Harmony provides the following services to users of the RADiQL approach:

- A one-stop shop for fully versioned knowledge capture, information modelling and business rules definition
- A one-stop shop for building and deploying RADiQL applications in the Cloud
- An app store for business and government applications
- Managed graph database services
- Integration with GitHub 
- Integration with Atlassian Cloud

AppStratum Harmony is implemented in the Rust programming language and is designed to fully exploit the latest generation of multicore CPUs from Intel and AMD.





