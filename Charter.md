# Charter for Working Group

CBOR Object Signing and Encryption (COSE, RFC 8152) describes how to
create and process signatures, message authentication codes, and
encryption using Concise Binary Object Representation (CBOR, RFC 7049)
for serialization. COSE additionally describes a representation for
cryptographic keys.

COSE has been picked up and is being used both by a number of groups
within the IETF (i.e. ACE, CORE, ANIMA, 6TiSCH and SUIT) as well as
outside of the IETF (i.e. W3C and FIDO). There are a number of
implementations, both open source and private, now in existence.
The specification has advanced to STD status.

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

The WG currently has two deliverables:

1. One or more documents describing the proper use of algorithms.
These algorithms must meet the requirements outlined above.

2. A CBOR encoding of the certificate profile defined in RFC 5280.
It is expected that the encoding works with RFC 7925 and takes into consideration any updates in draft-ietf-uta-tls13-iot-profile-00.
The encoding may also include other important IoT certificate profiles like
IEEE 802.1AR.
The main objective is to define a method of encoding current X.509
certificates that meet a specific profile into a smaller format. This
encoding is invertible so they can be expanded and normal X.509
certificate processing used.
The data structures used for such encoding of X.509 certificates are
expected to produce a compact encoding for certificate information, and are
not necessarily tied specifically to X.509 certificates.  Accordingly, a
secondary objective is to reuse these data structures to produce a natively signed CBOR certificate encoding; such a structure is relevant in situations
where DER parsing and the re-encoding machinery to convert
between CBOR and DER encodings are unnecessary overhead, such as embedded
implementations.  The possibility of a joint certificate artifact, conveyed in
CBOR encoding but including signatures over both the CBOR and DER encodings,
may be explored.
This work will be based on draft-mattsson-cose-cbor-cert-compress.
The working group will collaborate and coordinate with other IETF WGs such as
TLS, UTA, LAKE to understand and validate the requirements and solution.
