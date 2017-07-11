# Revision Process
*(also to be added to the CNA Rules as an Appendix)*

Revisions will be made in Git.

Revision list document and DRAFT new version.

Create a template for submissions to the CNA Rules revision process.
  - Goal
  - Proposed solution
  - Expected Outcome
  - Proposed language (optional)

First 30 days
  - open comment period
  - Board and CNAs
  - Use above format for revisions
  - 2 or 3 conference calls
  
 Next 60 days
  - 1 week sprints with a subset of the proposed revisions each sprint. Each subset is only to be discussed during that sprint.
  - 8 total sprints.
  - At the end of a sprint, if something wasn't resolved or discussed, it will not be included in this revision.
  - At the end of all sprints, the document will be finalized and sent to the Board for approval.
  
Proposed: New Rules go into effect on Jan 1, 2018
______

Suggested Rules Changes

These are suggested changes to the CNA Rules. These changes have not been vetted, and they may not have been fully developed or discussed. As suggestions are developed and discussed by the Board and the CNA community, this list will be updated to indicate if each suggestion will be incorporated or declined.

Comments can be added to each item or included in the Git comment system.

______

GOAL: Better define the correct use of CVE.

CHANGE: Should the requirement that CVE assignments must be public or planned to be made public be removed?
  - Should there be a new record type: "Not Public". This would accommodate the use case of a CVE ID being assigned without there being an intention for it to ever be made public (outside of the CNA's internal operation).

OUTCOME: CVE will be used as widely as necessary for as many use cases as practical.

______

GOAL: Track who reserved what CVE IDs.

CHANGE: Should the original reservation entity or reservation chain be added to required data?

OUTCOME: Regardless of the assigner, the entire Sub CNA/Root CNA chain of CVE ID reservations will be included in each CVE entry.

______

GOAL: Streamline the CVE Entry creation process.

CHANGE: Should "Description" be excluded from the required fields in Appendix B?

OUTCOME: CNAs and requesters will be able to assign CVE IDs with the least necessary effort.

______

GOAL: Make CNA scope more easily determined by third parties.

CHANGE: Add a rule that states a CNA must provide a page on their web site which lists the products for which they accept vulnerability reports. This includes a listing of EOL (or other) software that are explicitly _not_ covered.

OUTCOME: CNA scopes will be easy to find by anyone.

______

GOAL: Clarify existing language.

- Page 5 of the current CNA rules state: "In cases where requests or issues cannot be resolved by a given CNA, the issues are escalated to the next higher level CNA." Provide examples of the kinds of issues that might cause escalations. Also, create rule that requires some kind of paper trail for attempts to work with the CNA.
- Clarification around disclosure policies and what kinds of vulnerabilities (public, non-public, etc.) are given CVE IDs by the CNA and for what specific scope. Include a policy template. (Review the Embargo and Disclosure template)
- Clarify the difference between "when a vulnerability is made public" versus "when a vulnerability is added to the CVE list" and how they affect each other.
- Better describe the nested Root CNA structure (with a new diagram?).
  - Section 1.3: Clarify how to approach CNAs that are violating CNA Rules. Also, place limitations on sanctions (Perhaps "Any sanctions implemented by a Root CNA may be appealed up to the Primary CNA for adjudication.")
  - In Appendix B, clarify how to use the [VERSION] field. Use any of: Fixed-Version, Known-Affected-Version, Last-Affected-Version, First-Fixed-Version, etc. Adopt JSON standard here?
  - In Appendix B, remove "to the greatest level of detail available". As it is, this sounds like asking for full disclosure. Some may never provide details that can only be useful in constructing an exploit. The phrase "greatest level of detail" sounds unnecessary.
  - In Appendix B, give more examples that show how to handle multiple products or versions.
  - For Appendix C, INC2: Vulnerabilities intended to be private can become public.

I guess section 2.1.1 stated it better: "CVE IDs should only be assigned to vulnerabilities that are or will be made public."

  - For Appendix C, INC3: Suggestion this can be rephrased as:
  'Is it only in an online service (software-as-a-service), on a specific web site, or only offered through hosting solutions, where complete remediation of the vulnerability is under the full control of the vendor, and does not require any action from anyone else'.
  - For Appendix C, CNT3: 'Vulnerabilities in protocols' and 'vulnerabilities in protocol implementation' are two different beasts. Suggestion: make it 'vulnerabilities in protocol specifications "and" implementations'.
  - For Appendix C, CNT3: What about shared hardware or shared hardware architecture?

What about standard formats like file formats or data encoding formats?

OUTCOME: Less vague or confusing language.

______

GOAL:

CHANGE: Should we also allow projects/etc. to simply embed the data into their CNA listing, especially if it is "simple" (e.g. an Open Source project with a single software project, or a project with multiple projects that are well defined (e.g. within their GitHub organization) where they cover "everything" for example

OUTCOME:

______

GOAL:

CHANGE: Ensure some normalized format for the data, e.g. JSON? a simple list?

OUTCOME:

______

GOAL:

CHANGE: Ensure discoverability of the CNA coverage page (e.g. they list the URL in their CNA entry?)

OUTCOME:

______

GOAL:

CHANGE: Tie JSON updates schedule to CNA Rules update schedule.

OUTCOME:

______

GOAL: Add new required fields.

CHANGE: 
  - Should we make the publication date a required field? 
  - Should we make Impact a required field?

OUTCOME: Enrich the metadata included in CVE entries.

______

GOAL: Simplify assignment process

CHANGE: Just make CVE ID year the year it was assigned.

OUTCOME: Reduced overhead for getting a CVE ID with the correct year.  Reduced confusion by CVE consumers.

______

GOAL:  Make the CNA processes more standardized and repeatable.

CHANGE: Define when an entry be marked as disputed versus rejected.

OUTCOME:  Consistent results with defensible reasoning

______

GOAL: Transparency

CHANGE: The CVE List cannot be the first point of publication for any information.

OUTCOME:  Document current policy

______

GOAL:  Make the CNA processes more standardized and repeatable.

CHANGE Define how to handle third-party updates to a CNA's entry. References? Description changes?

OUTCOME: Set expectations, consistent results, and transparent processes.

______

GOAL:  Increase coverage

CHANGE:  Expand who can be a CNA (from CERTs, vendors, CCs).

OUTCOME:  Clarify requirements for becoming a CNA.  

______

GOAL:  Make the CNA processes more standardized and repeatable.

CHANGE:  Describe the annual review cycle for rejecting CVE IDs.

OUTCOME:  

______

GOAL:  

CHANGE:  Appendix B overhaul including what needs to be in the Description (product/version).

OUTCOME:

______

GOAL:  Make the CNA processes more standardized and repeatable.

CHANGE:  Define if and how CNAs assign CVE IDs to bundled third-party products.

OUTCOME:  Reduce duplicate, increased transparency in processes, and better quality entries.

WORDING:

    A product vendor may assign a CVE ID to a bundled product, if
    the producer of the bundled product is not a CNA
    they coordinate with the producer of the bundled product or
    (if contact with the producer fails) the Root CNA for the product.

______

GOAL:  Make the CNA Rules easier to use

CHANGE: Split CNT3 into a rule for codebases and another for standards, libraries, etc.

OUTCOME:  Increased clarity in the process.

WORDING:

- CNT3: Shared Codebase

      Affects a single product, assign one CVE ID
      Affects the same code in multiple products, assign a CVE ID to each affected codebase
      Affects multiple products but with different code, assign a CVE ID to each product
      Not sure or undefined, assign a CVE ID to each product
    
- CNT4: Libraries, Protocols, Standards, etc.

      Results from conforming to the specification, assign a single CVE ID.
      Results from a choice by the implementer, assign a CVE ID to each affected codebase.
      Not sure, assign a CVE ID to each affected codebase.
 
______

GOAL:  Make the CNA Rules easier to use

CHANGE: Add extra decision for the case when issues aren't independently fixable and when you aren't sure.

OUTCOME:  

WORDING:

- CNT1:

      If a vulnerability can be fixed independently of the others, go to CNT2.
      If the vulnerabilities cannot be fixed independently, group the bugs together and go to CNT2.
      If it is not clear whether the vulnerabilities can be fixed independently, group the bugs together and go to CNT2.

______

GOAL: Document existing policy

CHANGE: INC2 should be changed to clarify that the vulnerabilities that are already public can be assigned a CVE ID.

OUTCOME:  Reduced confusion.

______

GOAL: Increase adobption of CVE

CHANGE: Remove CVE ID assignment requirements for Root CNAs

OUTCOME:  Organizations willing to be a Root CNA but without the resources to handle CVE ID assignment will become join.

______

GOAL:  Clarify the CNA Rules

CHANGE: Rework the wording for INC4

OUTCOME:  The Counting Rules are easier to implement.

______

GOAL:  Incentivize proper behavior

CHANGE:  Change the issue resolution processes (Appendix E) to account for CNAs who violate the rules

OUTCOME:  Fewer rules violations

______

GOAL: Fix typos.

CHANGE:

- 2.2.9 has a typo at the end.

OUTCOME: Correct grammar and spelling.

______

GOAL: Better define terms.

CHANGE: 

  - Better define "hardware" with regard to CVE.
  - Go through the CNA docs and highlight some of the potentially undefined/problematic terms/phrases, e.g. "public disclosure" and so on is so that we can maybe define them better. 

OUTCOME: Regularized terminology.

______

GOAL: Improve process descriptions.

CHANGE:

  - Add references and rules updates regarding the CVE JSON format and its use.
  - The current CNA rules do not stipulate a specific time by which a CNA should update their upstream CNA after a CVE ID has been made public. MITRE asked the Board for guidance on the most time a CNA can wait. The Board suggested that CNAs should update their upstream CNAs within 24 hours of the publication of a CVE ID. This recommendation will be added to the list of updates to be considered for the next CNA Rules update.
  - Additionally, CVE IDs that have been reserved for long periods of time without any public assignment could be “REJECT”ed or labeled in some other way to indicate they are inactive in the CVE list.
  - Include rules describing how and when to assign CVE IDs using a year different from the current one.

http://cve.mitre.org/about/faqs.html#year_portion_of_cve_id

  - Add explicit how-to steps for submitting CVE entries to the Primary CNA.
  - Include rules explicitly describing when and how unused CVE IDs will be rejected each year.
  - How to assign for bundled third-party products.
  - A time limit for how long reserved CVE IDs can be held without any update to the CNA who issued them.
  - Sub CNAs can send CVE assignment information directly to the Primary CNA and not have to go through their Root CNA.

OUTCOME: CNAs will have clear processes to follow.

______

GOAL: Address reference formats in CNA rules.

CHANGE: Add descriptions and process for use of reference formats in CVE descriptions (e.g., MISC:, CONFIRM:, BUGTRAQ:, etc.)

OUTCOME: CNAs will make use of the reference formats to enrich the metadata surrounding entries.

______

GOAL: Include optional fields in CVE entry CSV and flat file submission standard.

CHANGE: Include [INITIALRELEASEDATE], [CURRENTRELEASEDATE], [CVSSSCORE], [ACKNOWLEDGEMENT], [PUBLISHER], [CWE], [CPE]. Should we rely on the JSON format to supply this instead?

OUTCOME: More metadata can be submitted in regularized formats.

______

GOAL: Notify requester when a CVE ID has been assigned.

CHANGE: Create a requirement that the original requester of a CVE ID will be notified when the CVE ID has been assigned.

OUTCOME: Improved communication between CNAs and CVE requesters.

_________________________________

11 July 2017

CVE Used vs. CVE assigned
Helps differentiate between what are actually assigned vs. those that are reserved and (maybe) unused.
The Primary CNA should be publishing these summaries.
The Root CNAs must provide the Primary CNA these data.
"Allocated" vs. "Reserved"?

Primary CNA will send periodic reports to the Root/Sub CNAs indicating what CVE IDs we have observed/had reported to us that have not been published.
One other option is a query on demand vs an email notification

For Automation WG: more publication notification tools, push or pull

JSON will become the preferred format for CVE assignment. This would be done through a migration process. Year-long?
JSON revision is tied to CNA Rules revision timeline

Add numbers to suggestions.

notification timeframes... what is a reasonable amount of time to expect details of CVE from CNA. Set as guideline with loose compliance. "notify immediately", but not a hard rule.

are the counting rules too flexible?










