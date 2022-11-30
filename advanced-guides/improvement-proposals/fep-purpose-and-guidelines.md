# FEP Purpose and Guidelines

## What is an FEP

FEP stands for FINL Enhancement Proposal. An FEP is a design document providing information to the FINL Chain community, or describing a new feature for FINL Chain or its processes or environment. The FEP should provide a concise technical specification of the feature and a rationale for the feature. The FEP author is responsible for building consensus within the community and documenting dissenting opinions.

## FEP Rationale

We intend FEPs to be the primary mechanisms for proposing new features, for collecting community input on an issue, and for documenting the design decisions that have gone into FINL Chain. Because the FEPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For FINL Chain implementers, FEPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the FEPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## FEP Types

There are three types of FEP:

* A Standard Track FEP
* An Informational FEP
* A Meta FEP

### A Standard Track FEP

A Standard Track FEP describes any change that affects most or all FINL Chain implementations, such as a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using FINL Chain. Furthermore, Standard FEPs can be broken down into the following categories. Standards Track FEPs consist of three parts, a design document, implementation, and finally if warranted an update to the formal specification.

#### Core

Core - improvements requiring a consensus fork, as well as changes that are not necessarily consensus critical but may be relevant to Block Producer and Block.

#### Networking

Networking - improvements around p2p protocol.

#### Interface

Interface - includes improvements around client API specifications and standards, and also certain language-level standards like contract formats. For contract formats, it aligns with the FINL Chain contracts repo and discussion should primarily occur in that repository before an FEP is submitted to the FEPs repository.

### An Informational FEP

An Informational FEP describes an FINL Chain design issue, or provides general guidelines or information to the FINL Chain community, but does not propose a new feature. Informational FEPs do not necessarily represent FINL Chain community consensus or a recommendation, so users and implementers are free to ignore Informational FEPs or follow their advice.

### A Meta FEP

A Meta FEP describes a process surrounding FINL Chain or proposes a change to (or an event in) a process. Process FEPs are like Standard Track FEPs but apply to areas other than the FINL Chain protocol itself. They may propose an implementation, but not to FINL Chain’s codebase; they often require community consensus; unlike Informational FEPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in FINL Chain development. Any meta-FEP is also considered a Process FEP.

It is highly recommended that a single FEP contain a single key proposal or new idea. The more focused the FEP, the more successful it tends to be. A change to one client doesn’t require an FEP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.

An FEP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

## FEP Work Flow

Your role as the champion is to write the FEP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful FEP will move along:

{% tabs %}
{% tab title="DGOS" %}
\[ WIP ] :arrow\_right: \[ DRAFT ] :arrow\_right: \[ LAST CALL ] :arrow\_right: \[ ACCEPTED ] :arrow\_right: \[ FINAL ]
{% endtab %}

{% tab title="Standard Specification" %}
\[ STANDARD ] :arrow\_right: \[ LAST CALL ] :arrow\_right: \[ ACCEPTED ] :arrow\_right: \[ FINAL ]
{% endtab %}
{% endtabs %}

Each status change is requested by the FEP author and reviewed by the FEP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your FEP. The FEP editors will process these requests as per the conditions below.

&#x20;The DGOS’s document number should increase sequentially from 1. The standard specification’s document number should increase sequentially from 9001.

### Work In Progrss (WIP)

Work in progress (WIP) – Once the champion has asked the FINL Chain community whether an idea has any chance of support, they will write a draft FEP as a \[pull request]. Consider including an implementation if this will aid people in studying the FEP.

#### "arrow\_right" Draft

"arrow\_right" Draft – If agreeable, FEP editor will assign the FEP a number (generally the issue or PR number related to the FEP) and merge your pull request. The FEP editor will not unreasonably deny an FEP.

#### "x" Draft

"x" Draft – Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, or not providing proper motivation or addressing backwards compatibility.

### Draft

Draft – Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the FEP to be mature and ready to proceed to the next status. An FEP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core FEPs).

#### "arrow\_right" Last Call

"arrow\_right" Last Call – If agreeable, the EEP editor will assign Last Call status and set a review end date, normally 14 days later.

#### "x" Last Call

"x" Last Call – A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that FEPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed. Last Call will be denied if the implementation is not complete and supported by the community.

### Standard

Standard – Once the standard from ITU, ETSI, IEEE, and TTA has been introduced, the FINL Chain community will review the standard and will decide whether to accept that standard.

#### "arrow\_right" Last Call

"arrow\_right" Last Call – If agreeable, the EEP editor will assign Last Call status and set a review end date, normally 14 days later.

#### "x" Last Call

"x" Last Call – A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that FEPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed. Last Call will be denied if the implementation is not complete and supported by the community.

### Last Call

Last Call – This FEP will listed prominently on the FEP website.

#### "x"

"x" – A Last Call which results in material changes or substantial unaddressed complaints will cause the FEP to revert to Draft.

#### "arrow\_right" Accepted (Core FEPs only)

"arrow\_right" Accepted (Core FEPs only) – After the review end date, the FINL Chain Core Developers will vote on whether to accept this change. If yes, the status will upgrade to Accepted.

#### "arrow\_right" Final (Not core FEPs)

"arrow\_right" Final (Not core FEPs) – A successful Last Call without material changes or unaddressed complaints will become Final.

### Accepted (Core FEPs only)

Accepted (Core FEPs only) – This is being implemented by FINL Chain Core Developers and integrated into the FINL chain.

#### "arrow\_right" Final

"arrow\_right" Final – When the implementation is complete and supported by the community, the status will be changed to “Final”.

### Final

Final – This FEP represents the current state-of-the-art. A Final FEP should only be updated to correct errata.

### Other Exceptional Statuses

#### Deferred

Deferred – This is for core FEPs that have been put off for a future hard fork.

#### Rejected

Rejected – An FEP that is fundamentally broken and will not be implemented.

#### Active

Active – This is similar to Final, but denotes an FEP which which may be updated without changing its FEP number.

#### Superseded

Superseded – An FEP which was previously final but is no longer considered state-of-the-art. Another FEP will be in Final status and reference the Superseded FEP.

## A successful FEP

### What belongs in a successful FEP?

Each FEP should have the following parts:

#### Preamble

Preamble - RFC 822 style headers containing metadata about the FEP, including the FEP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See below for details.

#### Simple Summary

Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the FEP.

#### Abstract

Abstract - a short (\~200 word) description of the technical issue being addressed.

Motivation (\*optional) - The motivation is critical for FEPs that want to change the FINL protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the FEP solves. FEP submissions without sufficient motivation may be rejected outright.

#### Specification

Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current FINL platforms.

#### Rationale

Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.

#### Backwards Compatibility

Backwards Compatibility - All FEPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The FEP must explain how the author proposes to deal with these incompatibilities. FEP submissions without a sufficient backwards compatibility treatise may be rejected outright.

#### Test Cases

Test Cases - Test cases for an implementation are mandatory for FEPs that are affecting consensus changes. Other FEPs can choose to include links to test cases if applicable.

#### Implementations

Implementations - The implementations must be completed before any FEP is given status “Final”, but it need not be completed before the FEP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.

#### Copyright Waiver

Copyright Waiver - All FEPs must be in the public domain. See the bottom of this FEP for an example copyright waiver.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
