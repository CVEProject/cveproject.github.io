---
title: Submitting CVE Entries to Root CNAs
layout: page
---
"Root" CVE Numbering Authorities (CNAs) manage a group of sub-CNAs within a given domain or community. Examples of organizations currently participating as [Root CNAs](https://cve.mitre.org/cve/cna.html#cna_types) include [Distributed Weakness Filing Project](https://cve.mitre.org/cve/request_id.html#cna_participants), [JPCERT/CC](https://cve.mitre.org/cve/request_id.html#j), and the [CVE Program Root CNA](https://cve.mitre.org/cve/request_id.html#cna_participants).

### Submitting to Root CNAs

Each Root CNA listed above has its own process for accepting CVE Entries from CNAs. Contact a specific Root CNA directly to request their specific submission requirements.

### Submitting to the Program Root CNA

A pilot program for CNAs to submit CVE Entries to the [Program Root CNA(https://cve.mitre.org/cve/request_id.html#cna_participants) using JSON is currently being hosted on the [CVEProject](https://github.com/CVEProject/cvelist) website on GitHub.com. All CNAs are eligible to participate in the pilot.

CNAs may also continue to use the [CVE ID Request web form](https://cveform.mitre.org/) to submit CVE Entries to the Program Root CNA.

#### Resources                                     

* [How to Contribute](https://github.com/CVEProject/cveproject.github.io/blob/master/docs/cna/Entry_Submission_Process.pptx)
  * [GitHub](https://github.com/CVEProject/cvelist/blob/master/CONTRIBUTING.md)
  * [Web form](http://cveproject.github.io/docs/cna/Web%20Form%20Entry%20Submission%20Process.pptx)
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
      
For help, contact the Program Root CNA:                                      
                                              
* [CVE ID Request web form - choose "Other"](https://cveform.mitre.org/)
* [CNA Coordinator Contact Email](mailto:cna-coordinator@mitre.org)
* [General CVE Team Contact Email](mailto:cve@mitre.org)
