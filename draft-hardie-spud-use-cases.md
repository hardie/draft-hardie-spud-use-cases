---
title: Use Cases for SPUD
abbrev: SPUD-uses
docname: draft-hartke-xmpp-stupid-latest
date: 2015-02-10
category: info

ipr: trust200902
area: RAI
workgroup: DISPATCH
keyword: Internet-Draft

stand_alone: yes
pi: [toc, sortrefs, symrefs]

author:
 -
    ins: T. Hardie
    name: Ted Hardie
    organization: Google
    email: ted.ietf@gmail.com
 -

normative:
  RFC2119:


informative:
  I-D.hildebrand-spud-prototype:




--- abstract

SPUD is a prototype for grouping UDP packets together in a session.
This grouping allows on-path network devices, especially middleboxes 
such as NATs or firewalls, to understand basic session semantics
and potentially to offer salient information about their functions
or the path to the endpoints.  This document describes basic
use cases for sharing that session semantic and for using the
information shared.



--- middle

Introduction        {#problems}
============

SPUD
{{I-D.hildebrand-spud-prototype}}
is a prototype for grouping UDP packets together in a session.
This grouping allows on-path network devices, especially middleboxes 
such as NATs or firewalls, to understand basic session semantics
and potentially to offer salient information about their functions
or the path to the endpoints.  This document describes basic
use cases for sharing that session semantic and for using the
information shared



The Need    {#need}
----------------------------



Basic Protocol Operation   {#ops}
========================



Protocol Definition
===================

Terminology          {#Terminology}
-----------
In this document, the key words "MUST", "MUST NOT", "REQUIRED",
"SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY",
and "OPTIONAL" are to be interpreted as described in BCP 14, RFC 2119
{{RFC2119}} and indicate requirement levels for compliant STuPiD
implementations.





Security Considerations
=======================

The privacy objective here is to enable UDP-based transports
whose payload is fully encrypted to have very simple session
semantics exposed to the path elements which might otherwise
required access to plaintext.  Obviously, any exposure beyond
the standard 5-tuple involves some information sharing which
is not required for packet delivery.  There are potential
attacks that use session start and stop semantics to infer
known plain text for a common protocol, those they require
cryptographics attacks or failures which are not common.
Later versions of this document will explore the cases in
which use of SPUD to expose those session semantics is not
appropriate.


--- back


Examples  {#examples}
========


