# SAD Template

## Executive summary 

This template can be used as reference for your own solution
architecture document.

You can download this template in MSWord, OpenOffice or as markdown.

But instead of using this static template I recommend our tool to
generate 80% (or more) of the document automatic.

Steps to complete:

Define your principles for your architecture/design

Define or gather your requirements

Make use of our collection of pre-defined solution building blocks
(SBB’s) and refer to the default description instead of repeating
trival information in your architecture document. In this way you can
keep your document clean and mean.

This is very easy:

  - Use our pre-defined

Contents

[Executive summary ii](#executive-summary)

[1 Introduction 4](#introduction)

[1.1 Terms Used in This Standard 4](#terms-used-in-this-standard)

[1.2 Scope 4](#scope)

[2 Goals and Context 6](#goals-and-context)

[2.1.1 Significant Driving Requirements
6](#significant-driving-requirements)

[2.2 Solution Background 6](#solution-background)

[2.2.1 Architectural Approaches 7](#architectural-approaches)

[2.2.2 Analysis Results 7](#analysis-results)

[2.2.3 Requirements Coverage 7](#requirements-coverage)

[2.2.4 Summary of Changes in Current Version
7](#summary-of-changes-in-current-version)

[2.2.5 Product Line Reuse Considerations
7](#product-line-reuse-considerations)

[3 Views 7](#views)

[4 Relations Among Views 8](#relations-among-views)

[4.1 General Relations Among Views 9](#general-relations-among-views)

[4.2 View-to-View Relations 9](#view-to-view-relations)

[5 Referenced Materials 9](#referenced-materials)

[6 Glossary and acronyms 9](#glossary-and-acronyms)

[7 Appendixes 9](#appendixes)

## Introduction 

General introduction of the project.

Tip: Make sure this document can be read and reviewed without reading
all reference documentation. E.g. Programme architecture, project plan,
business case etc.

The right software architecture is essential for a software-intensive
system to meet its

behavioral (functional) requirements as well as its quality requirements
that govern real-time performance, security, reliability,
maintainability, and a host of other quality attributes.

Software architecture is especially critical in large, complex systems
because software is a major contributor to the cost and quality of such
systems and to the schedule and risk of acquiring them.

Documenting the architecture effectively is as important as crafting it
because the

documentation is how the architecture is communicated to its many
stakeholders. An

architecture that is not communicated clearly, completely, and
unambiguously to developers, downstream designers, testers, analysts,
certification authorities, and other key practitioners is nearly useless
and will require a multitude of architects to constantly and repeatedly
explain themselves. In a very short time—let alone over a long-lived
system’s expected operational lifetime—the architecture will lose all
integrity

### Terms Used in This Standard

Document means a collection of data regardless of its medium or the
number of volumes

it consists of. Use of electronic data is encouraged.

A viewpoint is a pattern or template that specifies the conventions for
constructing and

using a view. It is created after three things have been determined: (1)
the view’s

purpose, (2) the view’s audience, and (3) how the view will be created
and analyzed. Once created, viewpoints are used to develop multiple
individual views.

A view is a representation of a whole system from the perspective of a
related set of

Concerns.

A view is described by the types of elements and relations that it

contains, as well as any constraints on their interaction. A view
conforms to a viewpoint.

A view packet specifies a portion of the system in a view. It is the
smallest bundle of

useful documentation that can be given to a stakeholder \[Clements 02\].
View packets

usually show large areas of the system at shallow depth or small areas
of the system at

great depth.

### Scope 

1\. Documentation Roadmap and Overview

In this section, provide information that will help readers of the SAD
find the information they

need quickly. Structure the information in the sections listed below.

1.1 Document Management and Configuration Control Information

Identify the version, release date, and other relevant management and

configuration control information associated with the current version of
the

document. Optional: Include a change history, highlighting significant
changes

from version to version.

1.2 Purpose and Scope of the SAD

Explain the SAD’s overall purpose and scope. Explain the criteria for
deciding

which design decisions are architectural (and therefore documented in
the SAD)

and which are non-architectural (and therefore documented elsewhere).

1.3 How the SAD Is Organized

Provide a narrative description and overall contents of the seven major
sections of

the SAD (as identified by this reference standard).

1.4 Stakeholder Representation

1.4.1 Stakeholders and Their Concerns

Provide a list of the stakeholder roles considered in the development of
the

architecture described by this SAD. For each role, list the stakeholder

concerns that can be addressed by the information in this SAD. A

convenient way to represent this information is as a matrix, where the
rows

list stakeholder roles, the columns list concerns, and the cells
indicate how

serious the concern is to a stakeholder in that role. The following

stakeholders shall be considered at a minimum:

  - application software developers

  - infrastructure software developers

  - end users

  - application and platform hardware engineers

  - security engineers and certifiers

  - safety engineers and certifiers

  - communications engineers

  - system-of-system engineers

  - chief engineer/chief scientist

  - lead system integrator (LSI) program management

  - government program management (including those concerned with

  - licensing)

  - system integration and test engineers

  - external test agencies

  - operational system managers

  - trainers

  - maintainers

  - other service representatives

  - auditors (LSI internal, the Government Accounting Office, etc.)

  - representatives of standardization activities

1.4.2 Stakeholder Scenarios for Using the SAD

For each role identified in Section 1.4.1, write a few short scenarios
that

explain how stakeholders in that role would use specific sections of the
SAD

to help address their concerns.

1.5 Viewpoint and View Definitions

Introduction to Viewpoints. Define the term viewpoint and describe how
it’s

used in this SAD.

Describe each viewpoint used in the SAD as outlined in Section 1.5.i.
The

following viewpoints must be included:

Communications viewpoint. Views conforming to this viewpoint show the
communication paths used by software-initiated or software carried
messages and the software elements that send and receive information
along those paths. Views conforming to this viewpoint

provide the basis for analysis for determining whether necessary
communication bandwidth and performance will be achieved, thus enabling
the system to meet its operational requirements that depend on
communication.

Data load viewpoint. Views conforming to this viewpoint show the

data required and provided by software elements and show where

that data is stored and how it is backed up and recovered in the

event of loss. Views conforming to this viewpoint provide the basis

for analysis for determining whether units will have access to the

necessary information.

Information assurance viewpoint. Views conforming to this viewpoint show
the location and flow of classified or otherwise sensitive information
in the system, as well as elements that provide essential

services that must be protected from denial-of-service attacks.

Views conforming to this viewpoint provide the basis for analysis for

determining whether the system’s information-assurance needs will

be met.

safety viewpoint. Views conforming to this viewpoint show elements

that provide safety-critical functionality and how they are used.

reliability viewpoint. Views conforming to this viewpoint show

elements that provide mission-critical functionality, how they are

used, and any redundancy or failover capabilities provided to

assume that functionality in the event of failure. Views conforming to

this viewpoint provide the basis for analysis for determining whether

the system’s reliability needs will be satisfied.

## Goals and Context 

Describe the goals and major contextual factors for the software
architecture. Include

a description of the role software architecture plays in the life cycle,
relevant acquisition

factors, the impact of the LSI model, the effects of incremental
development, and the

relationship to system engineering results and artifacts.

#### Significant Driving Requirements 

Describe behavioural and quality attribute requirements (original or
derived) that shaped

the software architecture. Include any scenarios that express driving
behavioural and

quality attribute goals, such as those crafted during an ATAM evaluation
\[Clements

01\].

### Solution Background 

In this section, provide a description of why the architecture is the
way it is and why it is

appropriate for satisfying the functional and quality attribute goals
levied upon it. Structure the

information in the following sections:

#### Architectural Approaches 

Provide a rationale for the major design decisions embodied by the
software

architecture. Describe any design approaches applied to the software
architecture—

including the use of architectural styles or design patterns—when the
scope of those

approaches transcends any single architectural view. Explain why those
approaches

were chosen and specifically why they were chosen over other seriously
considered

approaches. Describe any relevant issues dealing with commercial
off-the-shelf

(COTS) or government off-the-shelf (GOTS) components, including any
associated

trade spaces.

#### Analysis Results 

Describe the results of any quantitative or qualitative analyses that
have proven the

software architecture is fit for purpose. If an architecture evaluation
has been

performed using the ATAM or a comparable method, include the analysis
sections of

the final evaluation report. Refer to the results of any other relevant
trade studies,

quantitative modeling, or other analysis results.

#### Requirements Coverage 

Describe the requirements (original or derived) addressed by the
software architecture.

Include those requirements or constraints that are derived from higher
level SADs.

#### Summary of Changes in Current Version 

For versions of the SAD after the original release, summarize the
actions; the

decisions and decision drivers; the requirements changes and analysis
and trade

study results that became decision drivers; and explain how these
decisions caused

the architecture to evolve or change.

#### Product Line Reuse Considerations 

When a product line is being developed, this section details how the
software covered by this SAD is planned or expected to be reused in
order to support the product line vision. In particular, this section
includes a complete list of the variations that are planned to be

produced and supported. Variation refers to a variant of the software
produced through the use of pre-planned variation mechanisms made
available in the software architecture.

Variation may refer to a variant of a module or a collection of modules
identified in this SAD, or to the entire system or subsystem covered by
this SAD. For each variation, this section identifies the increment(s)
of the software build in which the variation will be available and used.
Finally, this section describes any additional potential that exists to
reuse one or more of the modules or their identified variations, even if
this reuse is not currently planned for any increment.

#### NAMING CONVENTIONS

\#1 This section should explain all naming conventions used, and draw
attention to any points a maintenance programmer would not expect. A
table of the file types and the permitted names or extensions for each
is recommended for quick reference.

\#2 Conventions for naming files, programs, modules, and possibly other
structures such as variables and messages, should all be documented
here.

#### PROGRAMMING STANDARDS

\#1 This section should define the project programming standards.
Whatever languages or standards are chosen, the aim should be to create
a convenient and easily usable method for writing good-quality software.
If an application development tool is used there may be other
conventions that need to be defined, e.g. colour schemes.

\#2 When programming in any new language, a standard for its use should
be written to provide guidance for programmers. This standard may be
referenced or included here.

\#3 Where there are external interfaces, the programming standards for
the interfaces required should be referenced.

\#4 In general, the programming standard should define a consistent and
uniform programming style. Specific points to cover are:

a. modularity and structuring;

b. headers and commenting;

c. indenting and layout;

d. library routines to be used;

e. language constructs to use;

f. language constructs to avoid.

## Views

Describe the different view points.

Describe for each view:

  - Name the view.

  - View Description

  - Describe the view’s purpose and contents. Refer to the viewpoint
    description in

  - To which this view conforms.

  - View Packet Overview

  - Show the set of view packets in this view and explain why the set is
    complete and no duplicative.

  - Architecture Background :Provide any architecture background
    (including significant driving requirements, design approaches,
    patterns, analysis results, and requirements coverage) that applies
    to this view.

  - Variability Mechanisms:Describe any architectural variability
    mechanisms (e.g., adaptation data, compile-time parameters, and
    variable replication) described by this view, including a
    description of how and when those mechanisms can be exercised and
    any constraints on their use.

  - View Packets. Describe each view packet in the view using the
    following outline:

View Packet:Name the view packet.

Primary Presentation :Using an appropriate language, languages,
notation, or tool-based representation, present the elements that
populate this view packet and the relations among them.

Element: Catalog

Elements: Describe each element shown in the primary presentation, along
with the values of its relevant properties, which are described in the
viewpoint to which this view conforms.

Relations :Describe any additional relations among elements shown in the
primary presentation and any specializations or restrictions on those
relations.

Interfaces: Specify the software interfaces to any elements shown in the
primary presentation that must be visible to other elements. The primary
presentation that must be visible to other elements.

Behaviour: Specify any significant behaviour of elements or groups of
interacting elements that are shown in the primary presentation.

Constraints: List any constraints on elements or relations not otherwise

described.

Context Diagram: Provide a context diagram showing the context of the
part of the system represented by this view packet. Designate the view
packet’s scope with a distinguished symbol and show interactions with
external entities in the view’s vocabulary.

Variability Mechanisms:Describe any variability’s that are available in
the portion of the system shown in the view packet, along with how and
when those mechanisms can be used.

Architecture Background:Provide the rationale for any significant design
decisions whose scope is limited to this view packet.

Related View Packets:Provide section references for related view
packets, including the parent, children, and siblings of this view
packet. Related view packets might be in the same view or in different
ones.

## Relations Among Views 

### General Relations Among Views 

Describe the general relationship among the views chosen to represent
the architecture.

Discuss the consistencies among those views and identify any known
inconsistencies.

### View-to-View Relations 

Show how the elements in related views are associated.

## Referenced Materials 

For each referenced document, provide a complete citation that enables a
reader to easily locate the document.

## Glossary and acronyms

Provide definitions of the special terms used in the SAD. If a term has
a different meaning in this SAD than it does in a parent SAD, explain
why.

Provide definitions of the acronyms used in the SAD.

## Appendixes 

Appendixes can be used to provide information published separately for
convenience in

document maintenance (e.g., charts, classified data). As applicable,
each appendix should be referenced in the main body of the document
where the appendix data would normally have been provided. Appendixes
can be bound as separate documents for ease in handling.
