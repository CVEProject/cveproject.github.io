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
[<u>the MITRE CVE site</u>](https://cve.mitre.org/cve/cve.html) and also by general web searches (at
any moment in time, not every assigned CVE ID is covered on the
cve.mitre.org web site). Also, if you have previously contacted
another organization on [<u>the CNA list</u>](https://cve.mitre.org/cve/cna.html), a
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

## Table of Contents


1. [Introduction](#introduction)
2. [Background](#background)
3. [Before Requesting a CVE Number](#before-requesting-a-cve-number)
4. [Following Coordinated Disclosure Practices](#following-coordinated-disclosure-practices)
5. [When to Request a CVE Number](#when-to-request-a-cve-number)
6. [Where to Request a CVE Number](#where-to-request-a-cve-number)
7. [Information to Provide in Your Request](#information-to-provide-in-your-request)
8. [Information That You Receive from the CNA (or MITRE)](#information-that-you-receive-from-the-cna-or-mitre)
9. [Sharing the CVE Number with Others](#sharing-the-cve-number-with-others)
10. [Information to Include in Your Announcement](#information-to-include-in-your-announcement)
11. [After Your Announcement Has Been Publicized](#after-your-announcement-has-been-publicized)


## 1. Introduction


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

## 2. Background

Following is some background information, which may help you to
understand the rationales for the process.

1. See [<u>the Identifiers page</u>](https://cve.mitre.org/cve/identifiers/index.html) for
   details on how vulnerabilities are included in CVE.

2. As more and more CVEs are included in announcements of new
   vulnerabilities, it can be more difficult to exchange CVEs
   across all involved parties.  This could increase the amount of
   "noise" in CVE.

3. If you do not use and share CVE numbers properly, then MITRE
   and other CVE Numbering Authorities (CNAs) will not provide
   them to you any more.  This reduces the risk of #2, and it helps to
   prevent abuse.

4. The CVE request process is designed so that it minimizes
   interference with the current disclosure process, e.g. posting to
   Bugtraq or Full-Disclosure.

5. The CVE request process is designed to minimize the amount of
   non-public vulnerability information that is available to MITRE.
   This reduces the risk of accidental disclosure of such information.
   It also reduces the amount of overlap with the work of other
   entities such as CERT/CC, Bugtraq, and Full-Disclosure.


## 3. Before Requesting a CVE Number

1. CVE numbers are ONLY for security issues that are going to be
   publicly announced.

2. You must make sure that your issue is not already a duplicate of an
   existing CVE entry by performing a keyword search on [<u>the CVE web
   site</u>](https://cve.mitre.org/cve/).

3. You should follow coordinated disclosure practices as described in
   the next section.

## 4. Following Coordinated Disclosure Practices

You should make a good faith effort to notify the affected vendor and
work with them to ensure that a patch is available.  Information is
more accurate and complete when researchers and vendors work together.

Improper disclosure practices have the following impact on CVE:

1. You may introduce inaccurate information, such as the affected
   versions or the underlying cause of the problem.

2. Your description of the problem could vary so much from that of the
   vendor, that duplicate CVE IDs may be produced - one for your
   description, and another for the vendor's.  This has happened in
   the past.

3. Without independent confirmation or vendor acknowledgement, members
   of the CVE Editorial Board may not be confident that the issue is
   real.


There are several documents that provide guidelines on disclosure,
such as the one at [<u>OISafety.org</u>](http://www.oisafety.org/) in PDF format.  See
Appendix A: Documents on Disclosure Practices for more details.


In general, you should do the following:

1. Find and notify the appropriate security contact for the vendor
   If you cannot find a contact, then try technical support.

2. Provide the vendor with at least 5 business days to respond and
   show that the vendor is aware of the problem.  An "auto-reply"
   email or other computer-generated response does not represent
   vendor awareness.

3. Work with the vendor to explain the problem, conduct further
   analysis if necessary, test any patches that the vendor proposes,
   and ensure the accuracy of your advisory - as well as the vendor's.

4. If the vendor is not responsive, then report the problem to a third
   party ("coordinator") such as CERT/CC.  These coordinators may have
   contacts with the vendor, or they may lend credibility to your
   report.

5. When possible, do not announce the vulnerability until the vendor
   has provided a patch.  This could take between 1 day and 6 months,
   depending on the vendor and the nature of the problem.  If you
   believe that the issue is urgent and the vendor is not responding
   quickly enough, then try using a coordinator as described in #4.

6. When possible, avoid releasing precise details of the vulnerability
   until system administrators have some time to apply the patch.

If an advisory will not be published by the vendor or an established
response team (e.g. CERT/CC), then you must announce the vulnerability
to a public forum that allows others to validate your claims.
Currently, those forums include the Bugtraq and Full-Disclosure
mailing lists, and sites like exploit-db and Packet Storm.


## 5. When to Request a CVE Number

You should request a CVE number after you have made a good faith
attempt to notify the vendor.

In general, you should request a CVE number 1 to 2 weeks before you
publicize the vulnerability.


## 6. Where to Request a CVE Number

You request a CVE number from a CVE Numbering Authority (CNA).  CNAs
obtain pools of "blank" candidate numbers from MITRE, and use those
pools to assign candidates to specific issues.  See [<u>the CNA list</u>](https://cve.mitre.org/cve/cna.html)
page.

Most major OS vendors use CVE numbers, even if they are not a CNA;
they generally obtain them from other CNAs.  You could ask them for a
CVE as well.


## 7. Information to Provide in Your Request

The information should be sent to: cve-assign@mitre.org

A CVE ID request must have sufficient information to determine the correct number of CVE IDs, and to categorize the product.

Specifically, there is no requirement to state the product name or vendor name. However, not all products are covered by CVE, and not all products can have CVE IDs from our CVE Assignment Team.

First, please confirm that cve-assign@mitre.org is the correct place to send your request. For a number of major vendors, the request must be sent directly to the vendor. See our [<u>"CNA List"</u>](https://cve.mitre.org/cve/cna.html) web page.

Second, please confirm that the vendor or product is listed on our [<u>"Product List"</u>](http://cve.mitre.org/cve/data_sources_product_coverage.html#products). This list represents the current coverage goals for the CVE program.

If you are able to confirm these, please ensure that your CVE ID request includes a wording similar to "The vendor is not on the CNA List. The vendor or product is on the Product List."

Here are a few notes about possible misunderstandings:

  - We assign CVE IDs for all products that have been packaged by a Linux distribution on our Product List, such as Debian or Fedora. It is not necessary for the specific product name to be listed on our "Product List."

  - We do not assign CVE IDs for software that may be optionally added to a listed product, such as a third-party plugin or module. For example, we assign CVE IDs for the WordPress core product but not for any WordPress plugin. We do not assign CVE IDs for an Android or iOS app unless the app's author is a listed vendor. We assign CVE IDs for a number of languages including Python and PHP, but not for all code written in those languages (e.g., we do not assign CVE IDs for a web application written in PHP, unless the product or vendor is separately listed).

  - If your request was about CVE IDs for multiple products, we need separate information about presence on the CNA List and Product List for each product.

You must state that you are actively working with the vendor to fix
the problem.  If the vendor is unresponsive, you should state this.

You may encrypt your communications using PGP or GnuPG (gpg), with
the following cve-assign@mitre.org PGP key, which can be downloaded
from various PGP key servers:

    -----BEGIN PGP PUBLIC KEY BLOCK-----
	Version: GnuPG v1

	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
	=N2Ok
	-----END PGP PUBLIC KEY BLOCK-----


## 8. Information That You Receive from the CNA (or MITRE)

After you send your request, MITRE will reserve the CVE number(s) and
provide them to you.  Generic, "blank" descriptions will be added to
the CVE entries, and the blank entries will be published on the CVE
web site.

NOTE: to reduce the risk of accidental disclosure of vulnerability
information before it is publicized, MITRE does not record any
vulnerability information with the CVEs it has assigned to your
security issue.  You must inform MITRE once you have publicized the
vulnerability.  See below.


## 9. Sharing the CVE Number with Others

After you have obtained the CVE number, you should provide it to
all affected vendors and other parties (such as CERT/CC) that you are
communicating with.  This reduces the risk that different parties may
assign different numbers.


## 10. Information to Include in Your Announcement

When you make your public announcement, include the CVE number
in the text.

You can include a paragraph such as the following:

  The Common Vulnerabilities and Exposures (CVE) project has assigned
  the name CVE-YYYY-NNNN to this issue. This is an entry on [<u>the CVE
  list</u>](https://cve.mitre.org), which standardizes names for security
  problems.

If you can not include this text due to space limitations, then try to
include a URL to the CVE:

   https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-YYYY-NNNN

You can also just say something like:

    CVE Number: CVE-yyyy-nnnn

1. Make sure that the CVE number is correct.  Some advisories have
   been released with incorrect numbers, occasionally due to typos.

2. If you are announcing more than one CVE number, then list each
   number followed by a short title (only a few words), so that people
   can easily tell which candidate is related to which issue.  For
   example:

      CVE-yyyy-nnnn - buffer overflows
      CVE-yyyy-mmmm - format string

3. OSF (an organization separate from MITRE) offers suggestions about
   other content in the announcement:

    [https://blog.osvdb.org/2013/01/15/researcher-security-advisory-writing-guidelines](https://blog.osvdb.org/2013/01/15/researcher-security-advisory-writing-guidelines)


## 11. After Your Announcement Has Been Publicized

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

The CVE information will also be updated in [<u>the National Vulnerability
Database (NVD)</u>](https://nvd.nist.gov).



## Appendix A: Documents on Disclosure Practices

The following documents describe processes for vulnerability
disclosure practices that lead to more accurate CVE entries.

1.  "Guidelines for Security Vulnerability Reporting and Response",
    Organization for Internet Safety.  Version 2.0, 01 September 2004.

      [http://www.oisafety.org/](http://www.oisafety.org/)  
      [http://www.symantec.com/security/OIS_Guidelines%20for%20responsible%20disclosure.pdf](http://www.symantec.com/security/OIS_Guidelines%20for%20responsible%20disclosure.pdf)

2. "Vulnerability Disclosure Framework", US Department of Homeland
    Security.  January 2004.

      [http://www.dhs.gov/xlibrary/assets/vdwgreport.pdf](http://www.dhs.gov/xlibrary/assets/vdwgreport.pdf)

3. "Responsible Vulnerability Disclosure Process", IETF draft
   document, Christey/Wysopal.  February 2002.

      [http://tools.ietf.org/html/draft-christey-wysopal-vuln-disclosure-00](http://tools.ietf.org/html/draft-christey-wysopal-vuln-disclosure-00)

4. "RFPolicy 2.0", Rain Forest Puppy.  2000.

      [http://packetstormsecurity.org/files/view/23364/rfpolicy-2.0.txt](http://packetstormsecurity.org/files/view/23364/rfpolicy-2.0.txt)
