---
title: Submitting CVE Records to CNA-LRs
layout: page
---

If the product affected by the vulnerability is not covered by a [CVE Numbering Authority (CNA)](https://www.cve.org/ProgramOrganization/CNAs) partner [listed on the main CVE website](https://www.cve.org/PartnerInformation/ListofPartners), please contact the appropriate [CNAs of Last Resort (CNA-LR)](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCNALR) ([Cybersecurity and Infrastructure Security Agency (CISA) Industrial Control Systems (ICS)](https://www.cve.org/PartnerInformation/ListofPartners/partner/icscert) and [MITRE Corporation](https://www.cve.org/PartnerInformation/ListofPartners/partner/mitre)), per below.

### Submitting to CNAs

Follow the instructions at [Request a CVE ID](https://www.cve.org/ResourcesSupport/ReportRequest#RequestCVEID).

### Submitting to the CISA ICS CNA-LR

Follow the instructions at [Report Incidents, Phishing, Malware, or Vulnerabilities to CISA ICS](https://www.cisa.gov/uscert/report).

### Submitting to the MITRE CNA-LR

A program for CNAs to submit CVE Records to the [MITRE CNA-LR](https://www.cve.org/PartnerInformation/ListofPartners/partner/mitre) using JSON is available on the [CVEProject](https://github.com/CVEProject/cvelist) website on GitHub.com. All CNAs are eligible to participate.

CNAs may also continue to use the [CVE ID Request web form](https://cveform.mitre.org/) to submit CVE Records to the MITRE CNA-LR.

#### Resources                                     

* [How to Contribute](https://cve.mitre.org/cve/cna/CVE_Entry_Creation.pptx)
  * [GitHub](https://cve.mitre.org/cve/cna/CVE_Entry_Submission_Process.pptx)
  * [Web form](https://cve.mitre.org/cve/cna/CVE_Entry_Submission_Process.pptx)
* [CVE JSON Schema Repository](https://github.com/CVEProject/automation-working-group/tree/master/cve_json_schema)
  <ul>
    <li><a href="https://github.com/CVEProject/automation-working-group/blob/master/cve_json_schema/DRAFT-JSON-file-format-v4.md">CVE ID JSON File Format 4.0 (Draft)</a></li>
    <li><a href="https://github.com/CVEProject/automation-working-group/blob/master/cve_json_schema/CVE_JSON_4.0_min_public.schema">Schema for validating a JSON file against the minimal CVE structure</a></li>
  </ul>
* [CVE Automation WG Tools](https://github.com/CVEProject/automation-working-group/tree/master/tools)
  <ul>
    <li><a href="https://github.com/CVEProject/automation-working-group/blob/master/tools/cmdlinejsonvalidator.py">Python script to validate JSON files (requires a valid schema file)</a></li>
  </ul>
* Vulnogram - tool for creating and editing CVE information in CVE JSON format:
  <ul>
  <li><a href="https://github.com/Vulnogram/Vulnogram">https://github.com/Vulnogram/Vulnogram</a></li>
  <li><a href="https://vulnogram.github.io/">https://vulnogram.github.io/</a></li>
  </ul>

### Help
      
For help, contact the MITRE Top-Level Root:                                      
                                              
* [CVE ID Request web form - choose "Other"](https://cveform.mitre.org/)
* [General CVE Team Contact via web form - choose "Other"](https://cveform.mitre.org/)
