AWS versus Chronopolis
======================

We should approach our instances of AWS and Chronopolis very differently.  This document explains the differences and
rationale.

AWS
---

When we complete this migration, we will have 2TB of AWS storage.  We kept this 2TB of storage for use cases where we
need **DIM** access.  By DIM, we mean that we are likely to need to fetch something from here and may write or update
what we have there.

See AWS Use Cases for examples of things where we definitely need AWS.

Chronopolis
-----------

Chronopolis is very different.  We intend to use Chronopolis as a true **dark** archiving solution.  This means that what
we intend to write to Chronoplis we would only retrieve if we exhaust all other options and only in a true disaster situation.

When we complete the migration we will have 25 TB of Chronopolis storage.  While this sounds like a lot, we should attempt
to only deposit things here that are "preservation" worthy. This means we should not send derivatives such as JP2 datastreams
generated from another JP2 or TIF, a generated PDF, OCR, HOCR, Medium Size JPEGs, etc.  The only exception to this is
when we have a situation where it'd be difficult to recreate the derivative or proxy.  We should think about these cases
as we come up with our use cases.
