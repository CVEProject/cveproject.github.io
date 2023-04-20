---
title: CVEList GitHub Pilot Deprecation FAQs
layout: page
---

## What was the GitHub Submission Pilot and when is it scheduled to be deprecated?
The [CVEList GitHub Submission Pilot](https://github.com/CVEProject/cvelist) was a temporary method for [CVE Number Authorities (CNAs)](https://www.cve.org/PartnerInformation/Partner#CNA) to submit [CVE Records](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) (by GitHub pull requests) to be processed and posted to the official [CVE List](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCVEList).

The CVE Program’s [Tactical Working Group (TWG)](https://www.cve.org/ProgramOrganization/WorkingGroups#TacticalWorkingGroup) has determined that the <strong>deprecation date</strong> for the CVEList GitHub Submission Pilot will be <strong>June 30, 2023</strong>. This means that beginning at 12:01 a.m. GMT, July 1, 2023, any CVE Record submissions (i.e., Pull Requests) to the CVEList GitHub Submission Pilot will not be processed and posted to the CVE List.

## Why is the CVEList GitHub Submission Pilot being deprecated?
As its name suggests, the GitHub Submission Pilot was never meant to be a permanent solution for automated CVE Record Submission. (Although, notably, it has been operational for a long time.)

In October 2022, the CVE Program fielded its new solution for automated CVE Record Submission with the “[Soft Deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-soft-deploy)” of [CVE Services - Record Submission and Upload Service (RSUS) version 2.1.1](https://www.cve.org/AllResources/CveServices#architecture). During the Soft Deploy period (between November 2022 and later March 2023) the CNA community began using the new services and used the clients/libraries that have been developed to support adoption of the new [CVE JSON 5.0 format](https://github.com/CVEProject/cve-schema). 

On March 29, 2023, the [CVE Program announced](https://cveproject.github.io/automation-transition#bulletin-number-15) that it had met the CVE Services “[Hard Deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-hard-deploy)” milestone meaning that the critical “issues” identified during the “Soft Deploy” period had been addressed and CNAs could now use CVE Services and have confidence that submitted CVE Records in CVE JSON 5.0 format would be posted accurately and expeditiously to the CVE JSON 5.0 List. With this milestone CNAs, as well as downstream users, could view and download the JSON 5.0 CVE List. 

With these milestones being met, it is now time to move forward in deprecating the submission of JSON 4.0 Records (and hence the CVEList GitHub Submission Pilot) and take the next steps to full adoption of the new CVE Record JSON 5.0 format. 

## Will the new CVE Services provide my organization with all of the functions that I have available to me now?
Almost. CNAs can reserve CVE IDs and Submit/Update CVE Records that they own using the new CVE Services. CNAs will see CVE Record Submissions/Updates within an hour of submission on the JSON 5.0 CVE List which is viewable at cve.org as well as in a new [cvelistV5 repository](https://github.com/CVEProject/cvelistV5) on GitHub.com. (Note that this repository is designed in the same manner as the repository under the CVEList GitHub Submission Pilot).

CNAs will not be able to update CVE records that are “owned” by a different CNA. Although this capability exists today in the GitHub Submission Pilot, this function will not be implemented in CVE Services until the Automated Data Publishing interfaces are available. This capability is the next priority for the CVE Program Automation Upgrade project. A schedule for this effort is forthcoming.

## Will the CVEList GitHub Submission Pilot deprecation coincide with the deprecation of the legacy CVE List (i.e., based on the CVE Program JSON 4.0 format)?
No, the specific deprecation date for the JSON 4.0 based CVE List has not been determined yet (although it has been announced that it <strong>will take place no later than December 31, 2023</strong>). This means that, although the CVEList GitHub Submission Pilot is ending, the legacy CVE List will continue to be available for Downstream users until announced otherwise. 

## Where can I get more information about CVE Services and the new CVE Record JSON 5.0 format?
You can get more information about [CVE Services](https://www.cve.org/AllResources/CveServices) (i.e., how to get started), as well as information about the [CVE JSON 5.0 format](https://www.cve.org/AllResources/CveServices#cve-json-5) on the [CVE Services page](https://www.cve.org/AllResources/CveServices) on the CVE.ORG website. 

Much of the guidance provided focuses on CNAs entering CVE Record information manually (i.e., the web clients are very “human user” centric). Is there any specific guidance/support for engaging the CVE Services in a more automated fashion?

There are resources are available to help CNAs build a more automated infrastructure to submit CVE JSON 5.0 format CVE Records:

  <ul>
    <li><strong>CVE Services Interface Specification</strong> &mdash; CVE Services presents itself as a series of APIs addressable from the Internet. You can view the API specification <a href="https://cveawg.mitre.org/api-docs/">here</a>.</li>
    <li><strong>CVE Services Testing Instance</strong> &mdash; The CVE Program has developed a <a href="https://cveawg-test.mitre.org/api-docs/">CVE Services Testing Instance</a> to allow CNAs to “test” their automation infrastructure. To support this testing environment there is also a <a href=">https://test.cve.org/">testing website</a> for CNAs to view individual test CVE Records that they post using the Testing Instance.</li>
    <li><strong>Community Developed Clients</strong> &mdash; There are community development efforts that have produced automation tools that might be useful for CNA CVE Submission automation:</li>
      <ul>
        <li><strong><a href="https://github.com/RedHatProductSecurity/cvelib">Red Hat cvelib</a></strong> &mdash; A library and command line interface for the CVE Services API.</li>
        <li><strong><a href="https://github.com/marketplace/actions/cve-cna-bot">CVE CNA Bot</a></strong> &mdash; A GitHub action that validates CVE JSON 5.0 records and allows them to be submitted to the CVE Services API. This tool could be used to allow CNAs to continue to use GitHub as part of its CVE Submission process.</li>
      </ul>
  </ul>
