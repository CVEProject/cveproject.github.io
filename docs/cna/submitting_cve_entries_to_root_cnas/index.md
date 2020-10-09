---
title: Submitting CVE Records to Root CNAs
layout: page
---
"Root" CVE Numbering Authorities ([CNAs](https://cve.mitre.org/about/terminology.html#cna)) manage a group of sub-CNAs within a given domain or community. For example, [JPCERT/CC](https://cve.mitre.org/cve/request_id.html#cna-lr) is a [Root CNA](https://cve.mitre.org/about/terminology.html#root_cna), and [CISA ICS](https://cve.mitre.org/cve/request_id.html#cna-lr) and [MITRE](https://cve.mitre.org/cve/request_id.html#cna-lr) are [Top-Level Root CNAs](https://cve.mitre.org/about/terminology.html#tlr-cna). Both Top-Level Root CNAs are also their own [CNAs of Last Resort (CNA-LR)](https://cve.mitre.org/about/terminology.html#cna-lr). 

### Submitting to Top-Level Root and Root CNAs

Each Top-Level Root and Root CNA listed above has its own process for accepting [CVE Records](https://cve.mitre.org/about/terminology.html#cve_record) (formally called CVE Entries) from CNAs. Contact a specific Top-Level Root CNA-LR or Root CNA directly to request their specific submission requirements.

### Submitting to the MITRE Top-Level Root CNA

A program for CNAs to submit CVE Records to the [MITRE Top-Level Root CNA](https://cve.mitre.org/cve/request_id.html#cna-lr) using JSON is available on the [CVEProject](https://github.com/CVEProject/cvelist) website on GitHub.com. All CNAs are eligible to participate.

CNAs may also continue to use the [CVE ID Request web form](https://cveform.mitre.org/) to submit CVE Records to the MITRE Top-Level Root CNA.

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
      
For help, contact the MITRE Top-Level Root CNA:                                      
                                              
* [CVE ID Request web form - choose "Other"](https://cveform.mitre.org/)
* [CNA Coordinator Contact Email](mailto:cna-coordinator@mitre.org)
* [General CVE Team Contact via web form - choose "Other"](https://cveform.mitre.org/)
