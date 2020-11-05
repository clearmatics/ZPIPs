---
zpip: 1
title: Community ZPIP Purpose and Guidelines
status: Active
type: Process
author(s): Antoine Rondelet <ar@clearmatics.com>
owner(s): Antoine Rondelet <ar@clearmatics.com>
created: 2020-11-02
---

## Abstract

This ZPIP is heavily based on [EIP-1](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md) by Martin Becze, Hudson Jameson et al.

Community ZPIP stands for Community Zeth Protocol Improvement Proposal. A Community ZPIP is a design document - written by community members willing to contribute to the design of Zeth - providing a concise technical specification of a feature and a rationale for the feature.

## Motivations

ZPIPs provide a gateway and communication channel for community engagement related to the design of the Zeth protocol and its upgrades.
A successful ZPIP must contain a unique and clear key proposal. The proposal may depend on other ZPIPs to present complex changes.
Importantly, the ZPIP author(s) is/are responsible for building consensus around the proposed changes as well as documenting dissenting opinions.

## Specification

### Community ZPIP Types

There are three types of Community ZPIPs:

- A **Standard Track** ZPIP describes any change that affects most or all Zeth implementations. Such changes are classified in two (non-exclusive) categories:
    1. **Interface**: ZPIPs describing changes in APIs/RPC-layer, contract ABIs and overall changes in data structures.
    2. **Cryptography**: ZPIPs describing alternative instantiations of cryptographic primitives and elliptic curves.
- A **Process** ZPIP describes a process surrounding Zeth or proposes a change to a process. Process ZPIPs are like *Standard Track ZPIPs* but apply to areas other than the Zeth protocol itself, such as changes in procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in Zeth development.
- An **Informational** ZPIP describes a Zeth design issue, provides general guidelines or information, and/or describes new protocol applications. It does not propose a new feature.

### ZPIP Workflow

#### Shepherding a ZPIP

Parties involved in the process are:
- the *ZPIP author(s)/owner(s)*
- the [*ZPIP editors*](#zpip-editors)
- the [*Zeth Core Developers*](https://github.com/clearmatics/zeth).

Before you begin writing a formal ZPIP, you should vet your idea. Verify first if an idea is original to avoid wasting time on something that will be be rejected based on prior research. It is thus recommended to check existing issues first and open a discussion thread on [the Issues section of this repository](https://github.com/clearmatics/ZPIPs/issues) if necessary.

In addition to making sure that your idea is original, it will be your role as the author to make your idea clear to reviewers and interested parties, as well as inviting editors, developers and community to give feedback on the aforementioned channels. You should try and gauge whether the interest in your ZPIP is commensurate with both the work involved in implementing it and how many parties will have to conform to it. Negative community feedback will be taken into consideration and may prevent your ZPIP from moving past the *Draft* stage.

#### ZPIP Process 

Following is the process that a successful ZPIP will move along:

```
[ IDEA ] -> [ DRAFT ] -> [ LAST CALL ] -> [ FINAL ]
```

Each status change is requested by the ZPIP author and reviewed by the ZPIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your ZPIP. The ZPIP editors will process these requests as per the conditions below.

- **Idea** -- Once the author has made sure that the proposed idea is original, has not been discussed in previous discussions and has any chance of support, they will write a draft ZPIP as a [pull request](https://github.com/clearmatics/ZPIPs/pulls). Consider including an implementation if this will aid people in studying the ZPIP (please be aware of the code's license if taken/adapted from an existing implementation).
    - :arrow_right: *Draft* -- If agreeable, ZPIP editors will assign the ZPIP a number (generally the issue or PR number related to the ZPIP) and merge your pull request. The ZPIP editor will not unreasonably deny a ZPIP.
    - :x: *Draft* -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or not addressing backwards compatibility.
- **Draft** -- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the ZPIP to be mature and ready to proceed to the next status. Depending on the scope of the ZPIP, ZPIP editors may request (pseudo-)code implementation of the ZPIP before considering it for promotion to the next status.
    - :arrow_right: *Last Call* -- If agreeable, the ZPIP editors will assign *Last Call* status and set a review end date (`review-period-end`) - normally 14 days later. For all **Standard Track** ZPIPs to move further the **Draft** stage, they must contain clear evidence that the proposed change is secure. This is all the more important for ZPIP labelled **Cryptography** which must contain sound cryptographic proofs of security (whether entirely new proofs or proofs adapting/referring to proofs in the literature).
    - :x: *Last Call* -- A request for *Last Call* status will be denied if material changes are still expected to be made to the draft. Ideally ZPIPs should only enter *Last Call* once.
- **Last Call** -- This ZPIP will be either be moved back to *Draft* or advance to the *Final* status at the date `review-period-end`.
    - :arrow_right: *Final* -- A successful *Last Call* without material changes or unaddressed technical complaints will become *Final*.
    - :x: *Final* -- A *Last Call* which results in material changes or substantial unaddressed technical complaints will cause the ZPIP to revert to *Draft*.
- **Final** -- This status signals that material changes are unlikely and Zeth developers should consider this ZPIP for inclusion. Their process for deciding whether to implement it is outside of the ZPIP process (which only focuses on - neutrally - merely accepting sound community protocol changes proposals).
    - :arrow_right: *Draft* -- The Zeth Devs can decide to move this ZPIP back to the *Draft* status at their discretion. E.g. a major, but correctable, flaw was found in the ZPIP.
    - :arrow_right: *Rejected* -- The Zeth Devs can decide to mark this ZPIP as *Rejected* at their discretion. E.g. a major, but uncorrectable, flaw was found in the ZPIP.
    - :arrow_right: *Implemented* -- If/When the implementation of the ZPIP is complete and added to the protocol, the status will be changed to *Implemented*.
- **Implemented** -- This ZPIP represents the current state-of-the-art. Protocol changes must be reflected in the formal protocol specifications, and credit must be granted to the ZPIP author(s) in the specification document changelog. A Final ZPIP should only be updated to correct errata.

Other exceptional statuses include:

- **Active** -- Some *Informational* and *Process* ZPIPs may also have a status of *Active* if they are never meant to be completed. E.g. ZPIP-1 (this ZPIP).
- **Abandoned** -- This ZPIP is no longer pursued by the original authors or it may not be a (technically) preferred option anymore.
    - :arrow_right: *Draft* -- Authors or new champions wishing to pursue this ZPIP can ask for changing it to *Draft* status.
- **Rejected** -- A ZPIP that is fundamentally broken or a ZPIP that will not be implemented. A ZPIP cannot move on from this state.
- **Superseded** -- A ZPIP which was previously *Final* but is no longer considered state-of-the-art. Another ZPIP will be in *Final* status and reference the Superseded ZPIP. A ZPIP cannot move on from this state.

### Structure of a ZPIP

Each ZPIP should have the following parts:

- `Preamble` - [RFC 822](https://tools.ietf.org/html/rfc822) style headers containing metadata about the ZPIP, including the ZPIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See below for details.
- `Terminology` - A short section defining - unambiguously - key-words semantics (e.g. [RFC2119](https://www.rfc-editor.org/rfc/rfc2119.html))
- `Abstract` - A short (~200 words) description of the technical issue being addressed.
- `Motivation` - The motivation explaining clearly why the current state of the protocol (or processes) is inadequate, and how the ZPIP solves it. ZPIP submissions without sufficient motivation may be rejected outright.
- `Specification` - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow multi-language/interoperable implementations of the protocol. Notations must be unambiguous, comprehensive, and follow the notations of the [Zeth protocol specifications](https://github.com/clearmatics/zeth-specifications/blob/master/zeth-protocol-specification.pdf) when possible.
- `Rationale` - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- `Backwards Compatibility` - All ZPIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The ZPIP must explain how the author proposes to deal with these incompatibilities. ZPIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- `Implementations` - The implementations must be completed before any ZPIP is given status *Final*, but it need not be completed before the ZPIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.
- `Security Considerations` - All ZPIPs must contain a section that discusses the security implications/considerations relevant to the proposed change(s). Likewise, they must include information that might be important for security discussions, surfaces risks and can be used throughout the life cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. ZPIP submissions missing the "Security Considerations" section will be rejected. A ZPIP cannot proceed to status *Final* without a Security Considerations discussion deemed sufficient by the reviewers.
- `References and acknowledgements` - All ZPIPs building on existing ideas and projects must contain a section with extensive acknowledgements and references.
- `Changelog` - All updates to a ZPIP must be accompanied by a brief and descriptive entry of the changes in the document's changelog. This, along the Git history, aims to simplify the review process of the document throughout its lifetime.
- `Copyright/License` - All ZPIPs must be in the public domain. See the bottom of this ZPIP for an example copyright waiver.

### ZPIP Formats and Templates

ZPIPs should be written in Markdown format. There is a [template](../zpip-template.md) to follow.

### ZPIP Header Preamble

Each ZPIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order.

- `zpip: <ZPIP-number>` (this is determined by the ZPIP editors)
- `title: <ZPIP-title>`
- `author(s): <author(s)-name(s)>` (and/or Github username(s), or name(s) and email(s))
- `owner(s): <owner(s)-name(s)>` (and/or Github username(s), or name(s) and email(s))
- `[Optional] discussions-to: <URL-to-discussions>`
- `status: <Idea, Draft, Last Call, Final, Active, Abandoned, Rejected, Superseded>`
- `[Optional: Last-Call only] review-period-end: <date-review-period-ends>`
- `type: <Standard Track, Process, Informational>`
- `[Optional: Standard-Track only] category: <Interface, Cryptography>`
- `created: <date-created-on>` (date format: `YYYY-MM-DD`)
- `[Optional] updated: <list-update-dates>` (comma separated list of dates)
- `[Optional] requires: <ZPIP-number(s)>` (comma separated list of ZPIPs on which this ZPIP depends)
- `[Optional] replaces: <ZPIP-number(s)>` (comma separated list of ZPIPs that this ZPIP replace)
- `[Optional] superseded-by: <ZPIP-number(s)>` (comma separated list of ZPIPs replacing this ZPIP)
- `[Optional] resolution: <URL-pointing-to-resolution-of-this-ZPIP>`

#### Conventions

- Headers that permit lists must separate elements with commas.
- Headers requiring dates will always do so in the format of [ISO 8601 (yyyy-mm-dd)](https://www.iso.org/iso-8601-date-and-time-format.html).

### Linking to other ZPIPs

References to other ZPIPs should follow the format `ZPIP-N` where `N` is the ZPIP number you are referring to. Each ZPIP that is referenced in a ZPIP **MUST** be accompanied by a relative markdown link the first time it is referenced, and **MAY** be accompanied by a link on subsequent references.  The link **MUST** always be done via relative paths so that the links work in this GitHub repository, forks of this repository, etc. For example, you would link to this ZPIP with `[ZPIP-1](./zpip-1.md)`.

### Auxiliary Files

Images, diagrams and auxiliary files should be included in a sub-directory of the `assets` folder for that ZPIP as follows: `assets/zpip-N` (where **N** is to be replaced with the ZPIP number). When linking to an image in the ZPIP, use relative links such as `../assets/zpip-1/image.png`.

### Transferring ZPIP Ownership

It occasionally becomes necessary to transfer ownership of ZPIPs to a new owner. In general, we'd like to retain the original author as a co-author of the transferred ZPIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the ZPIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the ZPIP. We try to build consensus around a ZPIP, but if that's not possible, you can always submit a competing ZPIP.

If you are interested in assuming ownership of a ZPIP, send a message asking to take over, addressed to both the original author and the ZPIP editors. If the original author doesn't respond to email in a timely manner, the ZPIP editors will make a unilateral decision - such decision may be reversed in the event of a conflict.

Transferring ownership of a ZPIP will translate into:
- A notification in the changelog of the document
- A modification of the `author(s)` and `owner(s)` headers.

### ZPIP Editors

The current ZPIP editors are:

- Antoine Rondelet (@AntoineRondelet)

The role of ZPIP editors is to read and check new ZPIPs (check soundness, consistency with ZPIP template and conventions, language) as well as merging them to the repository if all checks have been satisfied.

Communications between editors and ZPIP authors will be handled via Github issues and pull requests, but we gently ask ZPIP authors to be tolerant with regard to review delays :)

**Note:** No insurance can be made on the review delays for each ZPIP. The ZPIP editors will do their best to review ZPIPs in the best delays.

### Style Guide

When referring to a ZPIP by number, it should be written in the hyphenated form `ZPIP-X` where `X` is the ZPIP's assigned number.

## References and Acknowledgements

This ZPIP is strongly based on the [first Ethereum Improvement Proposal (EIP-1)](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md) by Martin Becze, Hudson Jameson et al. which was itself derived from Amir Taaki's [Bitcoin's BIP-0001](https://github.com/bitcoin/bips/blob/master/bip-0001.mediawiki) (then superseded by Luke Dashjr's [BIP-0002](https://github.com/bitcoin/bips/blob/master/bip-0002.mediawiki)) which in turn was derived from [Python's PEP-0001](https://www.python.org/dev/peps/pep-0001/) by Barry Warsaw, Jeremy Hylton, and David Goodger.

## Changelog

- November 2, 2020: ZPIP-1 creation (adapted from [EIP-1](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md))

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
