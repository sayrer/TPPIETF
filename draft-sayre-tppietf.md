---
stand_alone: true
ipr: trust200902
cat: info
submissiontype: independent
area: General

docname: draft-sayre-tppietf-00

title: "TPPIETF: The Proverbial Printer Impeding Encryption Task Forces"
abbrev: TPPIETF
lang: en
kw:
  - TLS
  - encryption
  - legacy devices
  - printers
date: 2026-04-01
author:
- ins: R. Sayre
  name: Robert Sayre
  email: sayrer@gmail.com
  uri: https://sayrer.com/

normative:
  RFC2119:
  RFC8174:
informative:
  RFC8446:
  RFC1149:

--- abstract

It is said to be in the basement.

Despite decades of work by the Internet Engineering Task Force to
develop, standardize, and promote transport layer security, global
deployment remains incomplete. This document investigates the primary
obstacle to universal encryption: a class of legacy printing devices,
often located in building basements, that are cited as justification
for continued plaintext transmission. This document provides a
taxonomy of such devices, analyzes the rhetorical structure of
printer-based encryption exemption claims, and proposes a framework
for evaluating their validity.

--- middle

# Introduction

The IETF has devoted substantial resources to the development of
protocols that protect data in transit. Transport Layer Security
(TLS) {{RFC8446}} is mature, widely implemented, and computationally
inexpensive on modern hardware. Yet deployment statistics suggest
that a significant fraction of network traffic remains unencrypted.

When pressed for an explanation, network administrators frequently
cite the existence of legacy devices that cannot be upgraded to
support modern cryptographic protocols. Chief among these devices
is a network printer, typically described as residing in a basement
or similarly liminal space.

This document examines the phenomenon of the Proverbial Printer In
The Basement (PPITB) and its outsize effect on Internet security
policy.

# Conventions and Definitions

{::boilerplate bcp14-tagged}

The following terms are used throughout this document:

{:vspace}
PPITB:
: Proverbial Printer In The Basement. A network-attached
  printing device of indeterminate age, cited as grounds for
  encryption exemption.

PEC:
: Printer Exemption Claim. A rhetorical construct in which the
  existence of a PPITB is offered as justification for
  continued plaintext transmission across an entire network
  segment, facility, or organization.

Liminal Space:
: A basement, utility closet, server room annex, or
  other location characterized by poor lighting, uncertain
  HVAC, and organizational ambiguity regarding responsibility.

# Background

The PPITB is rarely observed directly. Its existence is inferred from
statements made during security audits, policy discussions, and
budget meetings. Common formulations include:

> "We can't turn on TLS because there's a printer in the basement
> that doesn't support it."

> "Accounting needs that printer."

> "It's been running since before I started here."

> "I think someone from Facilities knows where it is."

The PPITB exhibits several properties that distinguish it from
ordinary network devices:

{:vspace}
Persistence:
: The PPITB has been operational for an indeterminate
  period, often described as "forever" or "since the Clinton
  administration."

Criticality:
: Despite its age, the PPITB is described as essential
  to business operations, typically involving financial
  reports, invoices, or other documents of unspecified but
  paramount importance.

Immutability:
: The PPITB cannot be upgraded, replaced, or configured.
  Attempts to do so are met with organizational resistance of
  uncertain origin.

Invisibility:
: The PPITB is believed to occupy a liminal space, but
  its precise location is known only vaguely. Those who claim
  knowledge of its whereabouts are unavailable for consultation,
  retired, or deceased.

# Taxonomy of Basement Printers

Field research has identified several common PPITB variants:

## The HP LaserJet 4

Manufactured between 1992 and 1998, the LaserJet 4 series is the
canonical PPITB. Specimens have been documented operating continuously
for over 25 years. The device communicates via parallel port, JetDirect
card, or in rare cases, LocalTalk.

Network administrators report a peculiar emotional attachment to
LaserJet 4 devices, often describing them as "tanks" or "the only
reliable thing in this building."

## The Dot Matrix Invoice Printer

A line printer of 1980s vintage, typically an Epson or Okidata model,
connected to a dedicated workstation running an end-of-life operating
system. The device prints multi-part invoices on continuous-feed paper
and is considered irreplaceable due to unspecified "integration" with
financial systems.

## The Plotter

A large-format printing device used by engineering or architectural
departments. The plotter is invariably described as "expensive" and
"still working fine." Its network stack predates widespread TLS
adoption and cannot be updated because the manufacturer no longer
exists.

## The Fax Machine

Though not strictly a printer, fax machines are frequently cited in
PECs. The fax machine occupies a unique position in organizational
mythology, being simultaneously obsolete and legally required.

## The Thermal Label Printer

A small device used in shipping or inventory operations. The thermal
label printer is typically connected via a protocol converter of
unknown provenance to a Windows XP workstation that "can't be touched."

# The Printer Exemption Claim (PEC)

A Printer Exemption Claim follows a predictable rhetorical structure:

1. An encryption mandate is proposed or imposed.

2. A stakeholder objects, citing the existence of a PPITB.

3. The PPITB is described as essential to operations.

4. The cost or complexity of addressing the PPITB is asserted to be
   prohibitive.

5. The encryption mandate is weakened, delayed, or abandoned.

The PEC is notable for its imperviousness to technical solutions. When
presented with options such as network segmentation, protocol gateways,
or device replacement, the claimant typically responds with one of
the following:

> "That's not in the budget."

> "We tried that and it didn't work."

> "The vendor says it's not supported."

> "We'd have to get approval from \[unreachable authority\]."

## The Recursive PEC

In advanced cases, a PEC may exhibit recursive properties. When one
PPITB is successfully addressed, a new PPITB is discovered, typically
in a different basement or at a remote facility. This pattern may
continue indefinitely.

## The Hypothetical PEC

Some PECs reference printers that may not actually exist. The
hypothetical PEC takes the form: "What if someone has a printer that
doesn't support TLS?" This variant is particularly difficult to
address, as it requires proving a negative across all possible
network configurations.

# The PPITB in Protocol Development

The PPITB exerts influence not only within individual organizations
but within the standards process itself. Working group discussions
reveal a consistent pattern in which security requirements are
weakened in deference to hypothetical legacy devices.

## The Weakening Gradient

A proposed security requirement typically follows a predictable
trajectory through the standardization process:

1. Initial draft: "Implementations MUST support TLS 1.3."

2. After working group discussion: "Implementations MUST support
   TLS 1.3, except where legacy device constraints prevent it."

3. After last call: "Implementations SHOULD support TLS 1.3."

4. After IESG review: "Implementations MAY support TLS 1.3 where
   operationally feasible."

At each stage, the PPITB is invoked not as a specific device but as
a category of concern. The argument takes the form: "What about
operators who have legacy equipment?" The equipment is never
identified, but its mere possibility is sufficient to erode the
requirement.

## The Mailing List Pattern

IETF mailing lists contain extensive archives of PPITB-based
objections. A representative exchange proceeds as follows:

> Author: "This draft requires TLS for all connections."
>
> Reviewer: "This will break existing deployments."
>
> Author: "Which deployments?"
>
> Reviewer: "I can't name them specifically, but they exist."
>
> Chair: "Perhaps we should make this a SHOULD."

The burden of proof is thus inverted: rather than requiring the
objector to demonstrate that a specific device would be harmed,
the author must prove that no such device exists anywhere on the
Internet.

## The Backward Compatibility Trap

The IETF has historically placed great emphasis on backward
compatibility and incremental deployment. This principle has
produced robust, long-lived protocols that interoperate across
decades of hardware and software.

However, this success has created a trap. The same commitment
to backward compatibility that allowed legacy devices to continue
operating has extended their operational lifespan far beyond
original expectations. Devices that were expected to be retired
in 2005 remain in service in 2025, precisely because the network
continued to accommodate them.

These devices are now cited as grounds for delaying or weakening
the very security standards the IETF develops. The IETF's own
architectural generosity has thus been turned against it: the
organization's commitment to not breaking the Internet is used
to argue against improvements to the Internet.

This document terms this phenomenon the Backward Compatibility
Trap.

## Opportunistic vs. Strict Encryption

The PPITB has shaped fundamental debates about encryption policy.
The "opportunistic encryption" approach, in which encryption is
used when available but plaintext is permitted as a fallback,
exists in part because of PPITB-based objections to strict
requirements.

Proponents of opportunistic encryption argue that some encryption
is better than none, and that strict requirements would cause
operators to disable encryption entirely rather than address
legacy devices. Critics observe that opportunistic encryption
can be trivially downgraded by an active attacker, and that the
PPITB thus provides cover not only for legacy devices but for
adversaries.

This document terms the broader pattern of security requirements
eroded by reference to hypothetical legacy devices the TPPIETF
effect.

# Evaluation Framework

This document proposes a framework for evaluating Printer Exemption
Claims. Organizations MAY refer to this as the TPPIETF framework.
Implementations SHOULD apply the following criteria:

## Existence Verification

The claimant MUST provide evidence that the PPITB exists. Acceptable
evidence includes:

* A photograph of the device with a current newspaper

* SNMP responses from the device's network interface

* Testimony from a witness who has seen the device within the
  past calendar year

Hearsay ("I heard there's a printer in the basement") is NOT
RECOMMENDED as a basis for policy decisions.

## Criticality Assessment

The claimant SHOULD demonstrate that the PPITB performs a function
that cannot be performed by other means. Questions to consider:

* What happens if the PPITB fails?

* When was the PPITB last used?

* Who uses the PPITB, and have they been consulted?

If the answers are "nothing," "unknown," and "no," respectively,
the PEC SHOULD be rejected.

## Remediation Analysis

The claimant MUST provide a cost-benefit analysis of addressing the
PPITB versus maintaining plaintext transmission. Factors to consider
include:

* The cost of a replacement device

* The cost of network segmentation

* The cost of a data breach attributed to unencrypted traffic

In most cases, the third factor will dominate.

# Protocol Considerations

This document does not propose modifications to existing protocols.
However, implementers MAY find it useful to include diagnostic
messages that acknowledge the PPITB phenomenon:

~~~~
TLS_ALERT_PRINTER_IN_BASEMENT (254): The server has declined to
negotiate TLS due to the presence of a legacy printing device.
~~~~

This alert code is purely informational and SHOULD NOT be implemented.

# IANA Considerations {#IANA}

This document requests the establishment of an "Excuses for Not
Deploying TLS" registry. Initial entries include:

| Code | Description                            |
|------|----------------------------------------|
| 0x01 | Printer in basement                    |
| 0x02 | Fax machine required by legal          |
| 0x03 | Vendor says it voids the warranty      |
| 0x04 | We're planning to migrate next quarter |
| 0x05 | The contractor who set it up left      |
| 0x06 | It works, why change it                |
| 0x07 | Certificate management is too hard     |
| 0x08 | Performance concerns (unsubstantiated) |
| 0x09 | Unfinished reading of TPPIETF          |
{: title="Excuses for Not Deploying TLS"}

Additional entries may be added via Expert Review.

# Security Considerations {#Security}

This entire document is a security consideration.

The Proverbial Printer In The Basement represents a class of
technical debt that has accrued interest for decades. Each year
that a PPITB is permitted to delay encryption deployment represents
an additional year of exposure to passive surveillance, active
interception, and data exfiltration.

Implementers are reminded that the PPITB is, in many cases,
proverbial. Its power derives not from its technical capabilities
but from its organizational mythology. Addressing the PPITB may
require skills beyond the purely technical, including stakeholder
management, budget negotiation, and in extreme cases, the physical
courage to enter a poorly lit basement.

--- back

# Canonical Printer Models

The following devices have been cited in Printer Exemption Claims
with sufficient frequency to warrant individual recognition:

* HP LaserJet 4 / 4M / 4 Plus / 4M Plus / 4V / 4MV
* HP LaserJet 5 / 5M / 5N / 5P
* HP LaserJet 6P / 6MP
* Epson FX-80 / FX-85 / FX-86e / FX-286e
* Okidata Microline 320 / 321 / 390 / 391
* IBM Proprinter / Proprinter II / Proprinter III
* Apple LaserWriter / LaserWriter Plus / LaserWriter II
* Xerox Phaser 350 / 450 / 740

This list is not exhaustive. New canonical models may be added as
field research continues.
