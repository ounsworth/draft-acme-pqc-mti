---
title: "ACME Post-Quantum Mandatory-To-Implement JWT Algorithm"
abbrev: "acme-pqc-mti"
category: info

docname: draft-ounsworth-acme-pqc-mti-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
updates: 8555
date:
consensus: true
v: 3
area: "Security"
workgroup: "Automated Certificate Management Environment"
keyword:
 - next generation
 - unicorn
 - AI-native
venue:
  group: "Automated Certificate Management Environment"
  type: "Working Group"
  mail: "acme@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/acme/"
  github: "ounsworth/draft-acme-pqc-mti"
  latest: "https://ounsworth.github.io/draft-acme-pqc-mti/draft-ounsworth-acme-pqc-mti.html"

author:
 -
    fullname: "Mike Ounsworth"
    organization: Cryptic Forest Software
    email: "mike@ounsworth.ca"

normative:

informative:

...

--- abstract

The ACME protocol specified in RFC8555 requires all implementations to support the signature algorithm EDCSA-P256 (ES256) and recommends support for Ed25519. Due to the risk of quantum computers, this mandatory-to-implement algorithm is removed, replacing it with ML-DSA-65.


--- middle

# Update to RFC8555 {#intro}

Due to the impending risks of Cryptographically-Relevant Quantum Computers (CRQCs), see {{?RFC9958}}, {{!RFC8555}} is updated to replace the following sentence from Section 6.2:

> An ACME server MUST implement the "ES256" signature algorithm
   [RFC7518] and SHOULD implement the "EdDSA" signature algorithm using
   the "Ed25519" variant (indicated by "crv") [RFC8037].

is replaced with:

> An ACME server MUST implement the "ML-DSA-65" signature algorithm [RFC9964].

# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations {#security}

This document enhances security by removing the requirement for implementations to support soon-to-be-weak algorithms and requiring instead mandatory support for the quantum-safe ML-DSA-65 signature algorithm.

# IANA Considerations {#iana}

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
