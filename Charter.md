# Charter for Working Group

CBOR Object Signing and Encryption (COSE, RFC 8152) describes how to
create and process signatures, message authentication codes, and
encryption using Concise Binary Object Representation (CBOR, RFC 7049)
for serialization. COSE additionally describes a representation for
cryptographic keys.

COSE has been picked up and is being used both by a number of groups
within the IETF (i.e. ACE, CORE, ANIMA, 6TiSCH and SUIT) as well as
outside of the IETF (i.e. W3C and FIDO). There are a number of
implementations, both open source and private, now in existence. ~~The
specification is now sufficiently mature that it makes sense to try
and advance it to STD status.~~ The specification has advanced to STD status.

~~The standards progression work will focus on:
1. Should the document be split in two? The first document would
contain the definitions of the structures and rules for processing
them. The second document would contain the set of original
algorithms that were defined.
2. What areas in the document need clarification before the document
can be progressed?
3. What implementations exist and do they cover all of the major
sections of the document?
4. Resolution of any Errata or ambiguities in the document~~

~~There are a small number of COSE related documents that will also be
addressed by the working group dealing with additional attributes and
algorithms that need to be reviewed and published. The first set
are listed below in the deliverables. A re-charter will be required
to expand this list.~~

The COSE working group will deal with two types of documents going forward:

1.  Documents that describe the use of cryptographic algorithms in COSE.
2.  Documents which describe additional attributes for COSE.

The WG will evaluate, and potentially adopt, documents dealing with algorithms
which would fit the criteria of being IETF consensus algorithms.
Potential candidates would include those algorithms which have been evaluated by
the CFRG and algorithms which have gone through a public review and evaluation
process such as was done for the NIST SHA-3 algorithms.
Potential candidate would not include national standards based algorithms
which have not gone through a similar public review process.

The WG will produce documents for new attributes only if they are in the
list of deliverables below.  A re-charter will be required to expand that list.
The WG is expected as part of normal processing to review and comment on
attributes which are not in charter but are of general public interest.

~~The SUIT working group has identified a need for the use of hash-based
signatures in the form of Leighton-Micali Signatures (LMS)
(draft-mcgrew-hash-sigs). This signature form is resistant to quantum
computer attacks and is low-cost for validation. The SUIT working group
additionally has identified a need for registering hash functions for
indirect packaging.~~

~~The W3C Web Authentication working group has identified a need for the
ability to use algorithms which are currently part of TPMs which are
widely deployed.~~

~~At the time COSE was developed, there was a sense that X.509
certificates were not a feature that needed to be transferred from the
JOSE key document (RFC 7517). Since that time a better sense of how
X.509 certificates would be used both in the IoT sphere and with COSE
outside of the IoT sphere has been developed. The ability to identify
or carry X.509 certificates now needs to be provided. This will require
the definition of a small number of hash functions for compact references
to X.509 certificates.~~

Key management and binding of keys to identities are out of scope for
the working group. The COSE WG will not innovate in terms of
cryptography. The specification of algorithms in COSE is limited to
those in RFCs, active CFRG or IETF WG documents, or algorithms which
have been positively reviewed by the CFRG.

The working group will coordinate its progress with the ACE, SUIT and
CORE working groups to ensure that we are fulfilling the needs of
these constituencies to the extent relevant to their work. Other
groups may be added to this list as the set of use cases is expanded,
in consultation with the responsible Area Director.

The WG has delivered the following:

1. Republishing a version of RFC 8152 suitable for advancement to Internet
Standard.
2. Use of Hash-based Signature algorithms in COSE using
draft-housley-suit-cose-hash-sig as a starting point (Informational).
3. Placement of X.509 certificates in COSE messages and keys using
draft-schaad-cose-x509 as a starting point (Informational).
4. Define the algorithms needed for W3C Web Authentication for COSE using
draft-jones-webauthn-cose-algorithms and draft-jones-webauthn-secp256k1
as a starting point (Informational).
5. Define a small number of hash functions for X.509 certificate thumbprints
and for indirect signing (for SUIT) (Informational).

The WG currently has two deliverables:

1. One or more documents describing the proper use of algorithms.
These algorithms must meet the requirements outlined above.

2. A CBOR encoding of the compressed certificate profile defined in RFC 7925.
It is expected that the compression works with a large subset of RFC 7925 and
takes into consideration any updates in draft-ietf-uta-tls13-iot-profile-00.
The compression may also include other important IoT certificate profiles like
IEEE 802.1AR.  It should be noted that this is not a new certificate
architecture, rather it is a method of compressing current X.509 certificates
that meet a specific profile into a smaller format.  The compression algorithm
is loss-less so they can be expanded and normal X.509 certificate processing
used.  This work will be based on draft-mattsson-cose-cbor-cert-compress.
The working group will collaborate and coordinate with other IETF WGs such as
TLS, UTA, LAKE to understand and validate the requirements and solution.
