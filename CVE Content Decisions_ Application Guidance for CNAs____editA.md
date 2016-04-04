
<!-- saved from url=(0072)http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html -->
<html><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"><title>CVE Content Decisions: Application Guidance for CNAs</title>
</head><body bgcolor="FFFFFF">

<h1>CVE Content Decisions: Application Guidance for CNAs</h1>

<i>

Last Modified: November 20, 2014<br>
</i>

<p>

This document provides guidance to CVE Candidate Numbering Authorities
(CNAs) to help them determine how many CVE identifiers to assign to a
set of issues.

</p><p>

This guidance only applies to CVE assignment that occurs <u>BEFORE
DISCLOSURE.</u> MITRE must be consulted after disclosure, and has
additional rules that may be followed.

</p><p>

</p><h1>
<font color="FF0000">CVE Assignment Might Be Different Than You
Expect</font>
</h1>


Following this guidance is essential.  It might not recommend what you
expect.  People count vulnerabilities differently, which can lead to
different methods for how to assign CVE identifiers.  However, because
there are multiple CNAs, it is important to follow these guidelines in
order to guarantee consistency between the CNAs.

<p>

This guidance is mostly based on well-established CVE rules called
"content decisions."  These help CVE to be consistent, even when the
amount of details can vary widely across different disclosures, or
when knowledge changes across time within a single disclosure.  These
have emerged over years, but they have proven to be repeatable - if
followed properly.

</p><p>

For background information, go to:

</p><p>

<a target="_blank" href="http://cve.mitre.org/cve/editorial_policies/cd_abstraction.html">
CVE Abstraction Content Decisions: Rationale and Application
</a>


</p><h1>Index</h1>

<ul>
<li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#inclusion">INCLUSION Decision Tree</a> - how to
determine if an issue should receive a CVE

</li><li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#abstraction">ABSTRACTION Decision Tree</a> - how many CVE
numbers must be assigned, and how related issues should be grouped
together

</li><li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#mult">Appendix: Handling More Than 2 Issues At Once</a>
- when you might be dealing with more than 2 issues

</li><li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#largescale">Appendix: Large-Scale Disclosures</a> - when many
products and vendors are affected

</li><li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#complexAB">Complex Abstraction Scenarios</a> - 


</li><li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#checklist">Final Pre-Disclosure Checklist for CVE</a> - 

</li><li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#FAQ">Frequently Asked Questions (FAQ)</a>

</li><li><a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#examples">Examples</a>


</li></ul>

<p>

<a name="inclusion"></a>

</p><h1>INCLUSION Decision Tree</h1>

Use this decision tree to determine if a bug/issue should be assigned
a CVE.

<p>

The possible conclusions for this decision tree are:

</p><ul>

<li><font color="FF0000">ASSIGN:</font> - the issue should be assigned a
CVE identifier.

</li><li><font color="FF0000">CONSULT:</font> - DO NOT assign a CVE
identifier; instead, consult MITRE (issue is complex)

</li></ul>

<p>


<table border="5" cellpadding="2" cellspacing="2">

<tbody><tr><td bgcolor="E0E0E0"><b>INC1:</b>
</td><td bgcolor="E0E0E0">

Does exploitation of the issue provide the attacker with extra
privileges or information, or cause a denial of service, that the
attacker would not already have before they attempt to exploit the
issue?

  </td></tr><tr><td></td><td>
    <ul>
	<li><b>Yes:</b> Continue to INC2
	</li><li><b>No:</b> Do not assign a CVE.
	</li><li><b>Not sure:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
	</li></ul>


</td></tr><tr><td bgcolor="E0E0E0"><b>INC2:</b>
</td><td bgcolor="E0E0E0">

Has the issue already been reported to a public source that is easily
accessible from the Internet?  (e.g. Bugtraq, vulnerability database,
blog entry, vendor changelog, web bulletin board or newsgroup, open
source bug entry, or a product-specific mailing list)

  </td></tr><tr><td></td><td>
    <ul>
	<li><b>Yes:</b> Do not assign a CVE.
	<font color="FF0000"><b>CONSULT</b></font> MITRE
	</li><li><b>No:</b> Continue to INC3
	</li></ul>

</td></tr><tr><td bgcolor="E0E0E0"><b>INC3:</b>
</td><td bgcolor="E0E0E0">

Is the issue site-specific?  Is it only in an online service
(software-as-a-service), on a specific web site, or only offered
through hosting solutions that are under the full control of the
vendor?

  </td></tr><tr><td></td><td>
    <ul>
	<li><b>Yes:</b> Do not assign a CVE.
	<font color="FF0000"><b>CONSULT</b></font> MITRE
	</li><li><b>No:</b> Continue to INC4
	</li></ul>

</td></tr><tr><td></td><td>
<i>Relevant content decisions: EX-ONLINE-SVC</i>

</td></tr><tr><td bgcolor="E0E0E0"><b>INC4:</b>
</td><td bgcolor="E0E0E0">

Does the issue only affect a version that was never made generally
available to the vendor's customers?

  </td></tr><tr><td></td><td>
    <ul>
	<li><b>Yes:</b> Do not assign a CVE.
	</li><li><b>No:</b> <font color="FF0000"><b>ASSIGN</b></font> a CVE
	</li><li><b>Not sure:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
	</li></ul>


</td></tr></tbody></table>


</p><p>


<a name="abstraction"></a>

</p><h1>ABSTRACTION Decision Tree</h1>


<p>

Use this decision tree to determine how many different CVE identifiers
should be assigned to a set of issues.  You must address ALL items in
the decision tree before making a final decision.


</p><p>

Consider two issues - whether distinct bugs or attack vectors.  Assume
they satisfy the INCLUSION decision tree.  Call them X and Y.

</p><p>

The possible conclusions for this decision tree are:

</p><ul>

<li><font color="FF0000"><b>SPLIT</b></font> - assign separate CVE identifiers
to X and Y

</li><li><font color="FF0000"><b>MERGE</b></font> - assign the same CVE identifier
to both X and Y (i.e. combine them)

</li><li><font color="FF0000"><b>CONSULT</b></font> - DO NOT assign a CVE
identifier; instead, consult MITRE (issue is complex)

</li></ul>

<p>
A separate <a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application-examples.html">document</a> lists
multiple examples of this decision tree.
</p>


<p>
<i></i>
</p>


<ul><i>
<li>to do: handling exploits with multiple vuln chains</li>
</i></ul>

<i></i>

<p>
</p>


<p>

<table border="5" cellpadding="2" cellspacing="2">
<tbody>

	<tr>
		<td bgcolor="E0E0E0"><b>*</b></td>
		<td bgcolor="E0E0E0">
		Are there more than 2 bugs, issues, or attack vectors?
		</td>
	</tr>

	<tr>
		<td></td>
		<td>
		  <ul>
		  <li><b>No:</b> Continue to ADT1.</li>
		  <li><b>Yes:</b> See the Appendix on
		  <a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#mult">"Handling More Than 2 Issues At Once"</a>
		  </li>
		  </ul>
		</td>
	</tr>

	<tr>
		<td bgcolor="E0E0E0"><b>ADT1:</b></td>
		<td bgcolor="E0E0E0"><i>(By codebase)</i><br>
		Does X affect at least one different product than Y?
		</td>
	</tr>

	<tr>
	<td></td>
		<td>
		  <ul><li><b>No:</b> Continue to ADT2.</li>
		  <li><b>Yes:</b>

			<table border="2" cellpadding="2" cellspacing="2">
			<tbody>
			
				 <tr>
					 <td bgcolor="E0E0E0"><b>ADT1.1.1:</b></td>
					 
					 <td bgcolor="E0E0E0">
					 Is there strong evidence that X and Y are the exact same bug,
					 e.g. the products share the same library?
					 </td>
				 </tr>
				 
				 <tr>
					 <td></td>
					 
					 <td>
					  <ul>
						  <li><b>Yes:</b> <font color="FF0000"><b>MERGE</b></font> them.
						  Continue to ADT1.2
						  </li>
						  
						  <li><b>No:</b> <font color="FF0000"><b>SPLIT</b></font> them.
						  Continue to ADT1.2
						  </li>
						  
						  <li>
						  <b>Not Sure:</b> Continue to ADT1.2
						  </li>
					  </ul>
					 </td>
				 </tr>
			 </tbody>
			 </table>
		  </li>
		  </ul>
		</td>
	</tr>
	
	<tr>
		<td bgcolor="E0E0E0"><b>ADT1.2:</b></td>
		<td bgcolor="E0E0E0">
		Do the two products share the same codebase in which X and Y
		appear, such as a library or executable, or third-party software
		that is used by many vendors?
		</td>
	</tr>
	
	<tr>
		<td></td>
		
		<td>
		  <ul>
			<li><b>Yes:</b> Jump to <u>ADT2</u></li>
			<li><b>No:</b> Continue to ADT1.3</li>
			<li><b>Not Sure:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE</li>
		  </ul>
		</td>
	</tr>
	
	<tr>
		<td bgcolor="E0E0E0"><b>ADT1.3:</b></td>
		<td bgcolor="E0E0E0">
		Is this a large-scale problem that affects many vendors and
		products?  (e.g. a new class of vulnerability or attack, or
		results from fuzz testing many products)
		</td>
	</tr>
	
	<tr>
		<td></td>
		<td>
		  <ul>
			  <li><b>No:</b> Continue to ADT2</li>
			  <li><b>Yes:</b> Jump to special appendix on <a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application.html#largescale">Large-Scale Disclosures</a>.</li>
			  <li><b>Not Sure:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE</li>
		  </ul> 
		</td>
	</tr>
  

  
	
 </li>
 </ul>

</td>
</tr>

<tr>
<td></td>

<td>
<i>Relevant content decisions: SF-CODEBASE</i>

</td>
</tr>










<tr><td bgcolor="E0E0E0"><b>ADT2:</b>
</td><td bgcolor="E0E0E0">
<i>(By bug type)</i><br>
Are X and Y different bug types? (e.g. buffer overflow, SQL injection,
NULL pointer dereference?)
See
<a href="http://cve.mitre.org/cve/editorial_policies/cd_abstraction.html#identifying_different_bug_types">
Guidance on Identifying Different Bug Types</a>

</td></tr><tr><td></td><td>
  <ul>
  <li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them.
  </li><li><b>No:</b>  Continue to ADT3
  </li><li><b>Not sure:</b>
     <table border="2" cellpadding="2" cellspacing="2">
     <tbody><tr><td bgcolor="E0E0E0"><b>ADT2.1:</b>
	 </td><td bgcolor="E0E0E0">
	 Are they both "unspecified", i.e., no details are available about
	 what programming error caused the bugs?
     </td></tr><tr><td></td><td>
	     <ul>
		 <li><b>Yes:</b> Jump to <u>ADT3</u>
		 </li><li><b>No:</b> Continue to ADT2.2
		 </li><li><b>Not Sure:</b> This option is not applicable
		 for this question.  Decide "Yes" or "No" based on the
		 information that you currently have available to you.
		 </li></ul>
      </td></tr><tr><td bgcolor="E0E0E0"><b>ADT2.2:</b>
	  </td><td bgcolor="E0E0E0">
	  Is X's bug type known, but Y's bug type is unspecified?
	  </td></tr><tr><td></td><td>
	    <ul>
		<li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them.
		Continue to ADT2.3.
		</li><li><b>No:</b> Continue to ADT2.3
		 </li><li><b>Not Sure:</b> This option is not applicable
		 for this question.  Decide "Yes" or "No" based on the
		 information that you currently have available to you.
		</li></ul>

      </td></tr><tr><td bgcolor="E0E0E0"><b>ADT2.3:</b>
	  </td><td bgcolor="E0E0E0">

	  Does X appear in a protection mechanism that tries to prevent
	  bug type T, and Y is of type T, but Y has no protection
	  mechanism at all?	 <font color="FF0000">(Needs Work)</font>
	  </td></tr><tr><td></td><td>
	    <ul>
		<li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font>
		them.  Continue to ADT3
		</li><li><b>No:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
		</li></ul>
	</td></tr></tbody></table>
  </li></ul>

</td></tr><tr><td></td><td>
<i>Relevant content decisions: AB1</i>

</td></tr><tr><td bgcolor="E0E0E0"><b>ADT3:</b>
</td><td bgcolor="E0E0E0">
<i>(By version)</i><br>
Does X affect a version that Y does not?  (e.g. X affects 1.2 and 3.4,
but Y only affects 3.4.  Consider "1.x" and "1.2" as different.)

</td></tr><tr><td></td><td>
  <ul>
  <li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them.
  </li><li><b>No:</b>  Continue to ADT4
  </li><li><b>Not sure:</b>
     <table border="2" cellpadding="2" cellspacing="2">
     <tbody><tr><td bgcolor="E0E0E0"><b>ADT3.1:</b>
	 </td><td bgcolor="E0E0E0">

	 Is an official vendor patch available for X, but Y does not have
     an official patch (or Y's patch status is unknown)?

     </td></tr><tr><td></td><td>
	     <ul>
		 <li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them.
		 Continue to ADT3.2
		 </li><li><b>No:</b> Continue to ADT3.2
		 </li></ul>

      </td></tr><tr><td bgcolor="E0E0E0"><b>ADT3.2:</b>
	  </td><td bgcolor="E0E0E0">
	  Does X affect a general range (such as "4.x") and Y's version is
	  more specific (such as "4.1")?
	  </td></tr><tr><td></td><td>
	    <ul>
		<li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them.
		Continue to ADT3.3
		</li><li><b>No:</b> Continue to ADT3.3
		</li></ul>

      </td></tr><tr><td bgcolor="E0E0E0"><b>ADT3.3:</b>
	  </td><td bgcolor="E0E0E0">
	  Does X's minimum affected version differ from Y's minimum
	  affected version, but the maximum versions are the same?
	  </td></tr><tr><td></td><td>
	    <ul>
		<li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them/
		Continue to ADT3.4
		</li><li><b>No:</b> Continue to ADT3.4
		</li><li><b>Not sure:</b> <font color="FF0000"><b>MERGE</b></font> them
		</li></ul>
      </td></tr><tr><td bgcolor="E0E0E0"><b>ADT3.4:</b>
	  </td><td bgcolor="E0E0E0">
	  Is X the result of an incomplete fix for Y, or X is a new
	  vulnerability that was introduced by a fix for Y?
	  </td></tr><tr><td></td><td>
	    <ul>
		<li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them.
		Continue to ADT4
		</li><li><b>No:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE.
		Continue to ADT4
		</li></ul>
	</td></tr></tbody></table>
  </li></ul>


</td></tr><tr><td></td><td>
<i>Relevant content decisions: AB2</i>


</td></tr><tr><td bgcolor="E0E0E0"><b>ADT4:</b>
</td><td bgcolor="E0E0E0">
<i>(Address Common SPLIT Assumptions)</i><br>
At this stage, X and Y are the same bug type, affect the same
versions, and affect the same products.

<p>

Do X and Y have any of the following characteristics?

</p><ul>

<li>X appears in a different DLL, library, program, or application
than Y (e.g. X affects LIB1.DLL and Y affects LIB2.DLL)

</li><li>X has a more serious impact than Y (e.g. code execution as root
versus leak of system pathname)

</li><li>X takes a different input parameter/argument than Y (e.g. SQL
injection in both the "user" and "password" parameters)

</li><li>X has a different "access vector" than Y (e.g. local, remote,
"adjacent network," physical, etc.)

</li><li>X requires stronger authentication than Y.

</li><li>X can be exploited by a certain user that Y can not (e.g. a guest
user vs. an admin)

</li><li>X has a different CVSS score than Y (e.g. due to different access
vector, attack complexity, or CIA impact)

</li><li>X uses a different service, port, or protocol than Y (e.g., UDP
versus TCP)

</li></ul>

  </td></tr><tr><td></td><td>
    <ul>
	<li><b>Yes:</b> <font color="FF0000"><b>MERGE</b></font> them.
	These characteristics are irrelevant for CVE.  Continue to
	ADT5
	</li><li><b>No:</b> Continue to ADT5
	</li></ul>


</td></tr><tr><td></td><td>
<i>Relevant content decisions: AB3, SF-LOC, SF-EXEC</i>

</td></tr><tr><td bgcolor="E0E0E0"><b>ADT5:</b>
</td><td bgcolor="E0E0E0">

<p>
<i>(By researcher)</i><br>

Is X reported by a different person from a different organization (or
other external party) than Y?

  </p></td></tr><tr><td></td><td>
    <ul>
	<li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> them.
	Continue to ADT6
	</li><li><b>No:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
	</li></ul>




</td></tr><tr><td bgcolor="E0E0E0"><b>ADT6:</b>
</td><td bgcolor="E0E0E0">

<p>
<i>(Fall-Through Merge)</i><br>

At this stage, you have multiple closely-related vulnerabilities,
issues, or attack vectors.

</p></td></tr><tr><td></td><td>

 <ul>
 <li><font color="FF0000"><b>MERGE</b></font> them.
 </li></ul>

</td></tr></tbody></table>

<a name="mult"></a>
</p><h1>Appendix: Handling More Than 2 Issues At Once</h1>

When assigning CVEs for groups of more than 2 issues, use the
following basic process:

<p>


<table border="2" cellpadding="2" cellspacing="2">
<tbody><tr><td bgcolor="E0E0E0"><b>MULT1:</b>
</td><td>
<ul>
<li>Remove any issues that should be excluded (see INCLUSION decision
tree).
</li></ul>
</td></tr><tr><td bgcolor="E0E0E0"><b>MULT2:</b>
</td><td>
<ul>
<li> Group the issues based on different bug types and affected
    versions.  See questions 2 and 3 in the ABSTRACTION guidelines.
</li></ul>

</td></tr><tr><td bgcolor="E0E0E0"><b>MULT3:</b>
</td><td>

<ul>
<li>For each remaining group with more than one issue, apply the rest of
the ABSTRACTION guidelines to each issue within each group.
</li></ul>

</td></tr><tr><td bgcolor="E0E0E0"><b>MULT4:</b>
</td><td>

<ul>
<li><font color="FF0000"><b>SPLIT</b></font> each group from the other
groups.
</li></ul>

</td></tr><tr><td bgcolor="E0E0E0"><b>MULT5:</b>
</td><td>

<ul>
<li><font color="FF0000"><b>MERGE</b></font> the issues that are within
a multi-issue group.
</li></ul>

</td></tr></tbody></table>


</p><h3>Example Table</h3>

For example, suppose you have issues V1, V2, V3, V4, and V5, which
have different affected versions and bug types.  Your table might look
something like:

<p>

<table border="2" cellpadding="2" cellspacing="2">
<tbody><tr><th>Bug type</th><th>Version</th><th>Issues
</th></tr><tr>
<td>XSS</td><td>1.0</td><td>V1
</td></tr><tr>
<td>XSS</td><td>1.0 and 2.0</td><td>V2, V3, V4
</td></tr><tr>
<td>SQL injection</td><td>2.0</td><td>V5
</td></tr></tbody></table>

</p><p>

One multi-issue group remains: V2/V3/V4.  Apply the ABSTRACTION CDs to
that group.

</p><p>

V1 and V5 would be split from this group.



<a name="largescale"></a>
</p><h1>Appendix: Large-Scale Disclosures</h1>


When dealing with large-scale problems, use the following item in
addition to the regular decision tree.

<p>

<table border="5" cellpadding="2" cellspacing="2">
    <tbody><tr><td bgcolor="E0E0E0"><b>LP1:</b>
	</td><td bgcolor="E0E0E0">

	Is it an implementation problem where many products
    accidentally make the same mistake?  (examples: certificates, FTP
    user overflows)

	</td></tr><tr><td></td><td>
    <ul>
	<li><b>No:</b> See next question.
	</li><li><b>Yes:</b>

	  <table border="2" cellpadding="2" cellspacing="2">
	      <tbody><tr><td bgcolor="E0E0E0"><b>LP1.1:</b>
		  </td><td bgcolor="E0E0E0">
		  Do you have solid knowledge of which vendors and products
		  are affected, and their codebase relationships?
		  </td></tr><tr><td></td><td>
		  <ul>
		  <li><b>Yes:</b> <font color="FF0000"><b>SPLIT</b></font> based
		  on related vendors/products, then apply other CDs for bug
		  type and affected versions
		  </li><li><b>No:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
		  </li><li><b>Not sure:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
	  </li></ul></td></tr></tbody></table>
  	</li></ul>

	</td></tr><tr><td bgcolor="E0E0E0"><b>LP2:</b>
    </td><td bgcolor="E0E0E0">

	Is it a fundamental problem with the design or protocol?  That
    is, does every implementation have this problem because it must
    conform to the design/protocol?


	</td></tr><tr><td></td><td>
    <ul>
	<li><b>Yes:</b> <font color="FF0000"><b>MERGE</b></font> them
	</li><li><b>No:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
	</li><li><b>Not Sure:</b> <font color="FF0000"><b>CONSULT</b></font> MITRE
	</li></ul>
	
</td></tr></tbody></table>


<a name="complexAB">
</a></p><h1><a name="complexAB">Complex Abstraction Scenarios</a></h1><a name="complexAB">
</a>

<h2>Vulnerability and Attack Chains</h2>

<p>

</p><ul>

  <li>When dealing with multiple issues that are chained together, a
  general rule to use is: "if one issue is fixed, then does it
  automatically fix the second issue?"  If so, then the first issue is
  probably the "root cause," and only one CVE would be needed.  But if
  the second issue could still exist even after the first is fixed,
  then likely both of them need separate issues.

  </li><li>If bug X creates a condition that introduces bug Y - e.g., an
  integer overflow that leads to a buffer overflow - then you need to
  consider whether X, on its own, would be a vulnerability.  In the
  case of an integer overflow leading to a buffer overflow, the
  integer overflow would not be a problem on its own; it is simply an
  incorrect calculation.

  </li><li>Consider issues X and Y.  Suppose the attacker can exploit X in
  order to gain privilege P.  Then, using P, the attacker can exploit
  Y.  In this case, the primary question is whether a valid user with
  privilege P already has the capability to perform Y.  For example,
  consider a web application in which any remote, unauthenticated
  attacker can call an administrator function that modifies web pages;
  the attacker then modifies the web page to insert an HTML injection
  (XSS) attack.  Here, an administrator is already allowed to modify
  HTML; the admin is already have the legitimate privileges to insert
  arbitrary HTML or Javascript code into the page, so to an admin
  there is no extra benefit to attempting an XSS.  As a result, only
  one CVE would be assigned - to the web application's lack of access
  control to the admin function - and the XSS would be "resultant"
  from that.


</li></ul>

<h2>Variants, Incomplete Fixes, and Regression Errors</h2>

<p>

<b>Variants.</b>  Generally, if an issue X is
fixed in one software version, but a new variant, Y, is discovered
that affects the new version, these are typically SPLIT.  The reason
is that X and Y affect different versions.

</p><p>

<b>Regression Errors.</b>  Regression errors are
generally SPLIT.  For the purpose of CVE, a specific issue is called a
regression error when:
</p><ul>
<li> the issue appears in a version (e.g., 3.1).
</li><li> the issue is fixed in a subsequent version (e.g., 3.2).
</li><li> a CVE ID is assigned for this issue.
</li><li> at a later time, the exact same issue re-appears in a later version
(e.g., 3.4).
  </li></ul>

In this case, a separate CVE ID would then be assigned.

<p>
  
The rationale is that since there was a fixed version between 3.1 and
3.4, CVE consumers and CVE-compatible tools have likely associated the
CVE with only version 3.1, applied patches that are only associated
with version 3.1, etc.  So, the assignment of a separate CVE ID for
the issue in version 3.4 acts as a "signal" that there is a different
issue that requires a distinct action.
</p><p>

<b>Later identification of additional affected versions.</b>  When an
issue is published with one set of versions, and later it is reported
that other versions are also affected, this typically will result in a
MERGE (with a CVE description update), except for regression errors as
outlined previously.

</p><p>

Here are a few common scenarios in which additional versions might be
announced at a later time:

</p><ul>

  <li>if the vendor is maintaining multiple ranges of versions
  simultaneously, such as a legacy major version 2.x that is still
  being actively maintained and a modern major version 3.x, the vendor
  might announce the vulnerability before all version ranges have been
  patched.  Other affected major versions might have their fixes
  published days, weeks, or months later.  This is not considered a
  regression error, but instead, a clarification of the set of
  affected versions for the original bug; as long as the same bug is
  being patched, a new CVE would not need to be assigned for these
  additional versions.

  </li><li>A researcher who does not coordinate closely with a vendor might
  publicize a vulnerability with incomplete version information,
  e.g. if they were analyzing an older version of the software.
  Later, the vendor (or another researcher) might publish that other,
  later versions are also affected.  Typically, no new CVE would be
  necessary, as long as there are not any apparent fixes in between
  the original version and the more recently-announced version (which
  would suggest a regression error); ideally, the CVE description
  would be updated with the new version information.

</li></ul>

  

<h1>Common Assumptions That Frequently Lead to Assignment Errors</h1>


<ul>

<li><b>One remote, one local.</b> I have two buffer overflows in the
same product.  One is exploitable <u>remotely</u>, and one is
exploitable <u>locally</u>.  Should I SPLIT them?
  <ul>

    <li>No (rather, these would stay merged based only on these two
    criteria).  ADT1 would not split - it's the same product.  ADT2
    would not split - it's the same bug type.  ADT3 woud not split -
    it's the same affected version.  However ADT4, explicitly says
    that the two issues should stay MERGED even if they have a
    different "access vector."

  </li></ul>

</li><li><b>Different bugs in different executables.</b>  I have two bugs
    of the same type in an open source product, such as SQL injection.
    There are two separate patches, in parameter X in executable A,
    and in parameter Y in executable B.  These are <u>clearly
    different bugs</u>.  Should I SPLIT them?

  <ul>

    <li>No.  They are in the same product, so ADT1 would not split.
    They are the same bug type, SQL injection, so ADT2 would not
    split.  They affect the same version, so ADT3 would not split.
    Also, ADT4 explicitly says that the issues should stay merged when
    "X appears in a different DLL, library, program, or application
    than Y."

  </li></ul>

</li><li><b>Different Impacts.</b>  I have two bugs, both directory
  traversal, affecting the same product versions.  One allows me to
  delete files, and the other allows me to read files.  Should I SPLIT
  them?

  <ul>

    <li>No.  By ADT1, there is no split since the bugs are in the same
    product.  There also is no split for the same bug type (ADT2) and
    affected versions (ADT3).  Finally, ADT4 explicitly recommends
    merge when "X has a more serious impact than Y."

  </li></ul>

</li></ul>

<a name="FAQ"></a>
<h1>Frequently Asked Questions (FAQ)</h1>



<p>

</p><h3>Changing CVEs Assignments After Discovering New Information</h3>


<ul>

<li> I assigned a CVE, but later analysis showed that the issue is not
a vulnerability.  The initial bug report was never publicly disclosed.
Can I re-assign the CVE to another issue?

  <ul><li>Probably not, especially if you have shared the CVE ID with
  any other external party.  Consult MITRE.
  </li></ul>

</li><li> I MERGED several issues into a single CVE, but after disclosure,
it became clear that these should have been SPLIT.  What should be
done about this?

  <ul><li>Work with MITRE on determining whether a SPLIT should be
  performed; if so, MITRE will do so.
  </li></ul>

</li><li> I've learned about a duplicate CVE.  What should I do?  Which CVE
should I use?

  <ul><li>Consult MITRE; only MITRE, as the Primary CNA, can decide
  which ID to use when a duplicate occurs.  (We generally follow the
  process as documented in
  https://cve.mitre.org/cve/editorial_policies/duplicates.html).
  </li></ul>

</li></ul>

<p>

</p><h3>Limited Disclosure Policy</h3>

<p>

</p><ul>

<li>I have a disclosure policy where I don't release
specific details about vulnerabilities, such as the type of
vulnerability.  How do I assign CVEs?

</li><li>I have a disclosure policy where I don't focus on issues
when I don't think they're important enough for my customers.  Do I
have to assign a CVE to those issues?



</li></ul>



<a name="checklist"></a>
<h1>Final Pre-Disclosure Checklist for CVE</h1>


Shortly before disclosure, follow this checklist for each CVE:

<p>

<table border="5" cellpadding="2" cellspacing="2">

<tbody><tr><td bgcolor="E0E0E0"><b>Share the CVE:</b>
</td><td>

Make sure that you've shared the CVE with all parties who are involved
in the disclosure.  This reduces the chance of duplicates.

</td></tr><tr><td bgcolor="E0E0E0"><b>Avoid typos:</b>
</td><td>

Make sure that none of your CVE numbers contain typos.  One way to do
this is to ensure that the CVE web site lists the "RESERVED" string in
each of their descriptions.

</td></tr><tr><td bgcolor="E0E0E0"><b>Multiple CVEs assigned:</b>
</td><td>

Ensure that your advisory clearly indicates which CVEs are associated
with which issues.

</td></tr><tr><td bgcolor="E0E0E0"><b>New issues discovered:</b>
</td><td>

If new issues were found during the disclosure process, see if you
need to SPLIT or MERGE them with the CVEs you already assigned.

</td></tr><tr><td bgcolor="E0E0E0"><b>Early disclosure:</b>
</td><td>

If the issue has already been publicly disclosed, even in a vague way,
check with MITRE.  Search the CVE or NVD web sites to be sure.

</td></tr></tbody></table>


</p><p>


<a name="examples"></a>

</p><h1>CVE COntent Decision Examples</h1>

See <a href="http://cvecmssrv1.mitre.org/cve-content/content-docs/cd-application-examples.html">this document</a> which
lists multiple examples for CD application.


<a name="changelog"></a>

<h1>Changelog</h1>

<table border="2" cellpadding="2" cellspacing="2">
<tbody><tr><th>Date</th><th>Comment

</th></tr><tr>
<td>September 17, 2008
</td><td>Initial creation

</td></tr><tr>
<td>September 10, 2012
</td><td>Added fall-through "Continue to [X]" options to make fall-through
more clear.

</td></tr><tr>
<td>April 19, 2013
</td><td>Added and clarified characteristics for ADT4, added additional
fall-through options.

</td></tr><tr>
<td>November 20, 2014
</td><td>Improved explanation of "Application Examples" page.
</td><td>Added "Complex Abstraction Scenarios" section.
</td><td>expanded "Common Assumptions" section.

</td></tr></tbody></table>
</body></html>