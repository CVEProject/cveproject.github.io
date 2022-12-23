---
title: CVE Automation Transition Details
layout: page
---
Two major CVE Automation deployments in October 2022/early 2023 will significantly enhance the [CVE Program](https://www.cve.org/)’s ongoing transition towards a fully automated [CVE ID](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCVEID) assignment and [CVE Record](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) publishing/updating environment for the [CVE Numbering Authority (CNA)](https://www.cve.org/ProgramOrganization/CNAs) community. 

The purpose of this webpage is to inform CNAs about the October 2022 (see [Bulletin 11](https://cveproject.github.io/automation-transition#bulletin-number-11) below) [soft deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-soft-deploy) and help prepare CNAs for the 2023 [hard deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-hard-deploy) releases of:

* <strong>[CVE Services v2.1](https://github.com/CVEProject/cve-services)</strong> &mdash; CVE Services is a CVE Program Web Application that allows members of the CNA community to reserve [CVE IDs](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCVEID) and publish/update/reject [CVE Records](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) 24/7. It is meant to fully automate the CVE Record publication process that is used today that often involves significant manual intervention and maintenance. CVE Services 2.1 is a major upgrade that includes the adoption of CVE JSON 5.0 (see below). With the deployment of CVE Services 2.1, CNAs will be able to perform the most common CVE Program functions in a more efficient manner, obtaining results in the matter of minutes. 
* <strong>[CVE JSON v5.0](https://github.com/CVEProject/cve-schema/blob/master/schema/v5.0/CVE_JSON_5.0_schema.json)</strong> &mdash; JSON is the format used by CNAs for publishing CVE Records. CVE JSON 5.0, which is a major upgrade to JSON 4.0 that further normalizes and enriches how CVE information is presented, adds several new data fields to CVE Records. In addition to the required data of CVE ID number, affected product(s), affected version(s), and public references, JSON 5.0 CVE Records will now include optional data such as severity scores, credit for researchers, additional languages, affected product lists, additional references, ability for community contributions, etc. This optional data will enhance CVE Records for both downstream users and the overall vulnerability management community. 

A [Current Status dashboard](), [Transition Details Bulletins](https://cveproject.github.io/automation-transition#transition-details), and links to [additional helpful resources](https://cveproject.github.io/automation-transition#additional-resources) are included below. Future transition schedule and bulletin updates will be posted below.

## Current Status

The purpose of this dashboard section is to provide CNAs with the current status of the CVE Program’s transition to the new CVE Services and CVE JSON 5.0.

Last updated: 19 December 2022

<strong>Current Transition Phase</strong>
* [Soft Deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-soft-deploy)

<strong>Status of Current Phase Activities</strong>
*Note: The items below must be completed before we move into the next phase.*

* CVE Services/CVE JSON 5.0 Transition Immediate Priority Issues: [view list](https://cveproject.github.io/automation-cve-services-known-issues)
* CVE Services developer issues on GitHub (high and low priorities only): [view list](https://github.com/CVEProject/cve-services/projects/29)
* CVE JSON 5.0-format bulk download capability: in development

<strong>Timeframe for Next Phases</strong>
* [Hard Deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-hard-deploy): Q1 calendar year 2023
* CVE JSON 4.0 Retirement: TBD

<br/>

## Transition Details

## Bulletin Number 13
<strong>*Moving Forward on CVE Service/CVE JSON 5.0 Adoption — December 22, 2022*</strong>

As the CVE Program continues to move through the [soft deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-soft-deploy) period for CVE Services/CVE JSON 5.0, we have continued to make upgrades to help you advance your adoption of both. As a reminder, soft deployment means CNAs are actively using the services and any issues found by the community are being prioritized and addressed by the [CVE Automation Working Group (AWG)](http://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG) once reported. The [hard deployment](https://cveproject.github.io/automation-cve-services-faqs#what-is-meant-by-cve-services-21-hard-deploy) phase will begin once the soft deployment phase is completed.

The following improvements are now available for CNAs:

<h3>Enhanced test environment for incorporating CVE Services into your infrastructure and/or developing a CVE Services client now available</h3>

The test environment consists of the following:

* CVE Services test instance – [https://cveawg-test.mitre.org/api](https://cveawg-test.mitre.org/api) 
* CVE website test instance (new) – [https://test.cve.org](https://test.cve.org)

CNAs can use the test environment to ensure that they have correctly integrated CVE Services into their established vulnerability management infrastructures. Specifically, the [CVE Services test instance](https://cveawg-test.mitre.org/api) allows you to test your integration of the [CVE ID Reservation (IDR) service](https://cveproject.github.io/automation-cve-services#services-overview) and [CVE Record Submission and Upload Service (RSUS)](https://cveproject.github.io/automation-cve-services#services-overview), while the new [CVE website test instance](https://test.cve.org/) allows you to verify that test CVE Records will be published correctly in [CVE JSON 5.0](https://cveproject.github.io/automation-cve-services#json-overview) format (simply use the CVE ID Lookup on the website test instance’s homepage to look up and view a test record). CVE Services test instance docs are available [here](https://cveawg-test.mitre.org/api-docs/).

A CNA developing its own CVE Services client can also use the test environment to test that its client is working properly, in the same manner.

By leveraging the test environment, CNAs can be confident that their incorporation of CVE Services into their infrastructure and processes, or development of their own CVE Services client, will work correctly once deployed in the CVE Services production environment.   

Test Instance Credentials Required — If you are a CNA and wish to use the CVE Services test instance, you will need credentials that are separate from your production environment CVE Services credentials. Credentials are not required to view the CVE website test instance. Learn how to request test instance credentials [here](https://cveproject.github.io/automation-cve-services-getting-started#obtaining-credentials-for-the-cve-services-test-instance).

<h3>CVE Program Website and CVE Services upgraded to address Prioritized Issues</h3>

Two updates were released in December 2022, one for the CVE website and the other for CVE Services.  One issue on the [CVE Services - Prioritized Issue List](https://cveproject.github.io/automation-cve-services-known-issues) was resolved, and we continue to work diligently on all the issue on the list. View the resolved issue [here](https://cveproject.github.io/automation-cve-services-known-issues#resolved-issues).

<strong>December 7</strong> – A bug on the CVE website that incorrectly rendered the “affected version” recorded in CVE JSON 5.0 CVE Records was fixed. With this correction, you can now view CVE JSON 5.0 records on the new cve.org website with confidence that the correct affected version is being rendered. 

<strong>December 19</strong> – CVE Services version 2.1.1 was released to fix, among [other issues](https://github.com/CVEProject/cve-services/releases/tag/v2.1.1-sd), a bug that was identified by the CNA community where valid CVE Records submitted for publication were incorrectly being flagged with JSON schema validation errors.  Thanks to those early adopters of CVE Services that continue to identify areas we need to address as we move CVE Services closer to our Hard Deploy milestone scheduled for Q1 calendar year 2023.  

<h3>“Current Status” dashboard for CVE Services/CVE JSON 5.0 transition added to CVE Program Automation Transition Website</h3>

We realize that the CVE Services/CVE JSON 5.0 transition is a long and often complicated process and that there is a lot of information that must be conveyed, digested, and acted upon. To help CNAs stay aware of the most current information and transition status, a new [“Current Status” dashboard](https://cveproject.github.io/automation-transition#current-status) has been added to the [CVE Automation Transition Details page](https://cveproject.github.io/automation-transition#current-status) on the automation transition website to keep you up to date. 

View the current status [here](https://cveproject.github.io/automation-transition#current-status).

<br/>

Questions? Please use the [CVE Request Web Forms](https://cveform.mitre.org/) and select “Other” from the dropdown.

<br/>

## Bulletin Number 12
<strong>*CVE Services Workshop Videos Now Available — November 15, 2022*</strong>

“[CVE JSON 5.0, CVE Services Clients & More Videos from the “CVE Services Workshop” Now Available](https://www.cve.org/Media/News/item/news/2022/11/15/CVE-JSON-50-CVE-Services)” — This announcement about the workshop videos for CNAs was sent to the CVE CNA Discussion email list on November 14, 2022 and posted on the main CVE website on November 15, 2022.

Introductions to CVE JSON 5.0, the CVE ID Reservation Service (IDR), the Record Submission and Upload (RSUS) Service, CVE Clients for interacting with the CVE Services, and information about how to obtain organizational and individual account credentials for the CVE Services, are all included in the videos.

For extended community awareness, the announcement was also posted on the main CVE website and on CVE social media. 

## Bulletin Number 11

<strong>*Soft Deployment of Record Submission and Upload Service/CVE JSON 5.0 Complete:  What’s Next for CVE Services/CVE JSON 5.0 Adoption — October 27, 2022*</strong>

Phase 1 of the soft deployment of [CVE Services 2.1](https://cveproject.github.io/automation-cve-services#services-overview)/[CVE JSON 5.0](https://cveproject.github.io/automation-cve-services#json-overview) to deprecate CVE Services ID Reservation (IDR) 1.1 and release [CVE Services - IDR 2.1](https://github.com/CVEProject/cve-services), was completed on October 6, 2022.

Phase 2, soft deployment of [CVE Services 2.1 – Record Submission and Upload Service (RSUS)](https://github.com/CVEProject/cve-services), was completed on October 25, 2022.

See [Bulletin #10](https://cveproject.github.io/automation-transition#bulletin-number-10) and [Bulletin #9](https://cveproject.github.io/automation-transition#bulletin-number-9) for the schedule and complete descriptions of the soft deploy phases.

<h3>Overview</h3>

With the completion of CVE Services 2.1 Soft Deployment, we enter a “transition period” for CNAs to begin adopting the CVE JSON 5.0 format. During the transition period the CVE Program will support the current CVE Record Submission workflows (i.e., the [CVEList GitHub Pilot](https://github.com/CVEProject/cvelist) in CVE JSON 4.0 format and the [CVE Program Request web forms](https://cveform.mitre.org/) submission process) while introducing a new submission process using CVE JSON 5.0 (using CVE Services). CNAs should begin transitioning their CVE Record management infrastructure to use CVE JSON 5.0 format using CVE Services. 

To begin the transition, CNAs should:

1. Check out the [CVE Services Prioritized Issues](https://cveproject.github.io/automation-cve-services-known-issues) page. This page will highlight some important issues that we know about and are working to correct. 2. If you uncover what you might think be an important issue for us to address, you can post it on the CVE Services Slack Channel (which is monitored from 9:00 a.m. – 5:00 p.m. ET weekdays) or by contacting the CVE Automation Working Group (AWG) at [awg@cve-CWE-Programs.groups.io](awg@cve-CWE-Programs.groups.io).
3. If you have not already done so, review your historical CVE Records that have been upconverted for you into CVE JSON 5.0 format [here](https://github.com/CVEProject/cvelistV5). (Note that this list is not the official CVE List but only a review list for you to consider as part of this transition period. The official CVE List will continue to be [here](https://cve.mitre.org/cve/search_cve_list.html) and downloadable [here](https://www.cve.org/Downloads) in the traditional formats, based on CVE JSON 4.0 records).
4. Make updates to your CVE Records using the new CVE Services if you find anomalies (see [Getting Started with CVE Services](https://cveproject.github.io/automation-cve-services-getting-started)).
5. Begin planning your transition to the new CVE JSON 5.0 format and adoption of CVE Services.
6. Attending the virtual [CVE Services Workshop](https://www.cve.org/Media/News/item/news/2022/08/30/CVE-Services-Workshop-for-CNAs) scheduled for November 2, 2022, from 10:00 a.m. – 2:00 p.m. EDT.
7. Report issues to the CVE Services Slack channel (or the web form), which will be monitored from 9:00 a.m. to 5:00 p.m. EDT for technical support. 
8. Check out the new [CVE Services Transition Frequently Asked Questions](https://cveproject.github.io/automation-cve-services-faqs) page. If you have a question that is not answered here, you can submit that question for inclusion using the [CVE Program Request web forms](https://cveform.mitre.org/) (use the “other” form).

Look for announcements of the next important CVE Services milestone (i.e., CVE Services “hard deploy” targeted for early 2023 which will introduce a “bulk download” capability for CVE JSON 5.0 records that will upgrade our current CVE List Download Architecture. (Note: there will be no CVE JSON 5.0 Bulk Download capability until this deployment).

<h3>Reviewing What’s Available for ID Reservation, Record Submission, Record Viewing, and Downloads</h3>

The table below provides a review of the options available to CNAs for reserving CVE IDs and submitting, viewing, and downloading CVE Records, via CVE Services automation or alternate methods, now that soft deployment was completed at the end of October 2022. User Registry is how CNAs manage their own CVE Services users.

Post-October next steps, including advance notice for the eventual deprecation of the CVEList GitHub Pilot, will be announced in future bulletins.

<h4>CVE ID Reservation/CVE Record Uploading/User Registry Operations/Search-Viewing Records/CVE Downloads</h4>

<table style="padding-left:5%;padding-right:30%;">
    <tr>
      <th style="width:25%;padding-left:3%;">Action</th>
      <th style="width:25%;padding-left:2%;">Prior to October 6</th>
      <th style="width:25%;padding-left:2%;">Phase 1<br/>Beginning October 6</th>
      <th style="width:25%;padding-left:2%;">Phase 2<br/>Beginning October 25</th>
    </tr>
    <tr>
      <td style="padding-left:3%;"><strong>Reserve CVE IDs</strong></td>
      <td style="padding-left:3%;padding-top:3%;">IDR 1.1<br/>CVE Request Web Form</td>
      <td style="padding-left:3%;padding-top:3%;">IDR 1.1 - DEPRECATED<br/>IDR 2.1 - AVAILABLE<br/>CVE Request Web Form</td>
      <td style="padding-left:3%;padding-top:3%;"><strong>IDR 2.1 - AVAILABLE</strong><br/>CVE Request Web Form</td>
    </tr>
    <tr>
      <td style="padding-left:3%;"><strong>Submit CVE Records</strong></td>
      <td style="padding-left:3%;padding-top:3%;">GitHub CVEList Pilot (JSON 4.0 only)<br/>CVE Request Web Form (JSON 4.0 only)</td>
      <td style="padding-left:3%;padding-top:3%;">GitHub CVEList Pilot (JSON 4.0 only)<br/>CVE Request Web Form (JSON 4.0 only)</td>
      <td style="padding-left:3%;padding-top:3%;"><strong>RSUS 2.1 with JSON 5.0 – AVAILABLE</strong><br/>GitHub CVEList Pilot (JSON 4.0 only)<br/>CVE Request Web Form (JSON 4.0 only)</td>
    </tr>
    <tr>
      <td style="padding-left:3%;"><strong>User Registry</strong><br/>(CNA manages its CVE Services users)</td>
      <td style="padding-left:3%;padding-top:3%;">IDR 1.1</td>
      <td style="padding-left:3%;padding-top:3%;">IDR 1.1 - DEPRECATED<br/>IDR 2.1 - REQUIRED</td>
      <td style="padding-left:3%;padding-top:3%;"><strong>IDR 2.1 – REQUIRED</strong></td>
    </tr>
     <tr>
      <td style="padding-left:3%;"><strong>Searching-Viewing CVE Records</strong></td>
      <td style="padding-left:3%;padding-top:3%;">
           <strong>ID LOOK UP:</strong><br/>
           cve.org website (JSON 4.0)<br/>
           <br/>
           <strong>ID & KEYWORD SEARCH:</strong><br/>
           cve.mitre.org legacy site (JSON 4.0)<br/>
           <br/>
           <strong>ID RECORD SEARCH:</strong><br/>
           GitHub CVEList Pilot (JSON 4.0)
      </td>
      <td style="padding-left:3%;padding-top:3%;"><strong>ID LOOK UP:</strong><br/>
           cve.org website (<strong>JSON 5.0</strong>)<br/>
           <br/>
           <strong>ID & KEYWORD SEARCH:</strong><br/>
           cve.mitre.org legacy site (JSON 4.0)<br/>
           <br/>
           <strong>ID RECORD SEARCH:</strong><br/>
           GitHub CVEList Pilot (JSON 4.0)
      </td>
      <td style="padding-left:3%;padding-top:3%;">
           <strong>ID LOOK UP:</strong><br/>
           cve.org website (<strong>JSON 5.0</strong>)<br/>
           <br/>
           <strong>ID & KEYWORD SEARCH:</strong><br/>
           cve.mitre.org legacy site (JSON 4.0)<br/>
           <br/>
           <strong>ID RECORD SEARCH:</strong><br/>
           GitHub CVEList Pilot (JSON 4.0)       
      </td>
     </tr>
     <tr>
      <td style="padding-left:3%;"><strong>CVE Downloads</strong><br/>NOTE: cve.org links-out to the cve.mitre.org <a href="https://cve.mitre.org/data/downloads/index.html">downloads</a></td>
      <td style="padding-left:3%;padding-top:3%;">
           cve.org website (JSON 4.0)<br/><br/>
           cve.mitre.org legacy site (JSON 4.0)<br/><br/>
           GitHub CVEList Pilot (JSON 4.0)
      </td>
      <td style="padding-left:3%;padding-top:3%;">
           cve.org website (JSON 4.0)<br/><br/>
           cve.mitre.org legacy site (JSON 4.0)<br/><br/>
           GitHub CVEList Pilot (JSON 4.0)
      </td>
      <td style="padding-left:3%;padding-top:3%;">
           cve.org website (JSON 4.0)<br/><br/>
           cve.mitre.org legacy site (JSON 4.0)<br/><br/>
           GitHub CVEList Pilot (JSON 4.0)
      </td>
     </tr>    
  </table>

<br/>

Questions? Please use the [CVE Request Web Forms](https://cveform.mitre.org/) and select “Other” from the dropdown.


## Bulletin Number 10

<strong>*Schedule for October Deployment of CVE Services 2.1/CVE JSON 5.0 — October 3, 2022*</strong>

[CVE Services 2.1](https://cveproject.github.io/automation-cve-services#services-overview)/[CVE JSON 5.0](https://cveproject.github.io/automation-cve-services#json-overview) Soft Deploy will occur during the entire month of October with Phase 1 beginning on October 3 and Phase 2 occurring during the last week of October. See [Bulletin #9](https://cveproject.github.io/automation-transition#bulletin-number-9) for a full description of all the Soft Deploy phases and how to prepare.

<h3>Overview</h3>

Phase 1 of soft deployment&mdash;to release CVE Services-IDR 2.1&mdash;began today on <strong>October 3, 2022, at 1:00 p.m. EDT.  Entering Phase 1 will take approximately 48 hours, completing on October 5</strong>. During this time, the CVE Program will convert the current CVE JSON 4.0 repository to CVE JSON 5.0, upgrade the software, and perform validation.  
<br/> 
><strong>During this 48-hour period, the system will be taken “offline” and CVE ID assignment and posting CVE Records to the CVE List will be suspended.  
<br/>
CVE Records submitted during this time will be “queued” and advanced to the CVE List when the system is brought back “online.”</strong>
 
We will make an announcement via this email list and on the CVE Services Slack Channel prior to taking the system down and again when we bring the system back up. Phase I marks the beginning of a significant transition for the CVE Program. You may see anomalies in processing data during the course of this transition. You can report anomalies/issues to CVE Services Slack Channel, which will be monitored from 9:00 a.m. to 5:00 p.m. EDT weekdays for technical support. In addition, you can report any anomalies using the [CVE Program Web Forms](https://cveform.mitre.org/) (select "Other" from the droopdown menu) as well. 

Phase 2 of soft deployment&mdash;to release CVE Services-RSUS 2.1&mdash;will take place during last week of October. An RSUS-specific deployment bulletin will be sent as we approach that date.

<h3>CVE Services 2.1 October Transition Description</h3>

The table below provides an overview for CNAs of what to expect in October. Post October “next steps” will be announced in future bulletins. 
<br/><br/>
<h4>CVE ID Reservation/ CVE Record Uploading / User Registry Operations</h4>
<br/>
<table style="padding-left:5%;padding-right:30%;">
    <tr>
      <th style="width:25%;padding-left:3%;">Action</th>
      <th style="width:25%;padding-left:2%;">Now</th>
      <th style="width:25%;padding-left:2%;">Phase 1 Beginning October 5th</th>
      <th style="width:25%;padding-left:2%;">Phase 2 Beginning Last Week of October</th>
    </tr>
    <tr>
      <td style="padding-left:3%;"><strong>Reserve CVE IDs</strong></td>
      <td style="padding-left:3%;padding-top:3%;">IDR 1.1<br/>CVE Request Web Form</td>
      <td style="padding-left:3%;padding-top:3%;"><strong>IDR 1.1 - DEPRECATED<br/>IDR 2.1 - AVAILABLE</strong><br/>CVE Request Web Form</td>
      <td style="padding-left:3%;padding-top:3%;"><strong>IDR 2.1 - AVAILABLE</strong><br/>CVE Request Web Form</td>
    </tr>
    <tr>
      <td style="padding-left:3%;"><strong>Submit CVE Records</strong></td>
      <td style="padding-left:3%;padding-top:3%;">GitHub CVEList Pilot<br/>CVE Request Web Form</td>
      <td style="padding-left:3%;padding-top:3%;">GitHub CVEList Pilot<br/>CVE Request Web Form</td>
      <td style="padding-left:3%;padding-top:3%;"><strong>RSUS 2.1 with JSON 5.0 – AVAILABLE</strong><br/>GitHub CVEList Pilot<br/>CVE Request Web</td>
    </tr>
    <tr>
      <td style="padding-left:3%;"><strong>User Registry</strong><br/>(CNA manages its CVE Services users)</td>
      <td style="padding-left:3%;padding-top:3%;">IDR 1.1</td>
      <td style="padding-left:3%;padding-top:3%;"><strong>IDR 1.1 - DEPRECATED<br/>IDR 2.1 - REQUIRED</strong></td>
      <td style="padding-left:3%;padding-top:3%;"><strong>IDR 2.1 – REQUIRED</strong></td>
    </tr>
  </table>
<br/>
<h3>Save the date! — “CVE Services Workshop” Scheduled for November 2, 2022</h3>

CNAs should also make preparations to participate in the virtual “[CVE Services Workshop](https://www.cve.org/Media/News/item/news/2022/08/30/CVE-Services-Workshop-for-CNAs)” for CNAs to learn how to use CVE Services 2.1/CVE JSON 5.0 scheduled for November 2, 2022, from 10am to 2pm ET. We are considering holding a second live workshop for CNAs in Asia at a better time for them.  If you are a CNA in Asia, please let us know if there is interest.   

A registration link will be sent soon via the CNA Discussion List, so please watch for that email. There is no limit on the number of attendees that can participate from your organization.
<br/><br/>

Questions? Please use the [CVE Request Web Forms](https://cveform.mitre.org/) and select “Other” from the dropdown.

## Bulletin Number 9
<strong>*Deployment Update for CVE Services 2.1 - Record Submission and Upload Service (RSUS) and CVE JSON 5.0 — September 12, 2022*</strong>

The CVE Program is in the final stages of planning its next steps in its automation update strategy. In Transition Bulletins [#2](https://cveproject.github.io/automation-transition#bulletin-number-2) and [#3](https://cveproject.github.io/automation-transition#bulletin-number-3) we laid out a broad transition strategy that would culminate in a new automated approach for CNAs to submit CVE Records.

<h3>Soft Deployment Schedule</h3>

“Soft Deployment” of [CVE Services 2.1](https://cveproject.github.io/automation-cve-services#services-overview)/[CVE JSON 5.0](https://cveproject.github.io/automation-cve-services#json-overview) will begin the first week of October 2022, and will be implemented in two phases over the course of the month:

* <strong>Phase I –</strong> This phase will begin the first week of October (10/3/22 – 10/9/22) with an update of the [CVE Services 2.1 - CVE IDR Reservation (IDR) Service](https://github.com/CVEProject/cve-services). At the completion of the Phase I on October 10, CNAs using CVE Services for CVE ID Reservation will be using CVE Services 2.1. 

* <strong>Phase II –</strong> The CVE IDR System update that was completed in Phase I will lay the groundwork for Phase II (i.e., the soft deployment of [CVE Services 2.1 – Record Submission and Upload Service (RSUS)](https://github.com/CVEProject/cve-services), which will take place the last full week of October (10/24/22 – 10/28/22). At the completion of Phase II on October 31, CNAs will have the ability to submit CVE JSON 5.0 records using the new CVE Services 2.1 RSUS interfaces to the live CVE List.

<h3>How CNAs Should Prepare</h3>

<h4>Preparing for Phase I (Week 1 October)</h4>

Current users of the CVE Services 1.1.1 - IDR Service will need to migrate to a client that has been upgraded to be compatible with CVE Services 2.1 - IDR Service.   
There are currently three clients that have been developed for community adoption that are expected to be ready for the first week of October that you can adopt:

  <table style="padding-left:5%;padding-left:30%;">
    <tr>
      <th style="width:30%;padding-left:3%;">Client Name</th>
      <th style="width:70%;padding-left:2%;">Notes</th>
    </tr>
    <tr>
      <td style="padding-left:3%;"><a href="https://vulnogram.github.io/#editor">Vulnogram</a></td>
      <td>
          <ul>
               <li>A client with a robust GUI</li>
               <li>Can be installed locally or it can be used from the internet through a web browser</li>
          </ul>
     </td>
    </tr>
    <tr>
      <td style="padding-left:3%;"><a href="https://certcc.github.io/cveClient/">cveClient</a></td>
      <td>
          <ul>
               <li>A client with a simple GUI</li>
               <li>Can be installed locally or run from the internet through a web browser</li>
          </ul>
     </td>
    </tr>
      <tr>
      <td style="padding-left:3%;"><a href="https://github.com/RedHatProductSecurity/cvelib/tree/cve-services-2.1.0">cvelib</a></td>
      <td>
          <ul>
               <li>A command line client</li>
               <li>Can downloaded and incorporated into existing tooling structure</li>
          </ul>
     </td>
    </tr>
  </table>

If your organization has created a unique automation framework that interfaces with CVE Services, contact your framework administrator to determine their plans for migrating to CVE Services 2.1 

If there is concern that the client you are using will not be upgraded by October 3, following are some options that may work for you:

* Prior to October 3, reserve a “block” of IDs to carry you through the month while your clients are upgraded.
* Temporarily adopt one of the publicly available clients that are being actively supported by community members. 

As we get closer to the deployment date for Phase I, we will send out reminders and note the specific days that CVE Records processing will be suspended while we update the software and the repositories. 

<h4>Preparing for Phase II (Week 4 October)</h4>

Phase II deployment will be an update to make the CVE Services 2.1 - RSUS endpoints available to the CVE Services clients for use by the CNA community.

If you wish to take advantage of these new endpoints, the client that you use will need to be designed to specifically do that.  You may adopt one of the recommended clients listed above (which will upgraded to take advantage of the new endpoints).  If you are operating in a unique organizational CVE framework, contact your framework administrators to gain insight into their plans for adoption of CVE JSON 5.0 and CVE Services 2.1 

Note that all of the old CVE Record submission processes (using CVE JSON 4.0) [see Bulletin #6](https://cveproject.github.io/automation-transition#bulletin-number-6) will be maintained for a period of time after this deployment, so you need not adopt CVE JSON 5.0/CVE Services 2.1  immediately, however, you should begin thinking about how you are going to do that in the very near future. 

><strong>CNAs should also make preparations to participate in the virtual “[CVE Services Workshop](https://www.cve.org/Media/News/item/news/2022/08/30/CVE-Services-Workshop-for-CNAs)” for CNAs to learn how to use CVE Services 2.1/CVE JSON 5.0 scheduled for November 2, 2022, from 11:00 a.m. – 5:00 p.m. ET. Learn more [here](https://www.cve.org/Media/News/item/news/2022/08/30/CVE-Services-Workshop-for-CNAs).</strong>

Questions? Please use the [CVE Request Web Forms](https://cveform.mitre.org/) and select “Other” from the dropdown.

## Bulletin Number 8
<strong>*SAVE THE DATE -“CVE Services Workshop” for CNAs to be held on November 2, 2022  —  August 25, 2022*</strong>

[*CVE Services Workshop* for CNAs to Be Held on November 2, 2022](https://www.cve.org/Media/News/item/news/2022/08/30/CVE-Services-Workshop-for-CNAs) — This announcement for CNAs about the upcoming *CVE Services Workshop* was sent to the CVE CNA Discussion email list on August 25, 2022 and posted on the main CVE website on August 30, 2022.

Details about the [CVE Services 2.1](https://cveproject.github.io/automation-cve-services#services-overview)/[CVE JSON 5.0](https://cveproject.github.io/automation-cve-services#json-overview) deployment plan and schedule will be announced very soon, so please keep an eye out. 

Questions? Please use the [CVE Request Web Forms ](https://cveform.mitre.org/) and select “Other” from the dropdown.

## Bulletin Number 7
<strong>*Call for Community Penetration Testing Volunteers to Test CVE Services 2.1 —  June 23, 2022*</strong>

The CVE Program is preparing for the deployment of the [CVE Record Submission and Upload Service (RSUS)](/automation-cve-services#services-overview), and an updated data format (i.e., [CVE JSON 5.0](/automation-cve-services#json-overview)).

The program thanks those of you who participated in previous milestones (e.g., early adoption of the CVE ID Reservation, CVE Services Requirements collection, CVE Services code development and review, Penetration Testing and Security analysis) as we move forward with development, testing, and deployment.

#### <strong>A request for continued support: CVE Services 2.1 Penetration Testing II, July 18-July 29</strong>

We performed Penetration Testing on [CVE Services 2.1](/automation-cve-services#services-overview) in March 2022, during which we identified issues that must be addressed prior to RSUS and JSON 5.0 deployment.

Beginning July 18 (and running through July 29) we will be engaging in another round of community penetration testing to achieve a level of assurance necessary to deploy. The program needs your help! The community is an integral part of building assurance and previously made substantial contributions from a testing perspective. If you have interest, contact the AWG Chair Kris Britton and he will get you the information you need to get started.

#### <strong>If you cannot participate in the Penetration Testing II event, you can still get familiar with CVE Services 2.1</strong>

CVE Services 2.1 will be a major upgrade to CVE Services 1.1.1 as it will provide the API for “client applications” to not only reserve CVE IDs in “near real time” and manage your own “user base” but it will also support the automated submission and update of CVE Records. When it is deployed, CNAs will be able “Post” records immediately to the CVE List with the records being available to the public in near real-time. 

Contact the AWG Chair if you have interest in either of the following:

* Using the “CVE Services Testing Instance” to test your client for CVE Services 2.1
* Joining the [CVE Automation Working Group (AWG)](https://www.cve.org/ProgramOrganization/WorkingGroups) which meets every Tuesday to discuss requirements, status, and all things related to CVE Services 

Please check this page regularly for updates. You may also [contact us](https://cveform.mitre.org/) with any comments or concerns.

## Bulletin Number 6
<strong>*Submitting CVE Records after CVE Service 2.x/JSON 5.0 Roll-out —  May 20, 2022*</strong>

As we prepare for CVE Services 2.x/JSON 5.0 roll-out in the coming weeks, there have been a number of questions about the various methods CNAs currently use to make CVE ID reservations and publish CVE Records and which methods will continue to be supported post deployment.

This bulletin clarifies the CVE Program specific methods that will be available to CNAs for reserving CVE IDs and submitting CVE Records after CVE Services/JSON 5.0 deployment. For non-CNAs, the existing method for requesting CVE IDs will not be affected.

<h3>Non-CNA Submission Methods</h3>
Non-CNAs will continue to contact the appropriate CNA to request CVE IDs, as described on the [Report/Request](https://www.cve.org/ResourcesSupport/ReportRequest) page on the CVE Program website. The CNA that assigns the ID will publish the CVE Record.

In addition, the CVE Program Secretariat will continue to maintain the [CVE Program Request web form](https://cveform.mitre.org/) for non-CNAs to submit vulnerability reports.

<h3>CNA Submission Methods</h3>
For CNAs, there will be five methods to reserve CVE IDs and submit CVE Records. Some methods will be retired over time while others will have constraints, but all five methods described below will be available for use immediately after CVE Services 2.x/JSON 5.0 is deployed.

CNAs that don’t yet have a CVE Services account may contact their Root to receive account credentials ahead of deployment.

<br/>

<h4><i>Method 1: The current CVE Program Secretariat Web Forms</i></h4>

This method allows CNAs to submit CVE Records in multiple formats: JSON 4.0, CSV, and flat file.
For a limited time, CNAs will continue to be able to request CVE ID Reservations and publish CVE Records as they do today using the CVE Program Secretariat [CVE Program Request web forms](https://cveform.mitre.org/). All currently supported input formats will continue to be supported, but this method will not process JSON 5.0 formatted input.

<hr style="border:1px solid red">

<h3>This submission method will be retired 90 days after CVE Services/JSON 5.0 is deployed.</h3>

<hr style="border:1px solid red">

<br/>

<h4><i>Method 2: CVE List GitHub Submission Pilot</i></h4>

This method allows CNAs to submit CVE Records in JSON 4.0 using GitHub pull requests. 
For a limited time, CNAs will continue to be able to use the [CVE List GitHub Submission Pilot](https://github.com/CVEProject/cvelist) to submit CVE Records in JSON 4.0, which will then be upconverted to JSON 5.0 records. 

<hr style="border:1px solid red">

<h3>This submission method will be retired 90 days after CVE Services/JSON 5.0 is deployed.</h3>

<hr style="border:1px solid red">

<br/>

<h4><i>Method 3: Vulnogram</i></h4>

This method is an existing web-based tool for reserving CVE IDs and creating and submitting CVE Records that is currently in use by CNAs. JSON 4.0 will continue to be supported in this method for 90 days post deployment.

After CVE Services/JSON 5.0 is deployed, this method will only accept direct user input (i.e., no attached files) and will submit JSON 5.0 CVE Records directly to CVE Services on the CNA’s behalf for publication on the CVE List. 

To use this method, CNAs will need to present their CVE Services User ID and authentication token through [Vulnogram](https://vulnogram.github.io/cve5/#editor) to identify/authenticate to CVE Services. New users, please request CVE Services credentials from your Root. 

<hr style="border:1px solid green">

<h3>Active submission method.</h3>

<hr style="border:1px solid green">

<br/>

<h4><i>Method 4: Adopt an available CVE Services Client</i></h4>

CVE Services is implemented as a Client/Server architecture. This method enables CNAs to adopt an already existing client and install and execute it in their own environment to assign CVE IDs and create and submit CVE Records. 

Three clients are currently available for use as part of CVE Services/JSON 5.0 deployment:

 * [Vulnogram web-based interface](https://vulnogram.github.io/cve5/#editor) (described above as Method 3)
 * [Red Hat command line interface – cvelib](https://github.com/RedHatProductSecurity/cvelib)
 * [CERT/CC simple HTML interface – cveClient](https://github.com/CERTCC/cveClient)

<hr style="border:1px solid green">

<h3>Active submission method.</h3>

<hr style="border:1px solid green">

<br/>

<h4><i>Method 5: CNAs can develop their own clients</i></h4>

CNAs may develop their own CVE Services clients. The CVE Program is currently preparing documentation to support that development, which will be announced in a future bulletin.

<hr style="border:1px solid green">

<h3>Active submission method.</h3>

<hr style="border:1px solid green">

<br/>

Please check this page regularly for updates. You may also [contact us](https://cveform.mitre.org/) with any comments or concerns.

<br/>

## Bulletin Number 5
<strong>*JSON 5.0 Format Record Review —  March 23, 2022*</strong>

The CVE Program transition to CVE JSON 5.0 continues with the community review of historical JSON 4.0 records that have been converted to JSON 5.0 format.

The message below, sent to CNAs by the Quality Working Group (QWG) on March 21, 2022, announces that review:

CNAs,

The GitHub submission pilot has been using an experimental JSON format (version 4.0) for publishing CVE Records. The CVE Quality Working Group has been working to improve this format for use with the upcoming [CVE Services API](https://github.com/CVEProject/cve-services), with a better-specified schema while fulfilling new requirements from the CVE Program ([version 5.0](https://github.com/CVEProject/cve-schema).

As part of this process, all existing CVE Records (about 181 thousand) are being programmatically upconverted and are available at [https://github.com/CVEProject/cvelistV5/tree/master/review_set](https://github.com/CVEProject/cvelistV5/tree/master/review_set) (last updated March 15th).

An index of these records by the CNAs is available here [https://cveproject.github.io/quality-workgroup/reports/](https://cveproject.github.io/quality-workgroup/reports/). You can also compare the records and their display previews for any converted CVE ID using the tool [https://vulnogram.github.io/seaview/](https://vulnogram.github.io/seaview/).

During this process, 314 records had issues with the data and are autocorrected to ensure we have valid content in the CVE Records. Such corrections include trimming excessively long fields and dropping invalid dates and data. Such records are reported here: [https://cveproject.github.io/quality-workgroup/reports/warnings]( https://cveproject.github.io/quality-workgroup/reports/warnings).

 <ol>
   <li>
     Please review <a href="https://cveproject.github.io/quality-workgroup/reports/">your CVE Records</a> to ensure the <a href="https://github.com/CVEProject/cve-schema/tree/master/schema/v5.0/support/CVE_4_to_5_converter">upconversion script</a> did not alter the meaning of the CVE Records.
    <br><br>
    If you believe <a href="https://github.com/CVEProject/cve-schema/tree/master/schema/v5.0/support/CVE_4_to_5_converter">the upconversion script</a> has a bug, please raise an issue at <a href="https://github.com/CVEProject/cve-schema/issues">https://github.com/CVEProject/cve-schema/issues</a> or suggest changes to the <a href="https://github.com/CVEProject/cve-schema/tree/master/schema/v5.0/support/CVE_4_to_5_converter">upconverter script</a> using a pull request. The upconverter will be used to continually transform any JSON 4.0 submissions to JSON 5.0 format for use in the CVE Services API during the transition phase while CNAs migrate to CVE JSON 5.0.
    <br><br>
  </li>
  <li>
    Please <a href="https://cveproject.github.io/quality-workgroup/reports/warnings">review this warnings report</a> to check if you have any CVE Records that triggered warnings or errors.
   <br><br>
   If you have a CVE Record that needs to be fixed, you have a few options:
   <br><br>
      <ul>
        <li>(Preferred) wait for the record submission feature in the CVE Services to be available (TBA)</li>
        <li>Submit corrections to the records via the Git pilot submission process</li>
        <li>No action is needed if the autocorrects make sense to you</li>
      </ul>
   <br>
  </li>
  <li>
    The display/layout of the CVE Record information as shown on <a href="https://vulnogram.github.io/seaview/">vulnogram.github.io/seaview</a> would be similar to how these records may be rendered on the new <a href="https://www.cve.org/">cve.org website</a>. Feedback on this new CVE Record display or layout is most welcome.
  </li>
 </ol>

If you have any further questions, please feel free to raise them with the CVE Quality Working Group ([cve-board-qualitywg-list@mitre.org](mailto:cve-board-qualitywg-list@mitre.org) or as issues at [https://github.com/CVEProject/cve-schema/issues](https://github.com/CVEProject/cve-schema/issues).

## Bulletin Number 4
<strong>*CVE Services Transition  —  March 21, 2022*</strong>

This message is to inform you about a revision to the CVE Services deployment schedule that will affect when CVE Services 2.1 is available for use by CNAs.

[CVE Services 2.1](https://cveproject.github.io/automation-cve-services#services-overview) consists of the Record Submission and Upload Service (RSUS) and the new [CVE JSON 5.0](https://cveproject.github.io/automation-cve-services#json-overview) data format. The CVE Program is in the middle of testing CVE Services 2.1. The program thanks the CVE community for participating in the functional and penetration testing during the test period that began on February 25, 2022. 

As a result of the ongoing testing, multiple issues have been identified. The [CVE Automation Working Group (AWG)](https://www.cve.org/ProgramOrganization/WorkingGroups#AutomationWorkingGroupAWG) is currently developing the sprint plans and deployment schedule to remediate the identified issues as quickly as possible. Once developed, the AWG will manage the sprints to fix the identified issues. Then, a second period of testing will be opened to the community. The second testing period is the best way to ensure that the services are effective and secure.

Once these sprints and schedule are better defined, they will be published to enhance community understanding of the issues and foster voluntary participation in the CVE Program (e.g., the AWG). Information related to the sprints and deployment plan will be announced on the [CVE CNA Slack channel](https://cve-cna.slack.com/), [CVE CNA Discussion email list](mailto:cve-cna-list@mitre.org), this [CVE Program Automation Website](/), and on CVE social media. 

To ensure the CVE Program delivers effective, automated, and secure CVE 2.1 services that reduce the transaction costs of program participation, the “CVE Global Summit” is being shifted to a later date so that program participants can get an interactive, “hands on” description of the services to make the transition to the services easier. A new summit date will be announced in the near future.

Please check this page regularly for updates. You may also [contact us](https://cveform.mitre.org/) with any comments or concerns.

## Bulletin Number 3
<strong>*CVE Services Transition  —  March 16, 2022*</strong>

The activities and schedule for the transition to CVE Services 2.1 and CVE JSON 5.0, as provided last month in [Transition Bulletin #2](https://cveproject.github.io/automation-transition#bulletin-number-2), are now underway. This bulletin adds two new activities and schedule updates. Most importantly, it adds an important new notification to CNAs that the [CVE List GitHub Submission Pilot](https://github.com/CVEProject/cvelist) will be retired as part of the transition (see below for details).

<strong>Transition Schedule and Activity Updates</strong>

Detailed descriptions for activities 1-6 below are provided in [Transition Bulletin #2](https://cveproject.github.io/automation-transition#bulletin-number-2). This new bulletin, Transition Bulletin #3, includes the addition of two new activities and updates to the transition schedule, to ensure CNAs have advance notice of all upcoming transition activities and actions needed by CNAs.  

Detailed descriptions of the two newly added activities for Bulletin #3 are included below. They have also been added as items 7 and 8 in the transition schedule that follows.

* <strong>CVE List GitHub Submission Pilot Retirement</strong> &mdash; The CVE List GitHub Submission Pilot is JSON 4.0-based and will not be upgraded to JSON 5.0. As a JSON 4.0 based effort, it will not continue to operate after JSON 4.0 Retirement. It will continue to operate for 3 months after CVE Services 2.1/JSON 5.0 Hard Deployment. After JSON 4.0 Retirement, JSON 5.0 format will be the only format that is available for download (other downloadable formats will be retired), and CNAs will be expected to submit CVE Records in JSON 5.0 format through either CVE Services web application API, or a program designated web interface.

* <strong>CVE List Download Format Changes</strong> &mdash; After JSON 4.0 Retirement, JSON 5.0 format will be the only format available for CVE List downloads. All other download formats will be retired at the same time JSON 4.0 is retired (read [announcement](https://www.cve.org/Media/News/item/blog/2022/01/18/CVE-List-Download-Formats-Are)).

<br>
<strong>Updated Transition Schedule</strong>

><strong>IMPORTANT:</strong> The timeframes in this bulletin have changed. Please see the newest bulletins above for the most current information.

See [Transition Bulletin #2](https://cveproject.github.io/automation-transition#bulletin-number-2) for descriptions of activities 1-6; descriptions for activities 7 and 8 are above.

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

If you have any further questions, please feel free to raise them with the [CVE Quality Working Group](cve-board-qualitywg-list@mitre.org) or as issues at [https://github.com/CVEProject/cve-schema/issues](https://github.com/CVEProject/cve-schema/issues).

## Bulletin Number 2
<strong>*CVE Services Transition  —  February 11, 2022*</strong>
 
><strong>IMPORTANT:</strong> The timeframes in this bulletin have changed. Please see the newest bulletins above for the most current information.

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

Please check this page regularly for updates. In addition, there will be follow-on communications to CNAs on [CVE CNA Discussion email list](mailto:cve-cna-list@mitre.org), on [CVE CNA Slack channel](https://cve-cna.slack.com/), and on CVE social media. You may also [contact us](https://cveform.mitre.org/) with any comments or concerns.

## Bulletin Number 1
<strong>*CVE Services Transition  —  January 6, 2022*</strong>

“[Changes Coming to CVE Record Format JSON and CVE List Content Downloads](https://www.cve.org/Media/News/item/news/2022/01/11/Changes-Coming-to-CVE-Record)” — This initial announcement to CNAs about major changes coming to CVE JSON and Downloads in 2022 was sent to the CVE CNA Discussion email list on January 6, 2022.

For extended community awareness, the announcement was also posted on the main CVE website, on CVE social media, and included in the CVE Newsletter.

## Additional Resources 

CVE Services Clients are hosted on GitHub:
* [cvelib (Red Hat's free CVE Services API)](https://github.com/RedHatProductSecurity/cvelib)
* [cveClient (CERT/CC's free CVE Services simple HTML interface)](https://github.com/CERTCC/cveClient)
* [Vulnogram (free web-based CVE Services interface)](https://vulnogram.github.io/cve5/#editor) 

CVE Services resources are hosted on GitHub:
* [CVE Services Project](https://github.com/CVEProject/cve-services#project)
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
