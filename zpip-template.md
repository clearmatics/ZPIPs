---
zpip: `<to-be-assigned>`
title: `<ZPIP-title>`
author: `<author(s)>`
discussions-to: `<URL>`
status: Draft
type: `<Standards Track, Process, or Informational>`
category (*only required for Standards Track*): `<Interface, Cryptography>`
created: `<yyyy-mm-dd>`
requires (*optional*): `<ZPIP number(s)>`
replaces (*optional*): `<ZPIP number(s)>`
---

This is the suggested template for new ZPIPs (taken and adapted from the [EIP template](https://github.com/ethereum/EIPs/blob/master/eip-template.md)).

Note that a ZPIP number will be assigned by an editor. When opening a pull request to submit your ZPIP, please use an abbreviated title in the filename, `zpip-draft_title_abbrev.md`.

The title should be 44 characters or less.

## Simple Summary

"If you can't explain it simply, you don't understand it well enough." Provide a simplified and layman-accessible explanation of the ZPIP.

## Abstract

A short (~200 word) description of the technical issue being addressed.

## Motivation

The motivation is critical for ZPIPs that want to change the Zeth protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the ZPIP solves. ZPIP submissions without sufficient motivation may be rejected outright.

## Specification

The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to be implemented in variours programming languages and must contain security proofs when necessary.

## Rationale

The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.

## Backwards Compatibility

All ZPIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The ZPIP must explain how the author proposes to deal with these incompatibilities. ZPIP submissions without a sufficient backwards compatibility treatise may be rejected outright.

## Test Cases

Test cases for an implementation are mandatory for ZPIPs that are proposing cryptographic changes.

## Implementation

The implementations must be completed before any ZPIP is given status "Final", but it need not be completed for the ZPIP to be merged as a "Draft".

## Security Considerations

All ZPIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surfaces risks and can be used throughout the life cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. ZPIP submissions missing the "Security Considerations" section will be rejected. A ZPIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.

## References and Acknowledgements

All ZPIPs building on existing ideas and projects must contain a section with extensive acknowledgements and references.
This ZPIP template, for instance, is taken and adapted from Martin Becze, Hudson Jameson et al.'s work on [EIPs](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md) and [EIP template](https://github.com/ethereum/EIPs/blob/master/eip-template.md).

## Changelog

All updates to a ZPIP must be accompanied by a brief and descriptive entry of the changes in the document's changelog. This, along the Git history, aims to simplify the review process of the document throughout its lifetime.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
