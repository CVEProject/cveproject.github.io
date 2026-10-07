---
title: CVE Search API Responsible Use Guidelines (Beta)
layout: page
---

The CVE Search API provides programmatic access to CVE Record data for targeted search, automation, and integration use cases. During the beta period, the service is available without identification or authentication requirements.
The Search API is a shared community resource. The following guidelines are intended to help users build integrations that use the service efficiently, respect service limits, and avoid unnecessary impact on other users.

## 1. Use the appropriate CVE data access method
The CVE Search API is intended for targeted searches and application queries. It is **not** intended to create, synchronize, or maintain a complete local copy of the CVE List.
If your use case requires the complete CVE dataset, large-scale backfills, or ongoing synchronization of a local repository, use the CVE Program's bulk data distribution capability [link] instead of the Search API.
Do not attempt to reconstruct or synchronize the complete CVE dataset by dividing it into many Search API queries for the purpose of working around Search API result limits.

## 2. Make only the requests your use case requires
Avoid continuous polling driven only by the possibility that new or modified CVE Records may be available. Where periodic queries are appropriate, choose a frequency that reflects the actual freshness requirements of your application or analysis process.
Cache and reuse previously retrieved results where practical. For repeated targeted searches, use applicable filters, including publication or modification date parameters such as `pubStartDate` or `lastModStartDate`, to reduce unnecessary retrieval of information you have already processed.
If CVE data is used broadly within an organization or service, a centralized retrieval and caching approach is preferable to many independent clients repeatedly making the same or substantially similar queries.
Applications distributed to large numbers of users MUST, where practical, avoid architectures in which every end-user device independently and repeatedly sends duplicate queries directly to the CVE Search API.

## 3. Respect rate limits
The current beta rate limit is **10,000 requests per five-minute period per IP address**.
This limit is a protective service ceiling, not a recommended operating rate. Applications should make only the requests needed for their use case and should not be designed to operate continuously at or near the limit.
Multiple applications or users that share the same public IP address may collectively contribute to that IP address's rate limit.
When the service returns HTTP `429 Too Many Requests`, clients should reduce their request rate and wait before retrying. Use bounded retries with progressively longer delays rather than immediately or continuously resubmitting failed requests.
Do not attempt to circumvent rate limits or other service restrictions, including by distributing requests across multiple IP addresses, proxies, processes, or application instances for the purpose of increasing effective request throughput.
Do not use the public beta service for load testing, stress testing, or capacity benchmarking.

## 4. Use pagination and the result window appropriately
The current beta pagination limits are:
- Default `resultsPerPage`: **20**
- Maximum `resultsPerPage`: **500**
- `pageNumber` starts at **1**
- A requested page must satisfy `pageNumber x resultsPerPage <= 10,000`
A search may report an exact total greater than 10,000 matching records, but the API cannot page beyond the 10,000-record result window.
Request only the pages needed for your use case and avoid repeatedly retrieving pages that have already been processed unless there is a specific need to do so. If a query produces more results than can be retrieved through the result window, consider narrowing the query. If the underlying need is bulk retrieval or dataset synchronization, use the CVE Program's bulk data distribution capability instead.

## 5. Avoid unnecessary concurrency and duplicate traffic
Applications should avoid issuing large numbers of simultaneous requests when the same result can reasonably be achieved through efficient filtering, permitted page sizes, caching, or reuse of previously retrieved data.
Where many users depend on the same CVE information, retrieving the data once and redistributing or caching it within the application or organization is preferable to generating separate, duplicate Search API request streams for each consumer.
If you publicly distribute an app to use this API, it must use the User-Agent header to provide an app name, app version, and contact information. Examples of contact information include a developer email address or a public repository where issues can be filed.

## 6. Design beta integrations for changing service conditions
The CVE Search API is currently a beta service. Availability, performance, data coverage, searchable fields, service limits, and other technical characteristics may change as the beta evolves.
Applications should tolerate temporary service unavailability and should not assume that every request will succeed immediately. Clients should use bounded retry behavior and should not depend on undocumented service behavior.
The CVE Program may revise these guidelines or service limits during the beta period.

## 7. Understand beta search and data-coverage limitations
Not all CVE Record data is equally represented or searchable during the beta period. Some queries may return fewer results than expected because relevant records or fields have not yet been populated or indexed for the applicable search capability.
Accordingly, the absence of a CVE Record or particular field from a Search API result should not necessarily be interpreted as evidence that the CVE Record or information does not exist.

Once a CVE Record has been indexed into the Search API's search infrastructure, applicable publication-date and modification-date parameters can be used to locate it according to the documented query behavior.

## 8. Follow CVE Program terms for use and redistribution
Use of CVE Program data, including redistribution of CVE Record data retrieved through the Search API, must comply with the CVE Program Terms of Use:
https://www.cve.org/Legal/TermsOfUse

## 9. Protect sensitive information in API requests
CVE Search API requests are logged and may be retained for up to **one year**. Use of the service is also subject to the CVE Program Privacy Policy:
https://www.cve.org/Legal/PrivacyPolicy
Do not place passwords, authentication credentials, personal information, proprietary information, or other sensitive information in search parameters or other request fields.

## 10. Use public feedback channels appropriately
Feedback on the beta Search API is encouraged through the CVE Search API GitHub project:
https://github.com/CVEProject/CVE-Search-API
Information submitted through public GitHub resources may be visible to others and may be reused or redistributed for purposes relevant to CVE Program operation. Do not include confidential, proprietary, personal, or other sensitive information in public feedback submissions.

## Questions and feedback
The beta period is intended to help the CVE Program and the community evaluate and improve the Search API. Users are encouraged to report unexpected search behavior, data-coverage issues, documentation problems, and requests for additional capabilities through the CVE Search API GitHub project.
These Responsible Use Guidelines may be updated as the Search API evolves.
