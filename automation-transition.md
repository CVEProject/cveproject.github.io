---
title: CVE Automation Transition Details
layout: page
---
Two major CVE Automation deployments are planned for calendar 2022 that will significantly enhance the [CVE Program](https://www.cve.org/)’s ongoing transition towards a fully automated [CVE ID](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCVEID) assignment and [CVE Record](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) publishing/updating environment for the [CVE Numbering Authority (CNA)](https://www.cve.org/ProgramOrganization/CNAs) community. 

The purpose of this webpage is to inform and help prepare CNAs for the upcoming releases of:

* <strong>[CVE Services v2.1](https://github.com/CVEProject/cve-services)</strong> &mdash; CVE Services is a CVE Program Web Application that allows members of the CNA community to reserve [CVE IDs](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCVEID) and publish/update/reject [CVE Records](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) 24/7. It is meant to fully automate the CVE Record publication process that is used today that often involves significant manual intervention and maintenance. CVE Services 2.1 is a major upgrade that includes the adoption of CVE JSON 5.0 (see below). With the deployment of CVE Services 2.1, CNAs will be able to perform the most common CVE Program functions in a more efficient manner, obtaining results in the matter of minutes. 
* <strong>[CVE JSON v5.0](https://github.com/CVEProject/cve-schema/blob/master/schema/v5.0/CVE_JSON_5.0_schema.json)</strong> &mdash; JSON is the format used by CNAs for publishing CVE Records. CVE JSON 5.0, which is a major upgrade to JSON 4.0 that further normalizes and enriches how CVE information is presented, adds several new data fields to CVE Records. In addition to the required data of CVE ID number, affected product(s), affected version(s), and public references, JSON 5.0 CVE Records will now include optional data such as severity scores, credit for researchers, additional languages, affected product lists, additional references, ability for community contributions, etc. This optional data will enhance CVE Records for both downstream users and the overall vulnerability management community. 

Transition details and rough draft deployment timelines, along with links to additional resources, are included below. Future transition news and updates will be posted below.

## Transition Details

## Bulletin Number 3
<strong>*CVE Services Transition  —  March 16, 2022*</strong>

The activities and schedule for the transition to CVE Services 2.1 and CVE JSON 5.0, as provided last month in [Transition Bulletin #2](https://cveproject.github.io/automation-transition#bulletin-number-2), are now underway. This bulletin adds two new activities (7 & 8) and includes schedule updates where needed. Most importantly, it adds a new notification to CNAs that the [CVE List GitHub Submission Pilot](https://github.com/CVEProject/cvelist) will be retired as part of the transition (see below for details).

<strong>Transition Schedule and Activity Updates</strong>

Detailed descriptions for activities 1-6 below are provided in [Transition Bulletin #2](https://cveproject.github.io/automation-transition#bulletin-number-2). Detailed  descriptions of newly added activities 7 and 8 are included directly below. This new bulletin (#3) also provides the current transition schedule along with any schedule adjustments, to ensure CNAs have advance notice of all upcoming transition activities and actions needed by CNAs. 

“GitHub Pilot Retirement,” described below, is a new transition activity. It has also been added to the updated transition schedule as item 8.

* <strong>CVE List GitHub Submission Pilot Retirement</strong> &mdash; The CVE List GitHub Submission Pilot is JSON 4.0-based and will not be upgraded to JSON 5.0. As a JSON 4.0 based effort, it will not continue to operate after JSON 4.0 Retirement. It will continue to operate for 3 months after CVE Services 2.1/JSON 5.0 Hard Deployment. After JSON 4.0 Retirement, JSON 5.0 format will be the only format that is available for download (other downloadable formats will be retired), and CNAs will be expected to submit CVE Records in JSON 5.0 format through either CVE Services web application API, or a program designated web interface.

Another activity, “CVE List Download Changes,” was previously added as a transition activity. It has been added to the updated transition schedule below as item 8.

* <strong>CVE List Download Format Changes</strong> &mdash; After JSON 4.0 Retirement, JSON 5.0 format will be the only format available for CVE List downloads. All other download formats will be retired at the same time JSON 4.0 is retired (read [announcement](https://www.cve.org/Media/News/item/blog/2022/01/18/CVE-List-Download-Formats-Are)).

Updated Transition Schedule:
<br>

  <table style="padding-left:5%;padding-left:30%;">
    <tr>
      <th style="width:12%;padding-left:3%;">Item</th>
      <th style="width:42%">Activity</th>
      <th style="width:46%">Schedule</th>
    </tr>
    <tr>
      <td style="padding-left:3%;">1</td>
      <td>CVE Services 2.1 Community Testing in the Testing Instance</td>
      <td>Late February/early March 2022</td>
    </tr>
    <tr>
      <td style="padding-left:3%;">2</td>
      <td>CVE Services 2.1 Community Penetration Testing</td>
      <td>Mid-to-late March 2022 (will run for approximately 3 weeks)</td>
    </tr>
      <tr>
      <td style="padding-left:3%;">3</td>
      <td>CNA Community Review of Historical JSON 5.0 Records</td>
      <td>January through April 2022</td>
    </tr>
      <tr>
      <td style="padding-left:3%;">4</td>
      <td>CVE Services 2.1/JSON 5.0 Soft Deployment</td>
      <td>Mid-to-late April 2022 (will span approximately 3 weeks)</td>
    </tr>
      <tr>
      <td style="padding-left:3%;">5</td>
      <td>CVE Services 2.1/JSON 5.0 Hard Deployment</td>
      <td>Late April 2022</td>
    </tr>
      <tr>
      <td style="padding-left:3%;">6</td>
      <td>JSON 4.0 Retirement</td>
      <td>July 2022 (3 months after JSON 5.0 is made available to CVE downstream users)</td>
    </tr>
      <tr>
      <td style="padding-left:3%;">7</td>
      <td>CVE List GitHub Submission Pilot Retirement</td>
      <td>July 2022 (3 months after JSON 5.0 is made available to CVE downstream users)</td>
    </tr>
      <tr>
      <td style="padding-left:3%;">8</td>
      <td>CVE List Download Format Changes</td>
      <td>July 2022 (3 months after JSON 5.0 is made available to CVE downstream users)</td>
    </tr>
  </table>

<br>
Please check this page regularly for updates. In addition, there will be follow-on communications to CNAs on [CVE CNA Discussion email list](mailto:cve-cna-list@mitre.org), on the main CVE website, and on CVE social media. You may also [contact us](https://cveform.mitre.org/) with any comments or concerns.

## Bulletin Number 2
<strong>*CVE Services Transition  —  February 11, 2022*</strong>

For CVE CNAs, the transition to CVE Services and JSON 5.0 began in December 2019 with the deployment of CVE Services 1.0 (the CVE ID Reservation (IDR) system) and the continued review and evolution the new CVE Record format (i.e., JSON 5.0). In June 2020 CVE Services 1.1 was deployed and in September 2021 CVE Services 2.0 was deployed into the new CVE Testing Instance. In November 2021, the community finalized the new JSON 5.0 format with the release of JSON 5.0 Release Candidate 5. Additional transition activities will take place in the spring of 2022 that will culminate in a major step forward for the automation effort for the program and the adoption of a richer, more robust CVE Record format (i.e., CVE JSON 5.0).

<strong>Spring 2022 CVE Services/JSON 5.0 Transition Activity Overview:</strong>

<ol>
<li><strong>CVE Services 2.1 Community Testing in the Testing Instance</strong> — In late February/early March 2022, the <a href="https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG" target="_blank">CVE Automation Working Group (AWG)</a> is planning on releasing CVE Services 2.1 into the CVE Services Testing Instance. As with CVE Service 2.0 testing, CNAs will be able to continue to test their clients against this instance. CVE Services 2.1 is the target version of CVE Services that will be deployed into production that will be supporting JSON 5.0 for the community.</li>
<li><strong>CVE Services 2.1 Community Penetration Testing</strong> — Upon the release of CVE Service 2.1 into the Testing Instance, the CVE Services 2.1 Community Penetration Testing effort will commence and will run for approximately 3 weeks into mid/late March 2022. The <a href="https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG" target="_blank">AWG</a> will be coordinating this community penetration testing effort so that interested members of the community may perform penetration testing on CVE Services 2.1. (This topic was discussed in the two “CVE Services 2.x Workshops” held September and October 2021). After the completion of the penetration testing effort, there will be a period of time for the development team to respond to issues identified in during the testing.</li>
<li><strong>CNA Community Review of Historical JSON 5.0 Records</strong> — From January through April 2022, the <a href="https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupQWG" target="_blank">CVE Quality Working Group (QWG)</a> will be coordinating two community reviews of historical CVE Records that have been converted to JSON 5.0. During the first review CNAs have an opportunity to review records that they “own” in the new format and offer early feedback on the Secretariat’s upconvert process. During the second review, CNAs will have an opportunity to update the CVE Records they own using the CVE Services Record Submission and Upload Subsystem (RSUS) interface. (This may be preferable for large CNAs who might be interested in upconverting their own records instead of relying on the Secretariat upconvert.) If you or your organization are interested in getting more engaged in the planning of these reviews, please send email to the QWG Co-Chairs.</li>
<li><strong>CVE Services 2.1/JSON 5.0 Soft Deployment</strong> — Once the above activities are completed, there will be a soft deployment of CVE Services 2.1/JSON 5.0 that will span approximately 3 weeks into mid/late April 2022. During this timeframe CVE Services 2.1 will be deployed into the production environment and CNAs will have the full feature set of CVE Services to submit and update JSON 5.0 records. Also, during this time, the QWG will administer the second phase of the CNA Community Review of JSON 5.0 Historical Records (see above), in which CNAs will be encouraged to review the CVE Records they own and make appropriate updates using CVE Services. It is important to note that during the soft deployment phase, only members of the CVE CNA community will have access to the JSON 5.0 CVE List. The general “downstream” user population of the CVE List will continue to observe and download JSON 4.0 Records from the main CVE website.</li>
<li><strong>CVE Services 2.1/JSON 5.0 Hard Deployment</strong> — After the soft deployment phase toward the end of April 2022, the AWG will move into a hard deployment phase that will include deployments to make JSON 5.0-format CVE Records easily accessible to the global community through the deployment of the JSON 5.0 GitHub download capability and the JSON website display and download capability on the main CVE website.</li>
<li><strong>JSON 4.0 Retirement</strong> — Six months after JSON 5.0 is made available to CVE downstream users, JSON 4.0 will be retired. After JSON 4.0 retirement, historical JSON 4.0 records will continue to be available in an archived state. CNAs will be expected to submit CVE Records in JSON 5.0 format through either CVE Services web application API or a program designated web interface. At this time, JSON 5.0 format will be the only format that is available for download (other downloadable formats will be retired).</li>
</ol>

Please check this page regularly for updates. In addition, there will be follow-on communications to CNAs on [CVE CNA Discussion email list](mailto:cve-cna-list@mitre.org), on the main CVE website, and on CVE social media. You may also [contact us](https://cveform.mitre.org/) with any comments or concerns.

## Bulletin Number 1
<strong>*CVE Services Transition  —  January 6, 2022*</strong>

“[Changes Coming to CVE Record Format JSON and CVE List Content Downloads](https://www.cve.org/Media/News/item/news/2022/01/11/Changes-Coming-to-CVE-Record)” — This initial announcement to CNAs about major changes coming to CVE JSON and Downloads in 2022 was sent to the CVE CNA Discussion email list on January 6, 2022.

For extended community awareness, the announcement was also posted on the main CVE website, on CVE social media, and included in the CVE Newsletter.

## Additional Resources 

CVE Services resources are hosted on GitHub:
* [CVE Services Project](https://github.com/CVEProject/cve-services#project)
* [cvelib (free CVE Services API)](https://github.com/RedHatProductSecurity/cvelib)
* [CVE Services License](https://github.com/CVEProject/cve-services/blob/dev/LICENSE)
* [Contributing to CVE Services](https://github.com/CVEProject/cve-services/blob/dev/CONTRIBUTING.md)
* [CVE Services CNA Account Registration form]((https://forms.monday.com/forms/03132d0646401f5d10d06c60e25444a1?r=use1))

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
