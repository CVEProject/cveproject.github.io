---
title: 'CVE Content Decisions: Application Guidance for CNAs'

layout: page
---

CVE Content Decisions: Application Guidance for CNAs
====================================================

*Author: Steve Christey Coley\
Last Modified: November 20, 2014\
*

This document provides guidance to CVE Candidate Numbering Authorities
(CNAs) to help them determine how many CVE identifiers to assign to a
set of issues.

This guidance only applies to CVE assignment that occurs BEFORE
DISCLOSURE. MITRE must be consulted after disclosure, and has additional
rules that may be followed.

CVE Assignment Might Be Different Than You Expect
=================================================

Following this guidance is essential. It might not recommend what you
expect. People count vulnerabilities differently, which can lead to
different methods for how to assign CVE identifiers. However, because
there are multiple CNAs, it is important to follow these guidelines in
order to guarantee consistency between the CNAs.

This guidance is mostly based on well-established CVE rules called
"content decisions." These help CVE to be consistent, even when the
amount of details can vary widely across different disclosures, or when
knowledge changes across time within a single disclosure. These have
emerged over years, but they have proven to be repeatable - if followed
properly.

For background information, go to:

[CVE Abstraction Content Decisions: Rationale and
Application](http://cve.mitre.org/cve/editorial_policies/cd_abstraction.html)

Index
=====

-   [INCLUSION Decision
    Tree](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#inclusion) -
    how to determine if an issue should receive a CVE
-   [ABSTRACTION Decision
    Tree](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#abstraction) -
    how many CVE numbers must be assigned, and how related issues should
    be grouped together
-   [Appendix: Handling More Than 2 Issues At
    Once](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#mult) -
    when you might be dealing with more than 2 issues
-   [Appendix: Large-Scale
    Disclosures](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#largescale) -
    when many products and vendors are affected
-   [Complex Abstraction
    Scenarios](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#complexAB) -
-   [Final Pre-Disclosure Checklist for
    CVE](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#checklist) -
-   [Frequently Asked
    Questions (FAQ)](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#FAQ)
-   [Examples](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#examples)

[]()

INCLUSION Decision Tree
=======================

Use this decision tree to determine if a bug/issue should be assigned a
CVE.

The possible conclusions for this decision tree are:

-   ASSIGN: - the issue should be assigned a CVE identifier.
-   CONSULT: - DO NOT assign a CVE identifier; instead, consult MITRE
    (issue is complex)

+--------------------------------------+--------------------------------------+
| **INC1:**                            | Does exploitation of the issue       |
|                                      | provide the attacker with extra      |
|                                      | privileges or information, or cause  |
|                                      | a denial of service, that the        |
|                                      | attacker would not already have      |
|                                      | before they attempt to exploit the   |
|                                      | issue?                               |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** Continue to INC2        |
|                                      | -   **No:** Do not assign a CVE.     |
|                                      | -   **Not sure:** **CONSULT** MITRE  |
+--------------------------------------+--------------------------------------+
| **INC2:**                            | Has the issue already been reported  |
|                                      | to a public source that is easily    |
|                                      | accessible from the Internet? (e.g.  |
|                                      | Bugtraq, vulnerability database,     |
|                                      | blog entry, vendor changelog, web    |
|                                      | bulletin board or newsgroup, open    |
|                                      | source bug entry, or a               |
|                                      | product-specific mailing list)       |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** Do not assign a CVE.    |
|                                      |     **CONSULT** MITRE                |
|                                      | -   **No:** Continue to INC3         |
+--------------------------------------+--------------------------------------+
| **INC3:**                            | Is the issue site-specific? Is it    |
|                                      | only in an online service            |
|                                      | (software-as-a-service), on a        |
|                                      | specific web site, or only offered   |
|                                      | through hosting solutions that are   |
|                                      | under the full control of the        |
|                                      | vendor?                              |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** Do not assign a CVE.    |
|                                      |     **CONSULT** MITRE                |
|                                      | -   **No:** Continue to INC4         |
+--------------------------------------+--------------------------------------+
|                                      | *Relevant content decisions:         |
|                                      | EX-ONLINE-SVC*                       |
+--------------------------------------+--------------------------------------+
| **INC4:**                            | Does the issue only affect a version |
|                                      | that was never made generally        |
|                                      | available to the vendor's customers? |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** Do not assign a CVE.    |
|                                      | -   **No:** **ASSIGN** a CVE         |
|                                      | -   **Not sure:** **CONSULT** MITRE  |
+--------------------------------------+--------------------------------------+

[]()

ABSTRACTION Decision Tree
=========================

Use this decision tree to determine how many different CVE identifiers
should be assigned to a set of issues. You must address ALL items in the
decision tree before making a final decision.

Consider two issues - whether distinct bugs or attack vectors. Assume
they satisfy the INCLUSION decision tree. Call them X and Y.

The possible conclusions for this decision tree are:

-   **SPLIT** - assign separate CVE identifiers to X and Y
-   **MERGE** - assign the same CVE identifier to both X and Y (i.e.
    combine them)
-   **CONSULT** - DO NOT assign a CVE identifier; instead, consult MITRE
    (issue is complex)

A separate
[document](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application-examples.html)
lists multiple examples of this decision tree.

**

-   to do: handling exploits with multiple vuln chains

**

+--------------------------------------+--------------------------------------+
| **\***                               | Are there more than 2 bugs, issues,  |
|                                      | or attack vectors?                   |
+--------------------------------------+--------------------------------------+
|                                      | -   **No:** Continue to ADT1.        |
|                                      | -   **Yes:** See the Appendix on     |
|                                      |     ["Handling More Than 2 Issues At |
|                                      |     Once"](http://cvecmssrv1.mitre.o |
|                                      | rg/cve-content/content-docs/cd-appli |
|                                      | cation.html#mult)                    |
+--------------------------------------+--------------------------------------+
| **ADT1:**                            | *(By codebase)*\                     |
|                                      | Does X affect at least one different |
|                                      | product than Y?                      |
+--------------------------------------+--------------------------------------+
|                                      | -   **No:** Continue to ADT2.        |
|                                      | -   **Yes:**                         |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT1.1:**                    |
|                                      |        | Does the same vendor offer  |
|                                      | both      |                          |
|                                      |     |                                |
|                                      |        | products?                   |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 1.2.      |                          |
|                                      |     |                                |
|                                      |        | -   **Yes:**                |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     +---------------------- |
|                                      | --------- |                          |
|                                      |     |                                |
|                                      |        | -------+------------------- |
|                                      | --------- |                          |
|                                      |     |                                |
|                                      |        | ----------+                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     | **ADT1.1.1:**         |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        | Is there strong ev |
|                                      | idence th |                          |
|                                      |     |                                |
|                                      |        | at X and  |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     |                       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        | Y are the exact sa |
|                                      | me bug, e |                          |
|                                      |     |                                |
|                                      |        | .g. the   |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     |                       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        | products share the |
|                                      |  same lib |                          |
|                                      |     |                                |
|                                      |        | rary?     |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     +---------------------- |
|                                      | --------- |                          |
|                                      |     |                                |
|                                      |        | -------+------------------- |
|                                      | --------- |                          |
|                                      |     |                                |
|                                      |        | ----------+                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     |                       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        | -   **Yes:** **MER |
|                                      | GE** them |                          |
|                                      |     |                                |
|                                      |        | .         |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     |                       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        |     Continue to AD |
|                                      | T1.2      |                          |
|                                      |     |                                |
|                                      |        |           |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     |                       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        | -   **No:** **SPLI |
|                                      | T** them. |                          |
|                                      |     |                                |
|                                      |        |  Continue |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     |                       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        |     to ADT1.2      |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |           |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     |                       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |        | -   **Not Sure:**  |
|                                      | Continue  |                          |
|                                      |     |                                |
|                                      |        | to ADT1.2 |                 |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        |     +---------------------- |
|                                      | --------- |                          |
|                                      |     |                                |
|                                      |        | -------+------------------- |
|                                      | --------- |                          |
|                                      |     |                                |
|                                      |        | ----------+                 |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT1.2:**                    |
|                                      |        | Do the two products share t |
|                                      | he same   |                          |
|                                      |     |                                |
|                                      |        | codebase in which X and Y a |
|                                      | ppear,    |                          |
|                                      |     |                                |
|                                      |        | such as a library or execut |
|                                      | able, or  |                          |
|                                      |     |                                |
|                                      |        | third-party software that i |
|                                      | s used by |                          |
|                                      |     |                                |
|                                      |        | many vendors?               |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** Jump to ADT2   |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 1.3       |                          |
|                                      |     |                                |
|                                      |        | -   **Not Sure:** **CONSULT |
|                                      | ** MITRE  |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT1.3:**                    |
|                                      |        | Is this a large-scale probl |
|                                      | em that   |                          |
|                                      |     |                                |
|                                      |        | affects many vendors and    |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | products? (e.g. a new class |
|                                      |  of       |                          |
|                                      |     |                                |
|                                      |        | vulnerability or attack, or |
|                                      |  results  |                          |
|                                      |     |                                |
|                                      |        | from fuzz testing many prod |
|                                      | ucts)     |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 2         |                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** Jump to specia |
|                                      | l         |                          |
|                                      |     |                                |
|                                      |        |     appendix on [Large-Scal |
|                                      | e         |                          |
|                                      |     |                                |
|                                      |        |     Disclosures](http://cve |
|                                      | cmssrv1.m |                          |
|                                      |     |                                |
|                                      |        | itre.org/cve-content/conten |
|                                      | t-docs/cd |                          |
|                                      |     |                                |
|                                      |        | -application.html#largescal |
|                                      | e).       |                          |
|                                      |     |                                |
|                                      |        | -   **Not Sure:** **CONSULT |
|                                      | ** MITRE  |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
+--------------------------------------+--------------------------------------+
|                                      | *Relevant content decisions:         |
|                                      | SF-CODEBASE*                         |
+--------------------------------------+--------------------------------------+
| **ADT2:**                            | *(By bug type)*\                     |
|                                      | Are X and Y different bug types?     |
|                                      | (e.g. buffer overflow, SQL           |
|                                      | injection, NULL pointer              |
|                                      | dereference?) See [Guidance on       |
|                                      | Identifying Different Bug            |
|                                      | Types](http://cve.mitre.org/cve/edit |
|                                      | orial_policies/cd_abstraction.html#i |
|                                      | dentifying_different_bug_types)      |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** **SPLIT** them.         |
|                                      | -   **No:** Continue to ADT3         |
|                                      | -   **Not sure:**                    |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT2.1:**                    |
|                                      |        | Are they both "unspecified" |
|                                      | , i.e.,   |                          |
|                                      |     |                                |
|                                      |        | no details are available ab |
|                                      | out what  |                          |
|                                      |     |                                |
|                                      |        | programming error caused th |
|                                      | e bugs?   |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** Jump to ADT3   |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 2.2       |                          |
|                                      |     |                                |
|                                      |        | -   **Not Sure:** This opti |
|                                      | on is not |                          |
|                                      |     |                                |
|                                      |        |     applicable for this que |
|                                      | stion.    |                          |
|                                      |     |                                |
|                                      |        |     Decide "Yes" or "No" ba |
|                                      | sed on    |                          |
|                                      |     |                                |
|                                      |        |     the information that yo |
|                                      | u         |                          |
|                                      |     |                                |
|                                      |        |     currently have availabl |
|                                      | e to you. |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT2.2:**                    |
|                                      |        | Is X's bug type known, but  |
|                                      | Y's bug   |                          |
|                                      |     |                                |
|                                      |        | type is unspecified?        |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** **SPLIT** them |
|                                      | .         |                          |
|                                      |     |                                |
|                                      |        |     Continue to ADT2.3.     |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 2.3       |                          |
|                                      |     |                                |
|                                      |        | -   **Not Sure:** This opti |
|                                      | on is not |                          |
|                                      |     |                                |
|                                      |        |     applicable for this que |
|                                      | stion.    |                          |
|                                      |     |                                |
|                                      |        |     Decide "Yes" or "No" ba |
|                                      | sed on    |                          |
|                                      |     |                                |
|                                      |        |     the information that yo |
|                                      | u         |                          |
|                                      |     |                                |
|                                      |        |     currently have availabl |
|                                      | e to you. |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT2.3:**                    |
|                                      |        | Does X appear in a protecti |
|                                      | on        |                          |
|                                      |     |                                |
|                                      |        | mechanism that tries to pre |
|                                      | vent bug  |                          |
|                                      |     |                                |
|                                      |        | type T, and Y is of type T, |
|                                      |  but Y    |                          |
|                                      |     |                                |
|                                      |        | has no protection mechanism |
|                                      |  at all?  |                          |
|                                      |     |                                |
|                                      |        | (Needs Work)                |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** **SPLIT** them |
|                                      | .         |                          |
|                                      |     |                                |
|                                      |        |     Continue to ADT3        |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** **CONSULT** MIT |
|                                      | RE        |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
+--------------------------------------+--------------------------------------+
|                                      | *Relevant content decisions: AB1*    |
+--------------------------------------+--------------------------------------+
| **ADT3:**                            | *(By version)*\                      |
|                                      | Does X affect a version that Y does  |
|                                      | not? (e.g. X affects 1.2 and 3.4,    |
|                                      | but Y only affects 3.4. Consider     |
|                                      | "1.x" and "1.2" as different.)       |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** **SPLIT** them.         |
|                                      | -   **No:** Continue to ADT4         |
|                                      | -   **Not sure:**                    |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT3.1:**                    |
|                                      |        | Is an official vendor patch |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | available for X, but Y does |
|                                      |  not have |                          |
|                                      |     |                                |
|                                      |        | an official patch (or Y's p |
|                                      | atch      |                          |
|                                      |     |                                |
|                                      |        | status is unknown)?         |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** **SPLIT** them |
|                                      | .         |                          |
|                                      |     |                                |
|                                      |        |     Continue to ADT3.2      |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 3.2       |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT3.2:**                    |
|                                      |        | Does X affect a general ran |
|                                      | ge (such  |                          |
|                                      |     |                                |
|                                      |        | as "4.x") and Y's version i |
|                                      | s more    |                          |
|                                      |     |                                |
|                                      |        | specific (such as "4.1")?   |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** **SPLIT** them |
|                                      | .         |                          |
|                                      |     |                                |
|                                      |        |     Continue to ADT3.3      |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 3.3       |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT3.3:**                    |
|                                      |        | Does X's minimum affected v |
|                                      | ersion    |                          |
|                                      |     |                                |
|                                      |        | differ from Y's minimum aff |
|                                      | ected     |                          |
|                                      |     |                                |
|                                      |        | version, but the maximum ve |
|                                      | rsions    |                          |
|                                      |     |                                |
|                                      |        | are the same?               |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** **SPLIT** them |
|                                      | /         |                          |
|                                      |     |                                |
|                                      |        |     Continue to ADT3.4      |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** Continue to ADT |
|                                      | 3.4       |                          |
|                                      |     |                                |
|                                      |        | -   **Not sure:** **MERGE** |
|                                      |  them     |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **ADT3.4:**                    |
|                                      |        | Is X the result of an incom |
|                                      | plete fix |                          |
|                                      |     |                                |
|                                      |        | for Y, or X is a new vulner |
|                                      | ability   |                          |
|                                      |     |                                |
|                                      |        | that was introduced by a fi |
|                                      | x for Y?  |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** **SPLIT** them |
|                                      | .         |                          |
|                                      |     |                                |
|                                      |        |     Continue to ADT4        |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** **CONSULT** MIT |
|                                      | RE.       |                          |
|                                      |     |                                |
|                                      |        |     Continue to ADT4        |
|                                      |           |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
+--------------------------------------+--------------------------------------+
|                                      | *Relevant content decisions: AB2*    |
+--------------------------------------+--------------------------------------+
| **ADT4:**                            | *(Address Common SPLIT               |
|                                      | Assumptions)*\                       |
|                                      | At this stage, X and Y are the same  |
|                                      | bug type, affect the same versions,  |
|                                      | and affect the same products.        |
|                                      | Do X and Y have any of the following |
|                                      | characteristics?                     |
|                                      |                                      |
|                                      | -   X appears in a different DLL,    |
|                                      |     library, program, or application |
|                                      |     than Y (e.g. X affects LIB1.DLL  |
|                                      |     and Y affects LIB2.DLL)          |
|                                      | -   X has a more serious impact than |
|                                      |     Y (e.g. code execution as root   |
|                                      |     versus leak of system pathname)  |
|                                      | -   X takes a different input        |
|                                      |     parameter/argument than Y (e.g.  |
|                                      |     SQL injection in both the "user" |
|                                      |     and "password" parameters)       |
|                                      | -   X has a different "access        |
|                                      |     vector" than Y (e.g. local,      |
|                                      |     remote, "adjacent network,"      |
|                                      |     physical, etc.)                  |
|                                      | -   X requires stronger              |
|                                      |     authentication than Y.           |
|                                      | -   X can be exploited by a certain  |
|                                      |     user that Y can not (e.g. a      |
|                                      |     guest user vs. an admin)         |
|                                      | -   X has a different CVSS score     |
|                                      |     than Y (e.g. due to different    |
|                                      |     access vector, attack            |
|                                      |     complexity, or CIA impact)       |
|                                      | -   X uses a different service,      |
|                                      |     port, or protocol than Y (e.g.,  |
|                                      |     UDP versus TCP)                  |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** **MERGE** them. These   |
|                                      |     characteristics are irrelevant   |
|                                      |     for CVE. Continue to ADT5        |
|                                      | -   **No:** Continue to ADT5         |
+--------------------------------------+--------------------------------------+
|                                      | *Relevant content decisions: AB3,    |
|                                      | SF-LOC, SF-EXEC*                     |
+--------------------------------------+--------------------------------------+
| **ADT5:**                            | *(By researcher)*\                   |
|                                      | Is X reported by a different person  |
|                                      | from a different organization (or    |
|                                      | other external party) than Y?        |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** **SPLIT** them.         |
|                                      |     Continue to ADT6                 |
|                                      | -   **No:** **CONSULT** MITRE        |
+--------------------------------------+--------------------------------------+
| **ADT6:**                            | *(Fall-Through Merge)*\              |
|                                      | At this stage, you have multiple     |
|                                      | closely-related vulnerabilities,     |
|                                      | issues, or attack vectors.           |
+--------------------------------------+--------------------------------------+
|                                      | -   **MERGE** them.                  |
+--------------------------------------+--------------------------------------+

[]()

Appendix: Handling More Than 2 Issues At Once
=============================================

When assigning CVEs for groups of more than 2 issues, use the following
basic process:

+--------------------------------------+--------------------------------------+
| **MULT1:**                           | -   Remove any issues that should be |
|                                      |     excluded (see INCLUSION          |
|                                      |     decision tree).                  |
+--------------------------------------+--------------------------------------+
| **MULT2:**                           | -   Group the issues based on        |
|                                      |     different bug types and          |
|                                      |     affected versions. See questions |
|                                      |     2 and 3 in the                   |
|                                      |     ABSTRACTION guidelines.          |
+--------------------------------------+--------------------------------------+
| **MULT3:**                           | -   For each remaining group with    |
|                                      |     more than one issue, apply the   |
|                                      |     rest of the ABSTRACTION          |
|                                      |     guidelines to each issue within  |
|                                      |     each group.                      |
+--------------------------------------+--------------------------------------+
| **MULT4:**                           | -   **SPLIT** each group from the    |
|                                      |     other groups.                    |
+--------------------------------------+--------------------------------------+
| **MULT5:**                           | -   **MERGE** the issues that are    |
|                                      |     within a multi-issue group.      |
+--------------------------------------+--------------------------------------+

### Example Table

For example, suppose you have issues V1, V2, V3, V4, and V5, which have
different affected versions and bug types. Your table might look
something like:

  Bug type        Version       Issues
  --------------- ------------- ------------
  XSS             1.0           V1
  XSS             1.0 and 2.0   V2, V3, V4
  SQL injection   2.0           V5

One multi-issue group remains: V2/V3/V4. Apply the ABSTRACTION CDs to
that group.

V1 and V5 would be split from this group. []()

Appendix: Large-Scale Disclosures
=================================

When dealing with large-scale problems, use the following item in
addition to the regular decision tree.

+--------------------------------------+--------------------------------------+
| **LP1:**                             | Is it an implementation problem      |
|                                      | where many products accidentally     |
|                                      | make the same mistake? (examples:    |
|                                      | certificates, FTP user overflows)    |
+--------------------------------------+--------------------------------------+
|                                      | -   **No:** See next question.       |
|                                      | -   **Yes:**                         |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     | **LP1.1:**                     |
|                                      |        | Do you have solid knowledge |
|                                      |  of which |                          |
|                                      |     |                                |
|                                      |        | vendors and products are af |
|                                      | fected,   |                          |
|                                      |     |                                |
|                                      |        | and their codebase relation |
|                                      | ships?    |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
|                                      |     |                                |
|                                      |        | -   **Yes:** **SPLIT** base |
|                                      | d on      |                          |
|                                      |     |                                |
|                                      |        |     related vendors/product |
|                                      | s, then   |                          |
|                                      |     |                                |
|                                      |        |     apply other CDs for bug |
|                                      |  type and |                          |
|                                      |     |                                |
|                                      |        |     affected versions       |
|                                      |           |                          |
|                                      |     |                                |
|                                      |        | -   **No:** **CONSULT** MIT |
|                                      | RE        |                          |
|                                      |     |                                |
|                                      |        | -   **Not sure:** **CONSULT |
|                                      | ** MITRE  |                          |
|                                      |     +------------------------------- |
|                                      | -------+---------------------------- |
|                                      | ----------+                          |
+--------------------------------------+--------------------------------------+
| **LP2:**                             | Is it a fundamental problem with the |
|                                      | design or protocol? That is, does    |
|                                      | every implementation have this       |
|                                      | problem because it must conform to   |
|                                      | the design/protocol?                 |
+--------------------------------------+--------------------------------------+
|                                      | -   **Yes:** **MERGE** them          |
|                                      | -   **No:** **CONSULT** MITRE        |
|                                      | -   **Not Sure:** **CONSULT** MITRE  |
+--------------------------------------+--------------------------------------+

[]()

[Complex Abstraction Scenarios]()
=================================

[]()

Vulnerability and Attack Chains
-------------------------------

-   When dealing with multiple issues that are chained together, a
    general rule to use is: "if one issue is fixed, then does it
    automatically fix the second issue?" If so, then the first issue is
    probably the "root cause," and only one CVE would be needed. But if
    the second issue could still exist even after the first is fixed,
    then likely both of them need separate issues.
-   If bug X creates a condition that introduces bug Y - e.g., an
    integer overflow that leads to a buffer overflow - then you need to
    consider whether X, on its own, would be a vulnerability. In the
    case of an integer overflow leading to a buffer overflow, the
    integer overflow would not be a problem on its own; it is simply an
    incorrect calculation.
-   Consider issues X and Y. Suppose the attacker can exploit X in order
    to gain privilege P. Then, using P, the attacker can exploit Y. In
    this case, the primary question is whether a valid user with
    privilege P already has the capability to perform Y. For example,
    consider a web application in which any remote, unauthenticated
    attacker can call an administrator function that modifies web pages;
    the attacker then modifies the web page to insert an HTML
    injection (XSS) attack. Here, an administrator is already allowed to
    modify HTML; the admin is already have the legitimate privileges to
    insert arbitrary HTML or Javascript code into the page, so to an
    admin there is no extra benefit to attempting an XSS. As a result,
    only one CVE would be assigned - to the web application's lack of
    access control to the admin function - and the XSS would be
    "resultant" from that.

Variants, Incomplete Fixes, and Regression Errors
-------------------------------------------------

**Variants.** Generally, if an issue X is fixed in one software version,
but a new variant, Y, is discovered that affects the new version, these
are typically SPLIT. The reason is that X and Y affect different
versions.

**Regression Errors.** Regression errors are generally SPLIT. For the
purpose of CVE, a specific issue is called a regression error when:

-   the issue appears in a version (e.g., 3.1).
-   the issue is fixed in a subsequent version (e.g., 3.2).
-   a CVE ID is assigned for this issue.
-   at a later time, the exact same issue re-appears in a later version
    (e.g., 3.4).

In this case, a separate CVE ID would then be assigned.

The rationale is that since there was a fixed version between 3.1 and
3.4, CVE consumers and CVE-compatible tools have likely associated the
CVE with only version 3.1, applied patches that are only associated with
version 3.1, etc. So, the assignment of a separate CVE ID for the issue
in version 3.4 acts as a "signal" that there is a different issue that
requires a distinct action.

**Later identification of additional affected versions.** When an issue
is published with one set of versions, and later it is reported that
other versions are also affected, this typically will result in a MERGE
(with a CVE description update), except for regression errors as
outlined previously.

Here are a few common scenarios in which additional versions might be
announced at a later time:

-   if the vendor is maintaining multiple ranges of versions
    simultaneously, such as a legacy major version 2.x that is still
    being actively maintained and a modern major version 3.x, the vendor
    might announce the vulnerability before all version ranges have
    been patched. Other affected major versions might have their fixes
    published days, weeks, or months later. This is not considered a
    regression error, but instead, a clarification of the set of
    affected versions for the original bug; as long as the same bug is
    being patched, a new CVE would not need to be assigned for these
    additional versions.
-   A researcher who does not coordinate closely with a vendor might
    publicize a vulnerability with incomplete version information, e.g.
    if they were analyzing an older version of the software. Later, the
    vendor (or another researcher) might publish that other, later
    versions are also affected. Typically, no new CVE would be
    necessary, as long as there are not any apparent fixes in between
    the original version and the more recently-announced version (which
    would suggest a regression error); ideally, the CVE description
    would be updated with the new version information.

Common Assumptions That Frequently Lead to Assignment Errors
============================================================

-   **One remote, one local.** I have two buffer overflows in the
    same product. One is exploitable remotely, and one is
    exploitable locally. Should I SPLIT them?
    -   No (rather, these would stay merged based only on these
        two criteria). ADT1 would not split - it's the same product.
        ADT2 would not split - it's the same bug type. ADT3 woud not
        split - it's the same affected version. However ADT4, explicitly
        says that the two issues should stay MERGED even if they have a
        different "access vector."
-   **Different bugs in different executables.** I have two bugs of the
    same type in an open source product, such as SQL injection. There
    are two separate patches, in parameter X in executable A, and in
    parameter Y in executable B. These are clearly different bugs.
    Should I SPLIT them?
    -   No. They are in the same product, so ADT1 would not split. They
        are the same bug type, SQL injection, so ADT2 would not split.
        They affect the same version, so ADT3 would not split. Also,
        ADT4 explicitly says that the issues should stay merged when "X
        appears in a different DLL, library, program, or application
        than Y."
-   **Different Impacts.** I have two bugs, both directory traversal,
    affecting the same product versions. One allows me to delete files,
    and the other allows me to read files. Should I SPLIT them?
    -   No. By ADT1, there is no split since the bugs are in the
        same product. There also is no split for the same bug
        type (ADT2) and affected versions (ADT3). Finally, ADT4
        explicitly recommends merge when "X has a more serious impact
        than Y."

[]()

Frequently Asked Questions (FAQ)
================================

### Changing CVEs Assignments After Discovering New Information

-   I assigned a CVE, but later analysis showed that the issue is not
    a vulnerability. The initial bug report was never publicly
    disclosed. Can I re-assign the CVE to another issue?
    -   Probably not, especially if you have shared the CVE ID with any
        other external party. Consult MITRE.
-   I MERGED several issues into a single CVE, but after disclosure, it
    became clear that these should have been SPLIT. What should be done
    about this?
    -   Work with MITRE on determining whether a SPLIT should be
        performed; if so, MITRE will do so.
-   I've learned about a duplicate CVE. What should I do? Which CVE
    should I use?
    -   Consult MITRE; only MITRE, as the Primary CNA, can decide which
        ID to use when a duplicate occurs. (We generally follow the
        process as documented
        in https://cve.mitre.org/cve/editorial\_policies/duplicates.html).

### Limited Disclosure Policy

-   I have a disclosure policy where I don't release specific details
    about vulnerabilities, such as the type of vulnerability. How do I
    assign CVEs?
-   I have a disclosure policy where I don't focus on issues when I
    don't think they're important enough for my customers. Do I have to
    assign a CVE to those issues?

[]()

Final Pre-Disclosure Checklist for CVE
======================================

Shortly before disclosure, follow this checklist for each CVE:

  ----------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Share the CVE:**            Make sure that you've shared the CVE with all parties who are involved in the disclosure. This reduces the chance of duplicates.
  **Avoid typos:**              Make sure that none of your CVE numbers contain typos. One way to do this is to ensure that the CVE web site lists the "RESERVED" string in each of their descriptions.
  **Multiple CVEs assigned:**   Ensure that your advisory clearly indicates which CVEs are associated with which issues.
  **New issues discovered:**    If new issues were found during the disclosure process, see if you need to SPLIT or MERGE them with the CVEs you already assigned.
  **Early disclosure:**         If the issue has already been publicly disclosed, even in a vague way, check with MITRE. Search the CVE or NVD web sites to be sure.
  ----------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------

[]()

CVE COntent Decision Examples
=============================

See [this
document](http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application-examples.html)
which lists multiple examples for CD application. []()

Changelog
=========

Date

Comment

September 17, 2008

Initial creation

September 10, 2012

Added fall-through "Continue to \[X\]" options to make fall-through more
clear.

April 19, 2013

Added and clarified characteristics for ADT4, added additional
fall-through options.

November 20, 2014

Improved explanation of "Application Examples" page.

Added "Complex Abstraction Scenarios" section.

expanded "Common Assumptions" section.
