---
title: CVE Automation Transition Details
layout: page
---
Two major CVE Automation deployments are planned for calendar 2022 that will significantly enhance the [CVE Program](https://www.cve.org/)’s ongoing transition towards a fully automated [CVE ID](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCVEID) assignment and [CVE Record](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) publishing/updating environment for the [CVE Numbering Authority (CNA)](https://www.cve.org/ProgramOrganization/CNAs) community. 

The purpose of this webpage is to inform and help prepare CNAs for the upcoming releases of:

* [CVE Services v2.1](https://github.com/CVEProject/cve-services)
* [CVE JSON v5.0](https://github.com/CVEProject/cve-schema/blob/master/schema/v5.0/CVE_JSON_5.0_schema.json)

Transition details and rough draft deployment timelines, along with links to additional resources, are included below. Future transition news and updates will be posted below.

## Transition Details

## Bulletin Number 2
# *CVE Services Transition  —  January 26, 2022*

For CVE CNAs, the transition to CVE Services and JSON 5.0 began in December 2019 with the deployment of CVE Services 1.0 (the CVE ID Reservation (IDR) system) and the continued review and evolution the new CVE Record format (i.e., JSON 5.0). In June 2020 CVE Services 1.1 was deployed and in September 2021 CVE Services 2.0 was deployed into the new CVE Testing Instance. In November 2021, the community finalized the new JSON 5.0 format with the release of JSON 5.0 Release Candidate 5. Additional transition activities will take place in the spring of 2022 that will culminate in a major step forward for the automation effort for the program and the adoption of a richer, more robust CVE Record format (i.e., CVE JSON 5.0).

<strong>Spring 2022 CVE Services/JSON 5.0 Transition Activity Overview:</strong>

<ol>
<li><strong>CVE Services 2.1 Community Testing in the Testing Instance</strong> — In February 2022, the <a href="https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG" target="_blank">CVE Automation Working Group (AWG)</a> is planning on releasing CVE Services 2.1 into the CVE Services Testing Instance. As with CVE Service 2.0 testing, CNAs will be able to continue to test their clients against this instance. CVE Services 2.1 is the target version of CVE Services that will be deployed into production that will be supporting JSON 5.0 for the community.</li>
<li><strong>CVE Services 2.1 Community Penetration Testing</strong> — Upon the release of CVE Service 2.1 into the Testing Instance, the CVE Services 2.1 Community Penetration Testing effort will commence and will run for approximately 3 weeks in late February/early March 2022. The <a href="https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG" target="_blank">AWG</a> will be coordinating this community penetration testing effort so that interested members of the community may perform penetration testing on CVE Services 2.1. (This topic was discussed in the two “CVE Services 2.x Workshops” held September and October 2021). After the completion of the penetration testing effort, there will be a period of time for the development team to respond to issues identified in during the testing.</li>
<li><strong>CNA Community Review of Historical JSON 5.0 Records</strong> — From January through March 2022, the <a href="https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupQWG" target="_blank">CVE Quality Working Group (QWG)</a> will be coordinating two community reviews of historical CVE Records that have been converted to JSON 5.0. During the first review CNAs have an opportunity to review records that they “own” in the new format and offer early feedback on the Secretariat’s upconvert process. During the second review, CNAs will have an opportunity to update the CVE Records they own using the CVE Services Record Submission and Upload Subsystem (RSUS) interface. (This may be preferable for large CNAs who might be interested in upconverting their own records instead of relying on the Secretariat upconvert.) If you or your organization are interested in getting more engaged in the planning of these reviews, please send email to the QWG Co-Chairs.</li>
<li><strong>CVE Services 2.1/JSON 5.0 Soft Deployment</strong> — Once the above activities are completed, there will be a soft deployment of CVE Services 2.1/JSON 5.0 that will span approximately 3 weeks into mid/late April 2022. During this timeframe CVE Services 2.1 will be deployed into the production environment and CNAs will have the full feature set of CVE Services to submit and update JSON 5.0 records. Also, during this time, the QWG will administer the second phase of the CNA Community Review of JSON 5.0 Historical Records (see above), in which CNAs will be encouraged to review the CVE Records they own and make appropriate updates using CVE Services. It is important to note that during the soft deployment phase, only members of the CVE CNA community will have access to the JSON 5.0 CVE List. The general “downstream” user population of the CVE List will continue to observe and download JSON 4.0 Records from the main CVE website.</li>
<li><strong>CVE Services 2.1/JSON 5.0 Hard Deployment</strong> — After the soft deployment phase toward the end of April 2022, the AWG will move into a hard deployment phase that will include deployments to make JSON 5.0-format CVE Records easily accessible to the global community through the deployment of the JSON 5.0 GitHub download capability and the JSON website display and download capability on the main CVE website.</li>
<li><strong>JSON 4.0 Retirement</strong> — Six months after JSON 5.0 is made available to the CVE Community and CVE downstream users, JSON 4.0 will be retired. After JSON 4.0 retirement, historical JSON 4.0 records will continue to be available in an archived state. CNAs will be expected to submit CVE Records in JSON 5.0 format through either CVE Services web application API or a program designated web interface. At this time, JSON 5.0 format will be the only format that is available for download (other downloadable formats will be retired).</li>
</ol>

Please check this page regularly for updates. In addition, there will be follow-on communications to CNAs on [CVE CNA Discussion email list](mailto:cve-cna-list@mitre.org), on the main CVE website, and on CVE social media. You may also [contact us](https://cveform.mitre.org/) with any comments or concerns.

## Bulletin Number 1
# *CVE Services Transition  —  January 6, 2022*

“[Changes Coming to CVE Record Format JSON and CVE List Content Downloads](https://www.cve.org/Media/News/item/news/2022/01/11/Changes-Coming-to-CVE-Record)” — This initial announcement to CNAs about major changes coming to CVE JSON and Downloads in 2022 was sent to the CVE CNA Discussion email list on January 6, 2022.

For extended community awareness, the announcement was also posted on the main CVE website, on CVE social media, and included in the CVE Newsletter.

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
