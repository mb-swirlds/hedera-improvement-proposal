---
hip: <HIP number (assigned by the HIP editor), usually the PR number>
title: Schema Registry Native Service
author: Michael Bennett <michael@strukt.org>, Justin Atwell <justin.atwell@swirldslabs.com>
working-group: ???
requested-by: ???
type: <"Standards Track" | "Informational" | "Process">
category: Service
needs-council-approval: Yes
status: Draft
created: 2024-05-08
discussions-to: ??? (URL to the discussion thread)
updated: <Latest date HIP was updated, in YYYY-MM-DD format.>
requires: n/a
replaces: n/a
superseded-by: n/a
---

## Abstract
_(Please provide a short (~200 word) description of the issue being addressed.)_

A Schema Registry is used to allow storage of structured data defintions that can be accessed in programmatical fashion. These Schemas (Data Definitions) can be used in many novel ways. Mostly it allows the validation of data being passed around a system. This new proposed service adds on features that many other native and non-native services can harness for ease of use when ingesting and reading data, backed by a DLT based storage system for an immutable source of truth when it comes to these Schemas provenance.

## Motivation

_The motivation is critical for HIPs that want to change the Hedera codebase or ecosystem. It should clearly explain why the existing specification is inadequate to address the problem that the HIP solves. HIP submissions without sufficient motivation may be rejected outright._

---

Currently, HCS allows unstructured data to be inserted into a queue/topic. This makes the data very opaque but also unusable without a lot of implied knowledge. 

Many other data items we store or manage on or near chain in metadata files on IPFS also are structured but not always in a readily apparent or reusable fashion. 

Having a Schema Registry service would allow the seperation of the structure/validation of this data and the data itself in a reusable manner.

In the case of HCS it would allow us to ensure data ingested was structurally correct according to a Schema or revisions of a Schema over time. This would also add value to the data stored in HCS as it would be more usable and less opaque.

In terms of Metadata being attached to a Token there are many uses to having a Schema Registry. For example, a Token could have a Schema attached to it that defines the metadata but also for semi-fungible tokens it could define the structure of the metadata for each individual token or as it changes over the life of the token.

In terms of DiD or other identity systems, a Schema Registry could be used to define the structure of the data that is stored in the identity system. This would allow for a more flexible and extensible system.

In terms of ESG data stored in iPFS or other means. Having a seperate Schema Registry would allow for the data to be validated and structured in a way that is more easily consumed by other systems. Adding in the value of then connecting industry standard systems to this data opens up the ESG data to a wider audience.

## Rationale
_The rationale fleshes out the specification by describing why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages._
_The rationale should provide evidence of consensus within the community and discuss important objections or concerns raised during the discussion._

---


## User stories

_Provide a list of "user stories" to express how this feature, functionality, improvement, or tool will be used by the end user. Template for user story: “As (user persona), I want (to perform this action) so that (I can accomplish this goal).”_

---
  
## Specification

The technical specification should describe the syntax and semantics of any new features. The specification should be detailed enough to allow competing, interoperable implementations for at least the current Hedera ecosystem.

## Backwards Compatibility

All HIPs that introduce backward incompatibilities must include a section describing these incompatibilities and their severity. The HIP must explain how the author proposes to deal with these incompatibilities. HIP submissions without a sufficient backward compatibility treatise may be rejected outright.

## Security Implications

If there are security concerns in relation to the HIP, those concerns should be explicitly addressed to make sure reviewers of the HIP are aware of them.

## How to Teach This

For a HIP that adds new functionality or changes interface behaviors, it is helpful to include a section on how to teach users, new and experienced, how to apply the HIP to their work.

## Reference Implementation

The reference implementation must be complete before any HIP is given the status of “Final”. The final implementation must include test code and documentation.

## Rejected Ideas

Throughout the discussion of a HIP, various ideas will be proposed which are not accepted. Those rejected ideas should be recorded along with the reasoning as to why they were rejected. This both helps record the thought process behind the final version of the HIP as well as preventing people from bringing up the same rejected idea again in subsequent discussions.

In a way, this section can be thought of as a breakout section of the Rationale section that focuses specifically on why certain ideas were not ultimately pursued.

## Open Issues

While a HIP is in draft, ideas can come up which warrant further discussion. Those ideas should be recorded so people know that they are being thought about but do not have a concrete resolution. This helps make sure all issues required for the HIP to be ready for consideration are complete and reduces people duplicating prior discussions.

## References

A collections of URLs used as references through the HIP.

## Copyright/license

This document is licensed under the Apache License, Version 2.0 -- see [LICENSE](../LICENSE) or (https://www.apache.org/licenses/LICENSE-2.0)
