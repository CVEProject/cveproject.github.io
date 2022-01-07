---
title: CVE Automation Transition Details
layout: page
---
Two major CVE Automation deployments are planned for calendar 2022 that will significantly enhance the [CVE Program](https://www.cve.org/)’s ongoing transition towards a fully automated [CVE ID](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCVEID) assignment and [CVE Record](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) publishing/updating environment for the [CVE Numbering Authority (CNA)](https://www.cve.org/ProgramOrganization/CNAs) community. 

The purpose of this webpage is to inform and help prepare CNAs for the upcoming releases of:

* [CVE Services v2.1](https://github.com/CVEProject/cve-services)
* [CVE JSON v5.0](https://github.com/CVEProject/cve-schema/blob/master/schema/v5.0/CVE_JSON_5.0_schema.json)

Transition details and rough draft deployment timelines, along with links to additional resources, are included below. Refer to the CVE Automation announcements for the most recent transition news and updates.

## Transition Details
*January 6, 2021, CVE Services Transition Bulletin #1*

Although the majority of the transition activities will take place in 2022, the process began informally with the release of CVE Services 2.0 into the “CVE Services Testing Instance” in September 2021. The CVE Services Testing Instance allows CNAs to test their CVE Service Clients against the new CVE Services 2.0 and JSON 5.0 versions prior to their official releases.

The next steps in the transition process are:

<ol>
<li><strong>CVE Services 2.1 Community Testing in the Testing Instance</strong> — In late January/early February 2022, the [CVE Automation Working Group (AWG)](https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG) will release CVE Services 2.1 into the CVE Services Testing Instance. As with CVE Service 2.0 testing, CNAs will be able to continue to test their clients against this instance. CVE Services 2.1 is the target version of CVE Services that will be deployed into production that will be supporting JSON 5.0 for the community.</li>
<li><strong>CVE Services 2.1 Community Penetration Testing</strong> — Upon the release of CVE Service 2.1 into the Testing Instance, the CVE Services 2.1 Community Penetration Testing effort will commence and will run for approximately 3 weeks in late February/early March 2022. The [AWG](https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG) will be coordinating this community penetration testing effort so that interested members of the community may perform penetration testing on CVE Services 2.1. (This topic was discussed in the two “CVE Services 2.x Workshops” held September and October 2021). After the completion of the penetration testing effort, there will be a period of time for the development team to respond to issues identified in during the testing. Currently, four organizations have expressed interest to participate. If you or your organization are interested in this effort, please contact the AWG Chair.</li>
<li><strong>CNA Community Review of Historical JSON 5.0 Records</strong> — From January through March 2022, the [CVE Quality Working Group (QWG)]( https://www.cve.org/ProgramOrganization/WorkingGroups#QualityWorkingGroupQWG) will be coordinating two community reviews of historical CVE Records that have been converted to JSON 5.0. During the first review CNAs have an opportunity to review records that they “own” in the new format and offer early feedback on the Secretariat’s upconvert process. During the second review, CNAs will have an opportunity to update the CVE Records they own using the CVE Services RSUS interface. (This may be preferable for large CNAs who might be interested in upconverting their own records instead of relying on the Secretariat upconvert) If you or your organization are interested in getting more engaged in the planning of these reviews, please send email to the QWG Co-Chairs.</li>
<li><strong>CVE Services 2.1/JSON 5.0 Soft Deployment</strong> — Once the above activities are completed, there will be a soft deployment of CVE Services 2.1/JSON 5.0 that will span approximately 3 weeks into mid/late March 2022. During this timeframe CVE Services 2.1 will be deployed into the production environment and CNAs will have the full feature set of CVE Services to submit and update JSON 5.0 records. Also, during this time, the QWG will administer the second phase of the CNA Community Review of JSON 5.0 Historical Records (see above), in which CNAs will be encouraged to review the CVE Records they ow and make appropriate updates using CVE Services. It is important to note that during the soft deployment phase, only members of the CVE Community (i.e., CNAs) will have access to the JSON 5.0 CVE List. The general “downstream” user population of the CVE List will continue to observe (and download) JSON 4.0 Records from the CVE website.</li>
<li><strong>CVE Services 2.1/JSON 5.0 Hard Deployment</strong> — After the soft deployment phase toward the end of March/2022, the AWG will move into a hard deployment phase that will include deployments to make JSON 5.0-format CVE Records easily accessible to the world-wide community through the deployment of the JSON 5.0 GitHub download capability and the JSON website display and download capability on the main CVE website.</li>
</ol>

Please check this page regularly for updates. In addition, there will be follow-on communications to CNAs on [CVE CNA Discussion email list](mailto:cve-cna-list@mitre.org), on the main CVE website, and on CVE social media. You may also contact us with any comments or concerns.

## Additional Resources 

CVE Services resources are hosted on GitHub:
* [CVE Services Project](https://github.com/CVEProject/cve-services#project)
* [cvelib (free CVE Services API)](https://github.com/RedHatProductSecurity/cvelib)
* [CVE Services License](https://github.com/CVEProject/cve-services/blob/dev/LICENSE)
* [Contributing to CVE Services](https://github.com/CVEProject/cve-services/blob/dev/CONTRIBUTING.md)

CVE JSON resources are hosted on GitHub:
* [CVE Record Structure Mind Map](https://cveproject.github.io/cve-schema/schema/v5.0/docs/mindmap.html)
* [CVE Record Format JSON 5.0 Schema](https://github.com/CVEProject/cve-schema/blob/master/schema/v5.0/CVE_JSON_5.0_schema.json)
* [CVE Record in JSON 5.0 Format – Basic Example](https://github.com/cveproject/cve-schema/blob/master/schema/v5.0/docs/basic-example.json)
* [CVE Record in JSON 5.0 Format – Advanced Example](https://github.com/cveproject/cve-schema/blob/master/schema/v5.0/docs/advanced-example.json)
* [Schema Documentation](https://cveproject.github.io/cve-schema/schema/v5.0/docs/)

Other helpful resources are hosted on the main CVE website:
* [CVE List Downloads](https://www.cve.org/Downloads)
* [CVE List Search](https://www.cve.org/)
* [List of CNA Partners](https://www.cve.org/PartnerInformation/ListofPartners)
* [How to Partner with the CVE Program](https://www.cve.org/PartnerInformation/Partner#HowToBecomeAPartner)
* [CVE Program Blog & News Updates](https://www.cve.org/Media/News/AllNews)

