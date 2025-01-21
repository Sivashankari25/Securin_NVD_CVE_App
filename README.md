# Securin_NVD_CVE
NVD - CVE API:
The CVE API is used to easily retrieve information on a single CVE or a collection of
CVE from the NVD. Pls refer to the below NVD CVE documentation to get more
information.
https://nvd.nist.gov/developers/vulnerabilities
Problem Statement:
1. Consume the CVE information from the CVE API for all the CVE's and store
it in a Database of your choice. - (API BaseURL -
https://services.nvd.nist.gov/rest/json/cves/2.0)
2. Hint for accessing all the CVE's from API - Through a series of smaller
“chunked” responses controlled by an offset startIndex and a page lim
resultsPerPage users may page through all the CVE in the NVD.
3. Apply data cleansing & de-duplication, ensure data quality wherever
applicable
4. CVE details should be synchronized into Database periodically in batch
mode in a specific time period - (This can be full data refresh or increment
refresh for modified data alon
5. Develop API’s to read & filter the CVE details by below parameters -
● CVE ID
● CVE ID’s belogs to a specific year
● CVE Score (Field to ref -
metrics.cvssMetricV2.cvssData.baseScore or
metrics.cvssMetricV3.cvssData.baseScore)
● last Modified in N days
6. Read the API and visualise it in UI using HTML, CSS and Javascript
7. Prepare the API documentations for each operations.
8. Write well defined unit test cases for the functionalitie
9. Code should be clear, vulnerable free & well tested and should follow the
best practices and standards.
The first page should contain:
1. The route path should be /cves/list.
2. Read the API and display its results in a table with a "Total Records" count.
3. Include "Results Per Page" below the table, offering options of "10", "50", and "100",
with a default selection of "10". Whenever an option is chosen, execute the
respective API call to retrieve the records.(Good to have)
4. Add server side “Pagination” functionality (Optional - Added advantage)
5. Add server side “sorting” for “Dates” (Optional - Added advantage)
