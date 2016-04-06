---
title: Researcher Reservation Guidelines
layout: page
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


Other text from our recent "Reservation Guidelines for Researchers"
including steps that occur before and after reservation:

* You should really coordinate with the vendor, including sharing CVE
  numbers.  Information quality is much better that way, and it
  reduces the chance of duplicate CVEs.

* You can encrypt your request using the cve-assign@mitre.org PGP key,
  available from the usual places and in this message.

* We don't release any details until they're public.

* If you have multiple CVEs, make sure that your advisory makes it
  clear about which CVE goes with which issue.

==========================================================================
<br>Table of Contents<br>
==========================================================================

1. Introduction
2. Background
3. Before Requesting a CVE Number
4. Following Coordinated Disclosure Practices
5. When to Request a CVE Number
6. Where to Request a CVE Number
7. Information to Provide in Your Request
8. Information That You Receive from the CNA (or MITRE)
9. Sharing the CVE Number with Others
10. Information to Include in Your Announcement
11. After Your Announcement Has Been Publicized

==========================================================================
<br>1. Introduction<br>
==========================================================================

This document provides vulnerability researchers with information on
how to reserve a CVE number before publicizing a new vulnerability.
CVE reservation allows researchers to include candidate numbers in the
initial public announcement of the vulnerability.  It ensures that the
CVE number is instantly available to all CVE users and makes it easier
to track vulnerabilities over time.

The basic process is:

1. You REQUEST one or more CVE numbers.
2. MITRE RESERVES the CVE numbers and provides them to you.
3. You share these CVE numbers with all parties
4. You include the CVE number in your announcement of the
   vulnerability.
5. You notify MITRE that the CVE has been made public.
6. The CVE later appears on the cve.mitre.org web site.

==========================================================================
<br>2. Background<br>
==========================================================================

Following is some background information, which may help you to
understand the rationales for the process.

1) See http://cve.mitre.org/cve/identifiers/index.html for
   details on how vulnerabilities are included in CVE.

2) As more and more CVEs are included in announcements of new
   vulnerabilities, it can be more difficult to exchange CVEs
   across all involved parties.  This could increase the amount of
   "noise" in CVE.

3) If you do not use and share CVE numbers properly, then MITRE
   and other CVE Numbering Authorities (CNAs) will not provide
   them to you any more.  This reduces the risk of #2, and it helps to
   prevent abuse.

4) The CVE request process is designed so that it minimizes
   interference with the current disclosure process, e.g. posting to
   Bugtraq or Full-Disclosure.

5) The CVE request process is designed to minimize the amount of
   non-public vulnerability information that is available to MITRE.
   This reduces the risk of accidental disclosure of such information.
   It also reduces the amount of overlap with the work of other
   entities such as CERT/CC, Bugtraq, and Full-Disclosure.


==========================================================================
<br>3. Before Requesting a CVE Number<br>
==========================================================================

1) CVE numbers are ONLY for security issues that are going to be
   publicly announced.

2) You must make sure that your issue is not already a duplicate of an
   existing CVE entry by performing a keyword search on the CVE web
   site at http://cve.mitre.org/cve/ .

3) You should follow coordinated disclosure practices as described in
   the next section.


==========================================================================
<br>4. Following Coordinated Disclosure Practices<br>
==========================================================================

You should make a good faith effort to notify the affected vendor and
work with them to ensure that a patch is available.  Information is
more accurate and complete when researchers and vendors work together.

Improper disclosure practices have the following impact on CVE:

1) You may introduce inaccurate information, such as the affected
   versions or the underlying cause of the problem.

2) Your description of the problem could vary so much from that of the
   vendor, that duplicate CVE IDs may be produced - one for your
   description, and another for the vendor's.  This has happened in
   the past.

3) Without independent confirmation or vendor acknowledgement, members
   of the CVE Editorial Board may not be confident that the issue is
   real.


There are several documents that provide guidelines on disclosure,
such as the one at http://www.oisafety.org/ in PDF format.  See
Appendix A: Documents on Disclosure Practices for more details.


In general, you should do the following:

1) Find and notify the appropriate security contact for the vendor
   If you cannot find a contact, then try technical support.

2) Provide the vendor with at least 5 business days to respond and
   show that the vendor is aware of the problem.  An "auto-reply"
   email or other computer-generated response does not represent
   vendor awareness.

3) Work with the vendor to explain the problem, conduct further
   analysis if necessary, test any patches that the vendor proposes,
   and ensure the accuracy of your advisory - as well as the vendor's.

4) If the vendor is not responsive, then report the problem to a third
   party ("coordinator") such as CERT/CC.  These coordinators may have
   contacts with the vendor, or they may lend credibility to your
   report.

5) When possible, do not announce the vulnerability until the vendor
   has provided a patch.  This could take between 1 day and 6 months,
   depending on the vendor and the nature of the problem.  If you
   believe that the issue is urgent and the vendor is not responding
   quickly enough, then try using a coordinator as described in #4.

6) When possible, avoid releasing precise details of the vulnerability
   until system administrators have some time to apply the patch.

If an advisory will not be published by the vendor or an established
response team (e.g. CERT/CC), then you must announce the vulnerability
to a public forum that allows others to validate your claims.
Currently, those forums include the Bugtraq and Full-Disclosure
mailing lists, and sites like exploit-db and Packet Storm.


==========================================================================
<br>5. When to Request a CVE Number<br>
==========================================================================

You should request a CVE number after you have made a good faith
attempt to notify the vendor.

In general, you should request a CVE number 1 to 2 weeks before you
publicize the vulnerability.


==========================================================================
<br>6. Where to Request a CVE Number<br>
==========================================================================

You request a CVE number from a CVE Numbering Authority (CNA).  CNAs
obtain pools of "blank" candidate numbers from MITRE, and use those
pools to assign candidates to specific issues.  See
http://cve.mitre.org/cve/cna.html for a list.

Most major OS vendors use CVE numbers, even if they are not a CNA;
they generally obtain them from other CNAs.  You could ask them for a
CVE as well.


==========================================================================
<br>7. Information to Provide in Your Request<br>
==========================================================================

The information should be sent to: cve-assign@mitre.org

You do not necessarily need to reveal the product or vendor names, as
long as there is sufficient information to determine the correct
number of CVE IDs.

However, the request will have much higher priority if you explain
its relationship to the CVE coverage goals stated at:

  http://cve.mitre.org/cve/data_sources_product_coverage.html

There are three aspects to this:

  - Is the product on the "Must-Have Products" list?

  - Does the vendor plan to announce the vulnerability fix within
    a source on the "Full Coverage Sources - Vendor Related" or
    "Partial Coverage Sources - Vendor Related" list?

  - Do you plan to announce your vulnerability discovery within
    a source on the "Full Coverage Sources - Other" or
    "Partial Coverage Sources - Other" list?

You must state that you are actively working with the vendor to fix
the problem.  If the vendor is unresponsive, you should state this.

You may encrypt your communications using PGP or GnuPG (gpg), with
the following cve-assign@mitre.org PGP key, which can be downloaded
from various PGP key servers:

- -----BEGIN PGP PUBLIC KEY BLOCK-----
Version: GnuPG v1

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
z2alm8YFAk7nvkLSXfEveHr/EtVm3kM=
=v/YW
- -----END PGP PUBLIC KEY BLOCK-----


==========================================================================
<br>8. Information That You Receive from the CNA (or MITRE)<br>
==========================================================================

After you send your request, MITRE will reserve the CVE number(s) and
provide them to you.  Generic, "blank" descriptions will be added to
the CVE entries, and the blank entries will be published on the CVE
web site.

NOTE: to reduce the risk of accidental disclosure of vulnerability
information before it is publicized, MITRE does not record any
vulnerability information with the CVEs it has assigned to your
security issue.  You must inform MITRE once you have publicized the
vulnerability.  See below.


==========================================================================
<br>9. Sharing the CVE Number with Others<br>
==========================================================================

After you have obtained the CVE number, you should provide it to
all affected vendors and other parties (such as CERT/CC) that you are
communicating with.  This reduces the risk that different parties may
assign different numbers.


==========================================================================
<br>10. Information to Include in Your Announcement<br>
==========================================================================

When you make your public announcement, include the CVE number
in the text.

You can include a paragraph such as the following:

  The Common Vulnerabilities and Exposures (CVE) project has assigned
  the name CVE-YYYY-NNNN to this issue. This is an entry on the CVE
  list (http://cve.mitre.org), which standardizes names for security
  problems.

If you can not include this text due to space limitations, then try to
include a URL to the CVE:

   http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-YYYY-NNNN

You can also just say something like:

  CVE Number: CVE-yyyy-nnnn

1) Make sure that the CVE number is correct.  Some advisories have
   been released with incorrect numbers, occasionally due to typos.

2) If you are announcing more than one CVE number, then list each
   number followed by a short title (only a few words), so that people
   can easily tell which candidate is related to which issue.  For
   example:

      CVE-yyyy-nnnn - buffer overflows
      CVE-yyyy-mmmm - format string

3) OSF (an organization separate from MITRE) offers suggestions about
   other content in the announcement:

    http://blog.osvdb.org/2013/01/15/researcher-security-advisory-writing-guidelines


==========================================================================
<br>11. After Your Announcement Has Been Publicized<br>
==========================================================================

After your announcement has been publicized, you should contact MITRE
again (cve-assign@mitre.org) and provide us with the following
information:

  - The CVE number(s) you used in the announcement
  - The public forum(s) or advisories where the announcement can be
    found

Until you provide this information to MITRE, only a "blank" entry
may be recorded on the CVE web site.  As described in section 7,
MITRE may not have the details of the vulnerability.

MITRE will then update the CVE information on the CVE web site with a
proper description, references, etc.

The CVE information will also be updated in the National Vulnerability
Database (NVD) at http://nvd.nist.gov.



==========================================================================
<br>Appendix A: Documents on Disclosure Practices<br>
==========================================================================

The following documents describe processes for vulnerability
disclosure practices that lead to more accurate CVE entries.

1)  "Guidelines for Security Vulnerability Reporting and Response",
    Organization for Internet Safety.  Version 2.0, 01 September 2004.

      http://www.oisafety.org/
      http://www.symantec.com/security/OIS_Guidelines%20for%20responsible%20disclosure.pdf

2) "Vulnerability Disclosure Framework", US Department of Homeland
    Security.  January 2004.

      http://www.dhs.gov/xlibrary/assets/vdwgreport.pdf

3) "Responsible Vulnerability Disclosure Process", IETF draft
   document, Christey/Wysopal.  February 2002.

      http://tools.ietf.org/html/draft-christey-wysopal-vuln-disclosure-00

4) "RFPolicy 2.0", Rain Forest Puppy.  2000.

      http://packetstormsecurity.org/files/view/23364/rfpolicy-2.0.txt
