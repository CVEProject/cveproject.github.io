---
title: Submitting CVE Records to Roots and CNA-LRs
layout: page
---
[Top-Level Roots (TL-Root)](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryTLRoot) and [Roots](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRoot) manage a group of CNAs within a given domain or community. For example, [JPCERT/CC](https://www.cve.org/PartnerInformation/ListofPartners/partner/jpcert) and [Spanish National Cybersecurity Institute, S.A. (INCIBE)](https://www.cve.org/PartnerInformation/ListofPartners/partner/INCIBE) are Roots, and [CISA ICS](https://www.cve.org/PartnerInformation/ListofPartners/partner/icscert) and [MITRE](https://www.cve.org/PartnerInformation/ListofPartners/partner/mitre) are TL-Roots. Both TL-Root are also their own [CNAs of Last Resort (CNA-LR)](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryCNALR). 

### Submitting to Roots and CNA-LRs

Each Root and CNA-LR listed above has its own process for accepting [CVE Records](https://www.cve.org/ResourcesSupport/Glossary?activeTerm=glossaryRecord) (formally called CVE Entries) from CNAs. Contact a specific CNA-LR or Root directly to request their specific submission requirements.

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
