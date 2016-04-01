
---

title: Researcher Reservation Guidelines

---

Here is the current description of how CVE reservation requests occur,
along with information about closely related parts of the CVE process.

The main elements of the reservation process are:

1. Someone sends cve-assign@mitre.org sufficient information
to determine the correct number of new CVE IDs.

2. We send an e-mail response that provides one or more CVE IDs
and an indication of which vulnerability information is
associated with which ID.

Here are the five factors that most often affect determination of the
correct number of new CVE IDs:

A. Duplicate search. Duplicates may be found by searching
http://cve.mitre.org/cve/cve.html and also by general web searches (at
any moment in time, not every assigned CVE ID is covered on the
cve.mitre.org web site). Also, if you have previously contacted
another organization on the http://cve.mitre.org/cve/cna.html list, a
CVE ID assignment may already exist and should not be duplicated.

B. Scope of CVE. CVE IDs are for cases in which the primary method of
addressing the vulnerability is for individual product users to take
an action to update their own copy of the product. (CVE IDs are not
for cases in which the primary method of addressing the vulnerability
is for an action to be taken by the operator of a single web site or
online service.)

C. Establishing a policy violation. CVE IDs are for cases in which the
vendor agrees (or it is essentially certain that a vendor would agree)
that the observed product behavior violates a security policy, such as
an unintended loss of confidentiality, integrity, or availability.
(CVE IDs are not for cases in which a reporter unilaterally believes
that product hardening is desirable, such as a different approach to
abuse prevention or a different display of security-relevant data.)

D. Establishing how the vulnerabilities differ. For example, in cases
of multiple findings reported at the same time for a single product,
separate CVE IDs are needed for each difference in primary
vulnerability type, set of affected versions, or discoverer.

E. Cross-vendor coordination. Separate CVE IDs are not assigned solely
because vulnerable code is shipped in more than one product.
Especially in the case of open-source software, it is common for
multiple vendors to use the same CVE ID in any scenario in which they
have bundled, repackaged, or copied a piece of vulnerable code.

Other text from our recent “Reservation Guidelines for Researchers”
including steps that occur before and after reservation:

-   You should really coordinate with the vendor, including sharing CVE
    numbers. Information quality is much better that way, and it
    reduces the chance of duplicate CVEs.

<!-- -->

-   You can encrypt your request using the cve-assign@mitre.org PGP key,
    available from the usual places and in this message.

<!-- -->

-   We don’t release any details until they’re public.

<!-- -->

-   If you have multiple CVEs, make sure that your advisory makes it
    clear about which CVE goes with which i

