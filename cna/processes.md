THIS CONTENT HAS BEEN DEPRECATED. 

REFER TO THE CNA RULES LOCATED AT <http://cve.mitre.org/cve/cna.html#documentation_for_cnas>
FOR THE CURRENT CNA PROCESSES

---
title: CNA Processes
layout: page
---

Updated: October 7, 2014

## Requirements


1. Must be an established entity that has published security
   advisories, or their equivalents, for at least six months,
   preferably a year.

2. Must publish advisories to the general public, for free, to at
   least one channel that does not require any registration or login.

3. Must publish at least 20 CVEs per year, and preferably 50 or more.

4. Must be willing to follow CVE content decisions - abstraction and
   inclusion - even when they are inconsistent with the CNA's own
   methods.

5. Must have a technical human POC and a public e-mail address for
   resolving any issues that arise.

6. Must be willing to coordinate with all parties - researchers,
   vendors, MITRE, etc. - regarding the exchange of CVE IDs in a way
   that minimizes duplicates.

7. Must be willing to undergo a training and review process.


## CNA Recruitment Process

Updated: October 7, 2014

The potential CNA is called a "prospect."

1. Determine if the prospect qualifies (see Requirements)

2. Email first, then telecon

3. Prospect identifies a primary POC - typically a person with very
   strong technical ability who is involved in the day-to-day process
   of vulnerability disclosure.  Prospect provides assurances to MITRE
   that the primary POC will follow content decisions closely, follow
   expected coordinatin procedures to reduce risk of duplicates, etc.

4. MITRE makes the prospect aware of process changes they may need to
   undergo (which might include working with their own management or
   other parts of their company)

5. Prospect provides MITRE with specific details on where its
   advisories are published online; ensures that registration is not
   required for any consumer; and tells MITRE how to access those
   advisories to find the most recent advisories first.

   ### Training period begins

6. MITRE provides documents on abstraction/inclusion and fields any
   questions.

7. MITRE back-fills any CVEs for relatively recent advisories, and use
   it to train the prospect about abstraction/inclusion.

8. For some time, the prospect makes "normal" reservations from the
   MITRE CNA, who clarifies potential issues and decisions.

9. TODO: it would be nice to have a series of "tests" to ensure the
   CNA prospect really understands CVE abstraction.

10. After prospect has performed enough reservations - either 20 CVEs
   (from step 8), or passed the to-be-implemented test (from step 9)
   - the prospect receives their first pool of CVEs.

11. Prospect is expected to devise its own processes and procedures
    for managing its CVE pool.  (This often requires some internal
    clarificatons of tasks and/or changes to the advisory-publication
    process.)

12. With the first pool, the primary POC is expected to (a) assign the
    CVEs relatively early in the process; (b) share these assignments
    with the MITRE CNA for its review; (c) make any corrections as
    needed before publication.

13. After a sufficient number of reviewed assignments - with no less
    than 20 public CVEs, and possibly more based on MITRE CNA's
    evaluation of the prospect's ability to follow content decisions -
    the prospect becomes an official CNA.

14. New CNA receives a new pool of IDs (if needed), is added to the
    official CNA list (e.g. on the CVE web site), mentioned in a news
    item, etc.




## Pool/Block Requests from Secondary CNAs

Updated: August 12, 2015


Secondary CNAs - typically vendors and coordinators - sometimes
request a new "pool" of candidates, also referred to as a "block" by
some.

1. Determine the size of the pool.  If the CNA specifically asks for a
   particular number of CVEs ("pool size"), then ensure that the pool
   size is reasonable for that particular CNA's volume; if the pool
   size seems too large, then negotiate with the CNA.

   If no pool size is given, then determine an "appropriate" size.
   Methods for determining pool size differ. Some prefer to use a pool size
   that is roughly equivalent to the number of IDs published by the
   CNA in 3 months (a quarter); others appear to prefer larger pool sizes.

2. Once the pool size has been determined, use the usual process to
   reserve and commit the IDs to candidates.txt.  (See the "Candidate
   Reservation" section.)

3. List the newly-reserved CVEs.  Using the reservation process in
   step 2 produces a [TEMPFILE] that contains the CVEs in the pool,
   perform a step such as:

      grep :CANDIDATE [TEMPFILE] | awk '{print $2}'

4. Copy-and-paste this list of IDs in the e-mail response to the CNA.
