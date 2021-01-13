Chronopolis
===========

Costs
-----

* $275 per TB (ingest)
* $163 per TB per year for long term storage
* $275 per TB (retrieval)

Storage
-------

* 25 TB

Procedures and Policies
-----------------------

1. Chronopolis should be treated as a dark archive.  As such, we should only put files related to preservation there. No
derivatives or files that can be easily recreated.

2. Similarly, once we deem an object ready for depost into Chronopolis, it should be "good enough."  We should not need
to update or interact with what's in Chronopolis if the object on our end has minor modifications.  For instance, descriptive
metadata may be updated, but we don't need to fix what's in Chronopolis.  That being said, we should send a descriptive
metadata file with the object so that the object could be understood in the future (either by us or our successors). See
use cases for more details.

3. It costs us the same amount to ingest content as it does to retrieve. Furthermore, retrieval is done based on the
snapshot, not the file.  Because of this, to restore one 200 MB file we'd have to restore 2 TB of data if we had a 2 TB
snapshot. This could be costly both in terms of money but specifically retrieval time. To be proactive, we should set a
maximum snapshot size.  I propose 150 GB.

4. Where possible, snapshot based on collection.  For instance, :code:`tdh` is approximately :code:`98.4 GB`. This is
well under my proposed limit, but semantically it makes sense to store tdh alone in a snapshot like :code:`tdh_1_2021`.

5. When collections are larger than 150 GB, we split the snapshots into chunks with parts and years like:
:code:`wwiioh_1_2021`, :code:`wwiioh_2_2021`, etc.

6. If we ingest a new "batch" of a previous existing collection, we snapshot that new batch separately. We could use the
same naming convention or something like :code:`wwiioh_new_2021_01_13`.  We really just need a snapshot namescheme.

7. In the rare case that we have a file larger than :code:`150GB`, we snapshot the file (or file(s) if we're thinking in
object) by itself.



Use Cases
---------
