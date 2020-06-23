# June 23, 2020 (12.5) 
## Added 
- **Campaign finance data**: Added active and terminated indicators on the global search and committee search on the [data landing page](https://www.fec.gov/data/) to make it easier for users to know which committees are still active, at a glance
- **Campaign finance data:** Added language to committee profile pages for those that have transitioned from a candidate committee to a nonconnected PAC within a single cycle
- **API:** Added filter for `load_date` to Schedule A endpoint, allowing users to filter for most recently added transactions
- **API:** Added pg_date indexes to fec_fitem_sched_a tables to support users’s request to filter on pg_date to download data for their usage
- *Help for candidates and committees*:**  Added a new [page](https://www.fec.gov/about/leadership-and-structure/james-e-trainor-iii/) for newly-sworn in Commissioner Trainor
## Changed
- **General:** Updated the message for when a search yields no results
- **General:** Updated the feedback box directions to make it more clear we are seeking feedback about the website and direct other feedback and questions to the appropriate places within the FEC
- **Help for candidates and committees:** Updated the Campaign Guide for Congressional Candidates for accessibility
- **Help for candidates and committees:** Changed the icon for example template pages to make them consistent
## Fixed
- **Campaign finance data:** Corrected an error message to show a “Page not found” for candidate and committee profile pages when an invalid candidate or committee ID is provided in the URL
- **API:** Updated a URL in the description of presidential end point to direct users to the appropriate methodology page
## Under the hood
- Updated search index for transition.fec.gov
- Provided user with an error message when MUR documents failed to load
- Moved inline CSS from television ad example templates to stylesheets and removed from template
- Updated Django minor version from 2.2.11 to 2.2.13
- Redirects from older files on transition.fec.gov to newer content were put in place.
- Added flake8 linting to `pytest`

# June 9, 2020 (12.4) 
## Added
- **Legal resources:** Added a single new administrative fines calculator for committees to estimate fines for late or non-filed reports 
- **Campaign finance data**: Added `active/terminated` indicator to committee profile page
## Changed
- **Legal resources:** Updated links to the 2020 11 CFR on our [regulations page](https://www.fec.gov/legal-resources/regulations/#go-to-11-cfr)
- **Legal resources:** Moved a page containing [enforcement and compliance procedural materials](https://www.fec.gov/legal-resources/enforcement/procedural-materials/) from the transition site to fec.gov
- **General:** Updated the [Office of Inspector’s General’s web page](https://www.fec.gov/office-inspector-general/) 
- **Help for candidates and committees:** Various pages were updated to reduce duplicative content and point users to the new page on [disclaimer notices](https://www.fec.gov/help-candidates-and-committees/advertising-and-disclaimer/)

# May 26, 2020 (12.3) 
## Added
- **API:** Added validation for Schedule A pagination requests so API users could paginate through results
- **API:** Added is_active column in endpoint: name/committees/ to help distinguish between committees that are active or terminated on fec.gov

## Changed
- **Help for candidates and committees:** The [web page containing information on disclaimer notice rules](https://www.fec.gov/help-candidates-and-committees/advertising-and-disclaimers/) was revamped to make it easier to navigate and include helpful examples.
- **General:** The [Office of Inspector’s General’s web page](https://www.fec.gov/office-inspector-general/) was updated.

## Fixed
- **Campaign finance data:** Fixed case-sensitive candidate and committee profile pages that were causing errors

## Under the hood
- Created alternative 500 error messaging in the CMS
- Added is_active column to two materialized views
- Update python code to include missing cites on AO’s.  Run API task to reload them manually.
- Redirects from older files on transition.fec.gov to newer content were put in place.

# May 12, 2020 (12.2) 
## Under the hood
- Updated vulnerable webargs package in eregs and API applications
- Updated vulnerable wagtail package
- Set API `get` request timeouts in CMS


# April 28, 2020 (12.1) 
## Added
- **Legal resources:** A new [page](https://www.fec.gov/legal-resources/policy-and-other-guidance/guidance-documents/) allows users to search Commission guidance documents that set forth a policy on a statutory, regulatory or technical issue, or interpret a regulation.
- **API:** Added is_active column to `/committee/{committee_id}/history/` endpoint

## Changed
- **Campaign finance data:** Added a way to access [pages explaining campaign finance data](https://www.fec.gov/campaign-finance-data/about-campaign-finance-data/) to our page on How to [research public records](https://www.fec.gov/introduction-campaign-finance/how-to-research-public-records/#data-tutorials) page
- **General**: Updated the “Official website of the US government with more information and styling

## Fixed
- **Help for candidates and committees:** Fixed missing feedback button on some pages
- **Campaign finance data:** Fixed download link for disbursements on presidential map 

## Under the hood
- Remove unused database objects
- Increased number of API application instances to ten (10)
- Redirects from older files on transition.fec.gov to newer content were put in place.
- Added sitemaps for guidance document searching for version control


# April 14, 2020 (11 innovation) 
## Added
- **Help for candidates and committees:** Added examples of [proper disclaimers]([https://www.fec.gov/help-candidates-and-committees/making-disbursements/advertising/) for party committee fundraising and advertising to various pages.

## Changed
- **Help for candidates and committees:** Revised a [page on filing frequency](https://www.fec.gov/help-candidates-and-committees/dates-and-deadlines/filing-frequency-type-filer/) to make it more clear to candidates that they must file pre-election reports in addition to quarterly reports.

## Under the hood
- Updated SEO of press releases that cut off the name of the court case they referenced to incorporate the case names.

# March 20, 2020 (11.6) 
## Added
- **Campaign finance data:** Added [Presidential candidate map](https://www.fec.gov/data/candidates/president/presidential-map/)
- **Campaign finance data:** Added new endpoint `/communication_costs/aggregates/`

## Under the hood
-  Enabled CircleCI pipelines on fec-cms, openFEC, fec-eregs, fec-pattern-library,
   fec-infrastructure and fec-dns repos

# March 10, 2020 (11.5) 

## Added
- **Legal Resources:**  Published a [new page](https://www.fec.gov/legal-resources/regulations/explanations-and-justifications/chronological-index-2020-2029-ejs/)  with the Commission’s explanation and justifications for regulations taking effect from 2020 to 2029
- **Help for candidates and committees:** Added disclaimer examples to the “Advertising and disclaimers” [page](https://www.fec.gov/help-candidates-and-committees/making-disbursements/advertising/) 

## Changed
- **Campaign finance data :** Added language to the [candidate data page](https://www.fec.gov/data/browse-data/?tab=candidates) above the presidential map accordion to indicate the time period covered by the data
- **Campaign Finance Data:** Independent expenditure data table “most recent” checkbox now includes unknown version 

## Under the hood
- In fec-cms repo, update Wagtail to v2.7 & Django to v2.2.10 LTS (Long Term Support) versions 
- In openFEC repo, update Node to LTS v10.16.* & NPM to v6.13.7
- F24 version issue has been fixed  

# February 25, 2020 (11.4) 
## Added

- **Help for candidates and committees:** Published a new page on [publicly funded presidential spending limits](https://www.fec.gov/help-candidates-and-committees/understanding-public-funding-presidential-elections/presidential-spending-limits-2020/) for 2020] 
- **Help for candidates and committees:** Published a new page on [lobbyist bundling disclosure requirements](https://www.fec.gov/help-candidates-and-committees/lobbyist-bundling-disclosure/)
- **API :** Added five endpoints to support a new presidential map feature  
    - /presidential/contributions/by_candidate/
    - /presidential/contributions/by_size/
    - /presidential/contributions/by_state/
    - /presidential/coverage_end_date/
    - /presidential/financial_summary/

## Changed
- **Legal resources :** Added a new section on audit report processing and policies to the [Audit Reports page](https://www.fec.gov/legal-resources/enforcement/audit-reports/#audit-report-processing-and-policies)
- **Help for candidates and committees:** Updated the [coordinated party expenditure limits](https://www.fec.gov/help-candidates-and-committees/making-disbursements-political-party/coordinated-party-expenditures/coordinated-party-expenditure-limits/) page with the limits for 2020
- **Campaign finance data:** Updated the [help page for presidential map data](https://www.fec.gov/campaign-finance-data/presidential-map-help/)
- **Campaign finance data:** Updated language above presidential accordions explaining contents of files
- **Campaign finance data:** Updated Independent Expenditure methodology
- **Campaign finance data:** Updated text of version checkbox 
- **Campaign finance data:** Updated Independent Expenditure report type toggle functionality

## Under the hood
- Updated Gunicorn from version 19.7.1 to 19.10.0
- Updated GitPython from version 2.1.8 to 2.1.15
- Upgraded Handlebars from version 4.3.0 to 4.7.2
- Switched eRegs from shared-psql to medium-psql-redundant and bound application to new database
- Added tests to Independent Expenditure data table
- Conditionally hide presidential section from docs until feature release
- Add presidential endpoint descriptions
- Add transfers_from_affiliated_committees field to /presidential/financial_summary/ endpoint
- Most recent Independent Expenditures logic updates

# February 11, 2020 (11.3) 
## Added

- **Campaign finance data:** Added current version filters to Independent expenditures datatables 
- **Campaign finance data:** Added bulk presidential map data downloads within browse data candidates tab 

## Under the hood
-  Improved sitewide search by making sure archived pages that have been taken offline do not appear in search results.
-  Upgraded Django to version 1.11.27

# January 29, 2020 (11.2) 
## Added
- **API:** Added filing_form and is_notice filters to /schedules/schedule_e/efile/ endpoint
- **About the FEC:** Added [meeting pages](https://www.fec.gov/meetings/?tab=executive-sessions) for 2020 executive sessions.
## Changed
- **Legal resources:** Updated links to GPO’s website on the [Statutes](https://www.fec.gov/data/legal/statutes/) page to point to the most recent versions of Titles 52 and 26.
- **Help for candidates and committees:** Updated information on multistate independent expenditure reporting for [PACs](https://www.fec.gov/help-candidates-and-committees/making-independent-expenditures/reporting-independent-expenditures-form-3x/) and [other filers](https://www.fec.gov/help-candidates-and-committees/making-independent-expenditures/reporting-independent-expenditures-form-5/).

## Under the hood
- Removed null value in cycles, cycles_has_finance and cycles_has_activity from ofec_committee_history_mv
- Legal citations field added to pages that use a full-width template.

# January 14, 2020 (11.1) 
## Added
- **Campaign Finance Data:** Added most recent Statement of Organization to committee profile pages
- **Help for candidates and committees:**  Added new pages regarding [public funding of presidential elections](https://www.fec.gov/help-candidates-and-committees/understanding-public-funding-presidential-elections/) and the [presidential transition and inauguration](https://www.fec.gov/help-candidates-and-committees/presidential-transition-and-inauguration/)
- **Help for candidates and committees:** Added new pages regarding [dates and deadlines for FEC reports in 2020](https://www.fec.gov/help-candidates-and-committees/dates-and-deadlines/)
- **Legal resources:** Added new terms to the glossary

## Changed
- **About the FEC:**  The Home page and Commissioner pages were updated to reflect the new Chair and Vice Chairman for 2020
- **General:** Clarified the license language for code repositories


## Fixed
- **Campaign finance data:** Fixed connected organization field on SSF committee profile pages
- **Campaign finance data:** Fixed the receipt datatable filter label from “Contributor name or ID” to “Recipient name or ID”

## Under the hood
- Updated API documentation for endpoint descriptions
- Added the ability to include legal citation blocks to the full width page Wagtail template
- Updated smart_open and its related python packages


# December 31, 2019 (PI 10 innovation)
## Added
- **Help for candidates and committees**: Published new pages on [presidential public funding](http://www.fec.gov/help-candidates-and-committees/understanding-public-funding-presidential-elections/) and funding the [presidential transition and inauguration](http://www.fec.gov/help-candidates-and-committees/presidential-transition-and-inauguration/)

## Changed
- **Help for candidates and committees**: Revamped the page for [purposes of disbursement](https://www.fec.gov/help-candidates-and-committees/purposes-disbursements/) into a format that allows committees to tab between adequate and inadequate purposes.
- **Help for candidates and committees**: Added links to assist navigation between the sections on [disbursements](https://www.fec.gov/help-candidates-and-committees/making-disbursements/) and [winding down costs](https://www.fec.gov/help-candidates-and-committees/winding-down-candidate-campaign/winding-down-costs/) for candidates.

## Fixed
- **About the FEC**: Fixed missing or broken links for several FEC Record [indexes](https://www.fec.gov/updates/record-archive-1975-2004/)

## Under the hood
- **API**: Added cloud.gov IPs to the API umbrella to limit server side calls to cloud.gov API keys 

# December 10, 2019 (10.6)
## Added
- **API**: Added new electioneering communications endpoint /electioneering/aggregates/

## Under the hood
- Added `TSVECTOR` trigger to schedule a raw efile

# November 26, 2019 (10.5)
## Added
- **About the FEC**: Published a new page on the FEC’s Limited English Proficiency [plan](https://www.fec.gov/about/equal-employment-opportunity/limited-english-proficiency/)

- **Campaign finance data**: Added new pages explaining [API data end points](https://www.fec.gov/campaign-finance-data/about-campaign-finance-data/) 

## Fixed
- **Legal resources**: Uploaded a corrected PDF of the FEC's compilation of federal election campaign laws to the [statutes page](https://www.fec.gov/data/legal/statutes/).
- **Campaign finance data**: Fixed candidate mentioned filter for independent expenditure raw datatable
- **Campaign finance data**: Fixed committee summary page with wrong form or cmte_type.

## November 12, 2019 (10.4) 
## Added
- **Help for candidates and committees**: Added information for host committees, convention committees and inaugural committees to the [Other Filers menu](https://www.fec.gov/help-candidates-and-committees/guides/?tab=other-filers)
- **Legal Resources**: Added a new page on [administrative terminations and debt settlement plans](https://www.fec.gov/legal-resources/policy/administrative-terminations-and-debt-settlement-plans/) 
- **About the FEC**: Added a new page for [Equal Employment Office](https://www.fec.gov/about/equal-employment-opportunity/) at the FEC 

## Changed
- **General**: Added information on paying for communications to the page for citizens on understanding ways to [support federal candidates](https://www.fec.gov/introduction-campaign-finance/understanding-ways-support-federal-candidates/)
- **About the FEC**: Updated the homepage and [leadership and structure page](https://www.fec.gov/about/leadership-and-structure/) to reflect the naming of Commissioner Caroline C. Hunter as Vice Chair

## Fixed
- **Legal resources**: Instead of requiring users to search for statutes by keyword before seeing any of the statutes, all now load by default 
- **Candidate Profile page**: Message showing "no financial data message" now appears for candidates with committees that have not filed disclosure forms

## Under the hood
- Removed unused partition code from API
- Updated schedules/schedule_e  API endpoint to filter by filing_date and dissemination_date columns
- Removed unused materialized view and view from database
- Upgraded`Flask` from 1.0.2 to 1.1.1
- Updated /schedules/schedule_e/efile API endpoint to filter by candidate_id


# October 28, 2019 (10.3) 

## Added
- **About the FEC**: Published a new version of the FEC [organization chart](https://www.fec.gov/about/leadership-and-structure/fec-offices/) 
- **General**: Added new social media images for advisory opinions, weekly digest, open meetings, public hearings, executive sessions, and press releases
- **Campaign finance data**: Added new interactive tool, Where Contributions Come From, to the Raising By The Numbers page
- **API**: Added designation filter to committee history endpoints

## Changed
- **General**: Updated the error message for 500 server errors to include a referral to the FEC’s API status page
- **Help for candidates and committees**: Retired older committee-specific pages about partnerships and redirected to the new, more [comprehensive page](https://www.fec.gov/help-candidates-and-committees/candidate-taking-receipts/partnership-llc-contributions/).
- **General**: Updated default social media image, renamed existing social media images
- **API**: Increased maximum number of committee_id to search to ten

## Fixed
- **About the FEC**: Broken links to FEC meeting documents and minutes from 2000 through 2003 were fixed
- **General**: Fixed layering issues where drop-down menus would sometimes appear behind other elements on the page
- **API**: Fixed filter by committee_id in these endpoints:
    - /schedules/schedule_a/by_size/,
    - /schedules/schedule_a/by_state/,
    - /schedules/schedule_a/by_zip/,
    - /schedules/schedule_a/by_employer/,
    - /schedules/schedule_a/by_occupation/,
    - /schedules/schedule_b/by_recipient/,
    - /schedules/schedule_b/by_recipient_id/,
    - /schedules/schedule_b/by_purpose/ and
    - /schedules/schedule_e/by_candidate/

- **Campaign finance data**: Fixed missing committee information and raising and spending tabs for future cycle candidate committee profile pages 
## Under the hood
- Forked `jmcarp/marshmallow-pagination` repository with `fecgov/marshmallow-pagination` for dependency management
- Added content security policy fix for Wagtail images under app.cloud.gov domain
- Updated search.gov indexing for global sitewide search

# October 15, 2019 (10.2) 
## Added
- **Help for candidates and committees**: Added new pages on [partnership and LLC contributions](https://www.fec.gov/help-candidates-and-committees/candidate-taking-receipts/partnership-llc-contributions/), [assigning debts](https://www.fec.gov/help-candidates-and-committees/handling-loans-debts-and-advances/assigning-debts-another-committee/), [raising and spending funds for the national party convention](https://www.fec.gov/help-candidates-and-committees/taking-receipts-political-party/national-nominating-convention/), [delegate activities](https://www.fec.gov/help-candidates-and-committees/candidate-taking-receipts/delegate-activity/), and reports by [host and convention committees](https://www.fec.gov/help-candidates-and-committees/other-filers/reports-filed-by-host-and-convention-committees/), [monthly filing presidential candidates](https://www.fec.gov/help-candidates-and-committees/filing-reports/monthly-reports-presidential/), and [inaugural committees](https://www.fec.gov/help-candidates-and-committees/filing-reports/inaugural-committee-reports/)

## Changed
- **API**: Revised message for API status errors to point to new [status page](https://www.fec.gov/status)

## Fixed
- **Campaign Finance Data**: Fixed incorrect counts for Schedule E raw data table
- **Campaign Finance Data**: Only link to election profile pages starting in 1980
- **Campaign Finance Data**: Fixed raising and spending tab behavior of candidate profile pages without activity in particular cycle 

## Under the hood
- Increased elasticsearch timeout to allow certain legal resources queries to load
- Fixed logic for loading unpublished legal cases
- Redirected older content pages on transition to updated pages on current site

# October 1, 2019 (10.1) 
## Added
- **Campaign finance data**: Added organization type and committee type to candidate pages
- **General**: Published the latest version of the [Combined Federal/State Disclosure Directory](https://www.fec.gov/introduction-campaign-finance/how-to-research-public-records/combined-federalstate-disclosure-and-election-directory/)
- **General**: Added page for Chair Weintraub's symposium on “Digital Disinformation and the Threat to Democracy: Information Integrity in the 2020 Elections”. 

## Changed
- **General**: Moved the page of archived Record articles from 1975 to 2004 to a new [location](https://www.fec.gov/updates/record-archive-1975-2004/). A link to this archive was added under “About latest updates” and to the no results message when a user searches Updates and gets no results.
- **Legal resources**:  For Matters Under Review changed title to include “closed”
## Fixed
- **Campaign Finance Data**: Fixed “Filter this data” buttons on Candidate and Committee profile pages filings tab to filter by form type
- **Campaign Finance Data**: Fixed pages for candidates with future election years
## Under the hood
- Refactored code for readability and future maintenance
- upgraded api to `python@3.7.4` (required upgrade of dependencies `gunicorn`, `gevent`, and `pandas`)
- Addressed vulnerability around ESLint
- Implemented Google Tag Manager, to be activated at a later date
- Added styles for a future organization chart
- Reorganized classic.fec.gov website to display the Campaign Finance Disclosure Portal as the new homepage
# September 10, 2019 (PI 9 innovation) 
## Fixed
- **Campaign finance data**:  fixed inconsistent data on candidate profile pages 
## Under the hood
- Added secure headers to API and CMS, including a Content Security Policy.
- Refactored three endpoint resource files: CandidateTotalsView, CandidateHistoryView, CommitteeHistoryView.
# August 20, 2019 (9.6) 
## Added
- **API**: Added filters to /schedules/schedule_e/efile/ endpoint.

## Fixed
- **Campaign finance data**: Fixed missing committee type filters (Lobbyist/Registrant PAC, Leadership PAC, and Separate Segregated Fund (SSF) PACs) for receipts, individual contributions and disbursements datatables 
- **Legal**: Fixed the missing mailto link when you try to click "Email our team

## Under the hood
- Added lodash 4.17.13 to “devDependencies” in package.json 
- Upgraded to django@1.11.23


# August 6, 2019 (9.5) 
## Added
- **Help for candidates and committees**: Added reporting examples for party committees to the [Filing party reports page](https://www.fec.gov/help-candidates-and-committees/filing-political-party-reports/#reporting-examples)
- **Help for candidates and committees**: Added language for presidential candidates to the [Guides page for candidates](https://www.fec.gov/help-candidates-and-committees/guides/#cand-comm-guides-candidates-and-their-authorized-committees).
- **API**: Added committee organization type and designation filters to schedules A and B

## Fixed
- **Campaign finance data**: Updated Receipts and Individual Contributions datatables to be able to reset to default table settings
- **Campaign finance data**: Fixed inconsistency between candidate profile page and candidate list page financial data
- **Campaign finance data**: Fixed election profile page data tables to click through to the full election cycle transaction data
- **Campaign finance data**: Fixed doubled totals in schedule A aggregate endpoints
- **API**: Fixed error handling for some sort errors
## Under the hood
- Made a redirect for old candidate registration brochure.
- Refreshed databases with new `tsvector` logic to better couple searched fields with parsed user input. Restored original `parse_fulltext` definition.
- Added diacritical mark handling for `tsvector` field searches

# July 23, 2019 (9.4) 
## Added
- **Help for candidates and committees**: Added guidance for presidential candidates to  various [pages for candidates](https://www.fec.gov/help-candidates-and-committees/guides/?tab=candidates-and-their-authorized-committees) 
- **Legal resources**: Added date filters to MUR search
- **API**: Added endpoint `/schedules/schedule_a/by_state/by_candidate/totals` to aggregate individual total contributes summed over all states by candidate by election cycle
## Changed
- **Legal resources**: Changed citation radio buttons to have a more visually intuitive representation of “selected” state
## Fixed
- **Campaign finance data**: Fixed missing `committee_name` column when exporting `.csv` report files for presidential, House and Senate, and PAC and Party reports data tables.
- **Campaign finance data**: Fixed full-cycle financial summary links on candidate profile pages 
## Under the hood
- Made redirects for various publications

# July 9, 2019 (9.3) 
## Changed
- **Help for candidates and committees**: Uploaded the [Guideline for Presentation in Good Order](https://www.fec.gov/resources/cms-content/documents/guideline-for-presentation-good-order.pdf) and [appendices](https://www.fec.gov/resources/cms-content/documents/guideline-for-presentation-good-order_appendices.pdf) used by publicly funded presidential candidates, and added links to them on the [public funding information page](https://www.fec.gov/introduction-campaign-finance/understanding-ways-support-federal-candidates/presidential-elections/public-funding-presidential-elections/).
- **General**: Updated language of message shown to users of older browsers, including Internet Explorer 10 and below.
## Fixed
- **Campaign finance data**: Fixed 404 error generated by some special election candidates linked from election profile 
- **Campaign finance data**: Made pull-downs for download options are still clickable when they’re the last row of the table
- **General**: Adjusted polyfills to improve appearance and performance for users of older browsers, including Internet Explorer 10 and 11 and last-gen browsers. 
- **General**:  Fixed some unmatched tag warnings that were being displayed for Internet Explorer users.
- **General**:  Resolved an issue with displaying the Calendar and related entries on the home page in Internet Explorer
## Under the hood
- Modified `to_tsvector` arguments to replace all non-alphanumeric characters with whitespace to be compatible with the Python search term parsing
- Add historical candidate inactive data 
- Updated API URL in CMS feature space to point to stage database
- Updated X-UA meta tag for Internet Explorer

# June 28, 2019 (9.2) 
## Added
- **Campaign Finance Data**: Added filter to exclude incumbents not seeking re-election from candidate data tables
## Changed
- **Campaign Finance Data**: Expanded all receipts and individual contributions datatable searches  to all time periods (as long as other criteria are also defined)
- **Campaign Finance Data**: Updated heading styles for filters of all receipts and individual contributions data tables of all receipts and individual contributions data tables
- **Campaign Finance Data**: Added report year to the filter panel of all receipts and individual contributions data tables
- **Campaign Finance Data**: Added multi-year select functionality to report year filter to all receipts and individual contributions
- **Campaign Finance Data**:Updated custom error handling of new all receipts and individual contributions filter interaction
- **Campaign Finance Data**: Clarified the tooltip text of “report time period” on raising and spending data tables
- **Campaign Finance Data**: Removed Separate Segregated Fund options from filters of all receipts and individual contributions datatables because they were not functioning properly
- **Homepage**: Changed the message that’s displayed when no results are found while searching Updates
## Fixed
- **Campaign Finance Data**: Fixed column headers of the election profile page that were not  displaying correctly
- **Campaign Finance Data**: Fixed empty download file bug for RFAIs
- **Campaign Finance Data**: Fixed totals for Puerto Rico Resident Commissioner totals by always showing 4-year cycle totals
- **Campaign Finance Data**: Democratic–Farmer–Labor Party candidates’ raising and spending meters are now colored blue instead of dark gray
## Under the hood
- Added test coverage for candidate endpoints

# June 11, 2019 (9.1) 
## Added
- **API**: Added 'is_active_candidate' filter to /candidates/ to exclude incumbents that have dropped out 
- **Campaign Finance Data**: Added an interactive module to Raising- and Spending-By The Numbers that lists total money raised or spent during a selected race with breakdowns by party
## Changed
- **Campaign finance data**: Applied multi-year and all report year search capability to Disbursement datatables
- **Campaign finance data**: Updated default time period across site to be 2020
- **Legal resources**: Added 2019 regulations to regulations explorer
- **Campaign Finance Data**: Changed any table columns of currency to use the new monospace currency font
## Fixed
- Added validation for proper line number formatting
- Added a better error message for over-rate-limit downloads 
- Fixed incorrect candidate totals for some candidates
- Fixed incorrect search results in house candidate datatables
- Fixed misleading “no data” messages by providing a more complete list of why data could be missing 
- Fixed improper capitalization on house/senate/presidential candidate datatables breadcrumbs and table headers
- Fixed DFL party to display as part of the democratic party color scheme
# May 21, 2019 (8.7) 
## Added
- **Help for candidates and committees**: Added a new page concerning [bank accounts of separate segregated funds](https://www.fec.gov/help-candidates-and-committees/registering-ssf/bank-accounts-ssf/)

## Changed
- **Help for candidates and committees**: Redirected older links for outdated publications and outreach files to current information on fec.gov.

## Under the hood
- Excluded Schedule L from cycle totals calculation
- Fixed CRLF injection with urllib3 package in openFEC repository
- Fixed security vulnerability with webargs by updating version to 5.1.3 (fec-eregs)
- Fixed Privilege Escalation security vulnerability for mysql:mysql-connector-java in `build.gradle` (openFEC)
- Fixed Integer Overflow security vulnerability for com.google.protobuf:protobuf-java in `build.gradle` (openFEC)
- Fixed `transaction_id` bug where type incorrectly specified as `Integer`
- Fixed `parse_fulltext()` function for user-provided search strings in full text fields


# May 07, 2019 (8.6) 
## Added
-**Campaign finance data:** A classic.fec.gov page showing how to [download and use .fec files](https://www.fec.gov/introduction-campaign-finance/data-tutorials/) is now housed on fec.gov

## Fixed
- **Campaign finance data:** Fixed loan incurred date filter
- **General:** Breadcrumbs for each section are now consistently color-coded

## Under the hood
- Fixed email filter of endpoint, /rad_analyst/ 
- Fixed /schedules/schedule_d/{sub_id}/
- Fixed /schedules/schedule_c/{sub_id}/

# April 23, 2019 (8.5) 
## Added
- **Campaign finance data:** Added new pages to explain the [presidential map](https://www.fec.gov/campaign-finance-data/presidential-map-help/) and the [House and Senate map](https://www.fec.gov/campaign-finance-data/house-and-senate-map-help/)
- **Campaign finance data:** Added new page to house [presidential financial summaries](https://www.fec.gov/campaign-finance-data/presidential-campaign-finance-summaries/) table previously on classic site. 
## Changed
- **Legal resources:** Redirected outdated links for explanations and justifications to the current [chronological index](https://www.fec.gov/legal-resources/regulations/explanations-and-justifications/chronological-index-e-j-s/) on fec.gov 
- **Help for candidates and committees:** Added language regarding specific requirements for [paper filers](https://www.fec.gov/help-candidates-and-committees/filing-reports/paper-filing/) to the paper filing page. 
- **Help for candidates and committees:** Added links to explain types of PACs to the contribution limits chart snippet embedded on several pages in this section.
- **Help for candidates and committees:** Updated footer to include Protected Voices link

## Fixed
- **Campaign finance data:**  Fixed incorrect totals on committee profile page 
- **Campaign finance data:** Fixed candidate and committee master files link
- **Help for candidates and committees:** Fixed non-filer publications filter under Latest updates section


## Under the hood
- Laid the groundwork for upcoming features (widgets functionality, fonts)
- Upgraded Django to v1.11.20

# March 26, 2019 (8.3) 
## Changed
- **Campaign finance data:** Updated raising and spending by the numbers pages to provide totals based on a candidate's election year
- **Help for candidates and committees:** Redirected older links to compliance pages, coordinated party expenditure limits and inflation adjustment Federal Register notice to their current homes on FEC.gov
- **Campaign finance data:** Refactored candidate: /candidates/totals/by_office/ endpoint to provide filter for active/inactive candidates
## Fixed
- **Help for candidates and committees:** Added a missing notation regarding combined party limits and a link to a page explaining more about the combined limit to the contribution limits chart
- **Help for candidates and committees:** Corrected a redirect to the forms

## Under the hood
- Added additional caching to the API during peak hours
- Upgraded from cflinuxfs2 to cflinuxfs3 for all 4 applications: CMS, OpenFEC, Eregs, and pattern library
- Added ability to temporarily block IPs from API
- Upgraded CMS Node to 10.15.1
- Migrated unit tests from PhantomJS to Puppeteer
- Upgrade SQLAlchemy to 1.3.1
- Upgrade redis to 13.2.0

# March 12, 2019 (8.2) 
## Added
- **Legal resources:** Updated the [legislation page](https://www.fec.gov/legal-resources/legislation/) with new legislation, signed into law in December, that extended the Commission’s administrative fine program
- **Campaign finance data:** Added 2019-2020 bulk data sets to candidates, committees, filings, raising and spending related pages
- **Campaign finance data:** Added candidate: /candidates/totals/by_office/ endpoint for calculating aggregated data for each office


## Changed
- **Legal resources:** Placed updated campaign finance statute files on the [statute page](https://www.fec.gov/data/legal/statutes/). Posted the agency’s 2019 compilation of federal election campaign laws. Added links to Title 52 and Title 26 of U.S.C. on GPO's website.
- **Help for candidates and committees:** Redirected older links for various Commission forms and transition pages to current materials. Older pages that already had been redirected to their new homes were removed classic and transition

## Fixed
- **Campaign finance data:** Fixed ability for user to filter filing dates by a single day
- **Campaign finance data:** Fixed operating expenditures line item within candidate financial summary
- **Campaign finance data:** Fixed pagination for raising and spending by the numbers pages
- **Campaign finance data:** Fixed reporting deadline links for Election profile pages


## Under the hood
- Upgraded OS stack to cflinuxfs3
- Increased API and proxy timeouts
- Added active candidates filter capability to /candidates/totals API endpoint 
- Fixed /elections API endpoint to exclude inactive candidates
- Added new endpoint /candidates/totals/by_office/ to calculate candidate totals by office
- Updated legal informational banners to link to HTTPS for the following classic legal applications: SAOS, SERS, SAOS

# February 14, 2019 (8.1) 
## Added

- **Help for candidates and committees**: Added 2019 due dates and filing information to [Dates and deadlines]([https://www.fec.gov/help-candidates-and-committees/dates-and-deadlines) 
- **Help for candidates and committees**: Added a new guide and reporting examples for “Other filers” (those who file Forms 5, 7 or 9)
- **Help for candidates and committees**: Added new pages and new reporting examples on making independent expenditures to the guides for PACs and corporations and labor organizations. 
## Changed
- **About the FEC**:  Updated references to the Chair and Vice Chairman for 2019 
- **Help for candidates and committees**: Update pages with the new contribution limits for 2019-2020 and coordinated party expenditure limits for 2019.
- **Help for candidates and committees:** Replaced the current page on making electioneering communications in the section for corporations and labor organizations with a new [page]( https://www.fec.gov/help-candidates-and-committees/other-filers/making-electioneering-communications/) applicable to all Form 9 filers.
- **Legal resources**:  Updated the [regulations page](https://www.fec.gov/legal-resources/regulations/) and the page on calculating [administrative fines](https://www.fec.gov/legal-resources/enforcement/administrative-fines/calculating-administrative-fines/) with the 2019 civil penalties as adjusted for inflation.
## Fixed
- **Campaign Finance Data**: Amounts are now displayed correctly on the raising and spending sections for a given PAC or Party committee.
- **Campaign Finance Data**: Fixed future cycle totals to display correctly for the entire election year
- **Campaign Finance Data**: Fixed tooltips to display text within the box on maps
- **Campaign Finance Data**: Fixed the ability to navigate back and forth between the raising and spending breakdown charts and candidate profile pages without losing the context on the chart page
- **Legal Resources**: Fixed MUR number search on enforcement search


## Under the hood
- Dropped unused sched c d e f tables and related process
- Updated candidate links for election profile pages to link to corresponding election year from page context
- Remove the `mur_` filters from the API

# December 04, 2018 (7.6)
## Added
- **Campaign Finance Data:**  : Added report beginning image number column to the committee filings datatable
- **Campaign Finance Data:**  : Added more searchable fields to filings/operations-log endpoint
- **General:** Added data.json file to add FEC’s API to data.gov 
## Changed
- **Help for candidates and committees:** Redirects were deployed for some older fec.gov pages to help uses find more current versions in Help for candidates and committees.
- **About the FEC:** Redirects for some older fec.gov hearing pages were deployed to help users find more current versions listed on the public hearing pages. 
- **About the FEC:** A link to the SERS database and some introductory language was added to the [public hearings](https://www.fec.gov/meetings/?tab=hearings) section of the meetings page to direct users to older archived rulemaking hearings
## Fixed
- **Homepage:** Fixed non-filer publications filter for press releases
## Under the hood
- Added robots.txt to prevent search engines from indexing pages in development and staging environments
- Implemented bastion host
- Upgraded requests and django-storages packages to fix security vulnerabilities
- Automated Elasticsearch backup process, added management tasks to create/restore backups 

# November 20, 2018 (7.5)
## Added
- **Campaign Finance Data**:  Disbursements aggregate data of memoed items are available (by API only)
- **Help for candidates and committees:**  Added “Disclosure Date” (of electioneering communications) to the glossary 
## Changed
- **Help for candidates and committees:** www redirects for some older fec.gov pages
## Under the hood
- Added new column “count” to two endpoints: sched-a/by_size/by_candidate and sched-a/by_state/by_candidate
# November 6, 2018 (7.4)
## Added
- **Campaign Finance Data:** Added host committee (Form 4) subtotals to committee profile pages 
- **Campaign Finance Data**: Added spender committee type filter on disbursement data table page
- **General:** [Election Day information](https://www.fec.gov/introduction-campaign-finance/election-day-information/)
## Changed
- **Campaign Finance Data:** Provide exact data table row counts when total is under 500,000. Provide approximate data table row counts, rounded to the nearest thousand, when total is over 500,000 
## Under the hood
- Removed unused /committees/totals/ endpoint from API
- Added automated test coverage for committee profile pages
- Added spender committee type filter on disbursement page to Schedule B in API
- Removed Elasticsearch 2.4 from eRegs app

# October 23, 2018 (7.3)
## Added

- **Legal Resources:** Updated the [Legislation page](https://www.fec.gov/legal-resources/legislation/) with newly passed legislation (H.R. 5895) changing the point of entry for Senate committees. Links and information regarding older legislation were updated as well.

## Changed
- **Campaign finance data:** Updated election search page to make it easier for users to see the results and to find upcoming presidential election data
- **Campaign finance data::** Added financial summaries for Inaugural and Host committees

## Fixed
- **Campaign finance data:** Fixed data table counts and added counts back to data table results 
- **General:** Fixed the breadcrumb links for the [FEC Record](https://www.fec.gov/updates/?update_type=fec-record) subjects

## Under the hood
- Upgraded Django and related packages to version 1.11.15 for security patch
- Upgraded Flask and Flask-related packages to the newest version for security patch and system stability:
    - Flask==1.0.2
    - Flask-Cors==3.0.6
    - Flask-Script==2.0.6
    - Flask-RESTful==0.3.6


# October 9, 2018 (7.2)
## Added
- **API:** Added legal resources to [API docs](api.open.fec.gov)
- **About the FEC:** Added two 2009 policy [hearings](https://www.fec.gov/meetings/?tab=hearings) 

## Changed
- **Help for candidates and committees:** Legacy “Quick Answers” pages regarding filing and candidates are redirected to Help for candidates and committees.

## Fixed
- **Campaign finance data:**  Fixed bug with Forms 1, 2, and 1M causing more than one to be marked “Most recent”
- **Campaign finance data:** Candidate Filings tab: Corrected issues with table display  at medium and small device/screen sizes 
- **Campaign finance data:** Candidate profile page: Candidate compare buttons now link to the correct election year based on candidate

## Under the hood
- Added recaptcha to feedback drawer in order to improve form security
- Deleted ofec_entity_chart_mv which is no longer used by any API endpoint

# September 25, 2018 (7.1)
## Added
- **Campaign finance data:** Added candidate office sought, party, state and district filters to independent expenditure data table
- **Legal API:** Added Administrative Fine and Alternative Dispute Resolution cases to legal API endpoint

## Changed

- **Help for candidates and committees:** Changed the trainings link in the drop down menu and the “Education and outreach” link on the Help for candidates and committees [landing page](https://www.fec.gov/help-candidates-and-committees/) to point to the new trainings page.
- **Help for candidates and committees:** Modified various pages and form instructions to remove references to the Secretary of the Senate, in response to the change in the law effective September 21 regarding e-filing and point of entry for Senate candidates and committees.

## Under the hood
- Switched to automated database migrations for all automated tests, rather than hard-coded database schema
- Added feature flag capability to data app section and line chart feature
- Temporarily removed datatable counts until misleading estimates can be resolved
- Removed hardcoded Press landing page contact information

# September 11, 2018 
## Added
- **Help for candidates and committees:** Added new resource [page](https://www.fec.gov/help-candidates-and-committees/trainings/) for FEC conferences, webinars and other training and appearance opportunities
- **API:** Added  filters to /committees/ endpoint so that committee search results can be filtered by most recently updated committee information
- **API:**  Added filter to /rad-analyst/ endpoint so that RAD analyst search results can be filtered by most recently changed analyst assignment information

## Fixed
- **Legal resources:** Fixed bug causing audit subcategory filters not to populate properly 
- **Legal resources:** Fixed broken statutory citation search for Advisory Opinions

## Under the hood
- Updated fec-cms project to use pytest testing framework
- Updated API pytest version to 3.7.4
- Added automated tests for candidate profile pages
- Added automated tests for legal search
- Re-enabled a validator for some API endpoints that requires a sort field to be an index on the underlying data table
- Fixed same name replacement file deletion in Wagtail CMS

# August 14, 2018 (Penny Robinson/6.5) 
## Added
- **Campaign finance data:** Added “other” to schedule A by state aggregates to show non-US states
-  **Campaign finance data:** Added important 2018 Pennsylvania redistricting information to the election search and Pennsylvania house election pages
- **Campaign finance data:** Added transaction-level coverage dates on candidate and committee profile pages.
- **Campaign finance data:** Added the ability to search for receipts from entities with foreign addresses
- **API:** Added transaction coverage date to /candidate/ID/totals
- **API:** Added transaction coverage date to committee/ID/totals endpoints

## Changed
- **Help with candidates and committees:** Modified the page on [electioneering communications](https://www.fec.gov/help-candidates-and-committees/making-disbursements-ssf-or-connected-organization/making-electioneering-communications/) to better indicate that these rules also apply to individuals and other entities as well as corporations and labor organizations.
## Fixed
- **Campaign finance data:** Fixed redirects from legacy election page tabs to new corresponding datatable anchors
- **Campaign finance data:** Fixed incorrect committee summary data description link on Advanced data committees tab
## Under the hood
- Upgraded to Wagtail 2.0. This includes major updates to the CMS editor interface which now utilizes Draftail. In addition, 2 new features were added to the editor: glossary term button and anchor button.
- Created public.ofec_sched_a_agg_state_vw to to group by all non-US state to “Other”,Modify ScheduleAByStateView to return “other” row.
- Upgraded to Django 1.11.13 in the CMS repo
- Upgraded cg-django-uaa python package to version 1.2.0
- Removed unused bandit python package
- Replaced vulnerable bleach npm package with the sanitize-html package
- Replaced vulnerable underscore.string.js npm package with the sprintf-js package
- React code within Draftail now utilizes webpack to transpile custom js.
- Added the ability to deploy the API without running migrations
- Added endpoint-specific caching to the API


# July 31, 2018 (Maj. Don West/6.4)
## Added
- **Help for candidates and committees:** Added new pages for candidates on [using personal funds](https://www.fec.gov/help-candidates-and-committees/candidate-taking-receipts/using-personal-funds-candidate/), [understanding independent expenditures](https://www.fec.gov/help-candidates-and-committees/candidate-taking-receipts/understanding-independent-expenditures/) and [joint fundraising](https://www.fec.gov/help-candidates-and-committees/making-disbursements/joint-fundraising-candidates-political-committees/)
- **Campaign finance data:** Enabled candidate financial totals export feature on elections page

## Changed
- **Legal resources:** Updated [PDF](https://www.fec.gov/resources/cms-content/documents/feca.pdf) of [statute](https://www.fec.gov/data/legal/statutes/) in CMS
- **Help for candidates and committees:** Reorganized the [receipts](https://www.fec.gov/help-candidates-and-committees/candidate-taking-receipts/) and [disbursements](https://www.fec.gov/help-candidates-and-committees/making-disbursements/) pages for candidates to aid readability and fill in gaps in information, including moving some current pages to a new section on [outside spending](https://www.fec.gov/help-candidates-and-committees/candidate-taking-receipts/#outside-spending)

## Fixed
- **Legal Resources:** Improved parsing of AO statutory and regulatory citations to recognize citations listed in a series (ex. “52 USC 30101, 30133” and “11 CFR 110.1 and 112.4”)
- **Legal Resources:** Added missing multi-part PDFs to nine archived MURs
- **Campaign finance data:** RQ-4 RFAIs now display in the 24- and 48-hour reports section of committee filings page

## Under the hood
- Refactored elections (ElectionView) endpoint to handle download function
- Improved meeting page template to accommodate regulatory hearings and include audio and video links


# July 17, 2018 (Judy Robinson/6.3)
## Added
- **Legal resources:** Embedded search boxes on the Enforcement and Audit report landing pages to help users search for relevant audit reports
- **Campaign finance data:** Added historical statistics link to campaign finance data submenu
- **General:** Added pre-release testing procedures documentation
- **API:** Added new operations log endpoint to the API (/filings/ section)


## Changed
- **Campaign finance data:** Updated default presidential year to 2020

## Fixed
- **Campaign finance data:** Added totals for [senate](https://www.fec.gov/data/candidates/senate/) and [presidential](https://www.fec.gov/data/candidates/president/) candidates running in future election years
- **Campaign finance data:** Added RFAI request types RQ2 and RQ4 to the 24/48 hour reports table of the committee filings tab
- **Campaign finance data:** Removed unused mid-year and year-end filter options from calendar
- **Legal resources:** Restored legal citation blocks to AO canonical page
- **Legal resources:** Added “About” menu and glossary to regulations search

# July 5, 2018 (The Robot/6.2)

## Added
- **Legal resources:**  Added Joint Fundraising Committee filter to audit search

## Fixed
- **Campaign finance data:** Removed joint fundraising activity from the “elections” endpoint to avoid returning inflated candidate financial results 
- **General:** Restored icons and styling missing on megamenu while visiting datatables or calendar.

## Under the hood
-  **Legal resources:** Implemented process to load advisory opinion (AO) data daily when there are changes to AO data and to reload all AOs on Sunday
- **API:** Updated Flyway to version 5.1.3

# June 26, 2018

## Added
- **General:** Added search box on mobile menus as well as “Explore All” links for each section, making it easier for users to find what they are looking for
- **Legal resources:** Added functionality to allow users to search for audits of joint fundraising committees

## Changed

- **Help for candidates and committees:** Updated [pages](https://www.fec.gov/help-candidates-and-committees/registering-candidate/) on appointing a treasurer, registering a candidate and registering a candidate’s committee 
- **API:** Updated the look and feel of the API page interface using Swagger 3.16.0
- **Campaign finance data:** Updated the election profile pages to make it easier for users to find different election datasets as well as linking to important report deadlines
- **About the FEC:** Updated the URL and design of the [Contact page](https://www.fec.gov/contact/) to help users find the FEC services they need 
- **Home page:** New background picture
- **Help for candidates and committees:** Brochures and forms that were outdated but still housed and linked on FEC transition site and in other places are redirected now to more current resources on the appropriate pages.

## Fixed
- **Help for candidates and committees:** Corrected link to compliance page for [PA/07](https://transition.fec.gov/info/ElectionDate/2018/PA_07.shtml) election

# June 19, 2018 (Will Robinson/6.1)
## Added
- **Campaign finance data:** Added language on our All receipts and Individual contributions data tables to help users search for occupation-specific individual contributor data prior to 2003
- **Legal resources:** Built an [audit report search](https://www.fec.gov/legal-resources/enforcement/audit-search) function to replace the search that is currently on classic.fec.gov site
- **General** Added new design and Wagtail CMS template to allow content editors to make changes to contact information
- **Help for candidates and committees:** Created a shortcut link to [candidate reporting examples](www.fec.gov/candidate-reporting-examples)

## Changed
- **General:** Updated the definitions of “independent expenditure only committee” and “Super PAC” to ensure legal accuracy and help them better correspond to each other 
- **General:** Updated the appearance of our feedback tool and added a tool to allow users to sign up for usability testing

## Fixed
- **Help for candidates and committees:** Fixed link to “Explore all compliance resources” link in the Help for candidates and committees main menu 
- **Campaign finance data:** Improved the user interface to display line-two committee addresses
- **Campaign finance data:** Fixed incorrect display of contributors for earmarked contributions on Receipts and Individual contributions datatables

## Under the hood
- Schedule A queries now use fecp-driven fec_fitem_sched_a tables for better performance and data accuracy
- PAC and party reports page now include Form 3s filed by these committees
- Added better error handling for navigating regulations

# May 29, 2018 (Sprint 5.6)
## Added
- **Campaign finance data:** Added new page explaining how to work with [downloadable data files.]( https://www.fec.gov/campaign-finance-data/working-downloadable-fec-data-files-using-ms-access/)
- **Help for candidates and committees:** Added FECFile help links to the troubleshooting section of Filing committee reports for all committee types

## Changed
- **General:** Changed main menu options to improve site navigation

## Under the hood
- Upgraded ElasticSearch
- Update sample_db SQL to include test data for all materialized views
- Created sample test data for all 52 ofec materialized views
- Updated Redis/Celery/Kombu packages for system stability
- Created a new materialized view, ofec_report_pac_party_all_mv

# May 15, 2018 (Sprint 5.5)

## Changed
- **General:** We updated our website menus to improve navigation to areas our users find most helpful

## Fixed
- **General:** We fixed the link back to FEC.gov on transition pages so that users will be returned to the main homepage
- **Campaign finance data:** Added monthly filter for [PAC and Party committee reports page](https://www.fec.gov/data/reports/pac-party/)
- **Campaign finance data:** Removed bundling reports filter from [House](https://www.fec.gov/data/reports/house-senate/), [Presidential](https://www.fec.gov/data/reports/presidential/), and [PAC and Party](https://www.fec.gov/data/reports/pac-party/) report pages
- **Campaign finance data:** [Raising](https://www.fec.gov/data/raising/) and [spending](https://www.fec.gov/data/spending/) breakdown charts now have cycles that are data-driven
- **Campaign finance data:** Fixed current version icons on advanced data report page datatables

## Under the hood
- Removed Gemnasium badge from our code repositories fec-cms, fec-eregs, openFEC, and fec-pattern-library. 
- Replaced Gemnasium by SNYK
- Schedule_b queries now use fecp-driven fec_fitem_sched_b tables for better performance and data accuracy
- Added better error handling for loading invalid or archived MUR numbers


# May 2, 2018 (Sprint 5.4)
## Added
- **Campaign finance data:** Added the ability for users to navigate to the authorized candidate’s page from the committee’s page 

## Changed
- **Campaign finance data:** Updated Pennsylvania district map on elections pages
- **Candidate and committee search:** Changed candidate/committee search results to sort by total financial activity rather than total receipts only

## Fixed
- **Advanced data pages:** Fixed House, Senate and Presidential candidate search pages to return all candidates regardless of financial activity
## Under the hood
- Updated CMS to the latest version of Python 3.6
- Refreshed MUR and AO tables in development and staging from the tables in production 
- Switched API to the campaign finance database-driven Schedule B tables
- Created itemized Schedule A tables and transferred data from our primary campaign finance database to Postgres
- Implemented and tested SNYK, a new vulnerability tracking tool 
- Optimized independent expenditure queries
- Analyzed and fixed slow running raw data queries

# April 18, 2018 (Sprint 5.3)
## Added
- **Campaign finance data:** Redesigned Advanced data section and bulk downloads page 
- **Campaign finance data:** Enabled [House](https://www.fec.gov/data/candidates/house/), [Senate](https://www.fec.gov/data/candidates/senate/) and [Presidential](https://www.fec.gov/data/candidates/president/) downloads
- **General:** Added new page on [public funding](https://www.fec.gov/introduction-campaign-finance/understanding-ways-support-federal-candidates/presidential-elections/public-funding-presidential-elections/) of presidential elections
- **General:** GovDelivery email [signup](https://www.fec.gov/updates/) is now active
- **Legal resources:** Added new SERS supplemental index [page](https://www.fec.gov/legal-resources/regulations/sers-supplemental-information/) for FEC rulemakings
- **Legal resources:** Added new page on how to file a [complaint](https://www.fec.gov/legal-resources/enforcement/complaints-process/how-to-file-complaint-with-fec/)

## Changed
- **Campaign finance data:** Changed the individual contributor, ZIP code search to match first 5 digits entered by the user
- **General:** Updated pattern library to include more comprehensive examples, including breadcrumbs, color pairing guidance and form examples 
- **General:** Careers page now querying USAJobs API hiring path 
parameter and displaying “Open to:” information for each open position 

## Fixed
- **Candidate profile pages:** Corrected contribution refunds total on candidate profile pages
- **Legal Resources:** Fixed a bug where 2 U.S.C. statutes on Advisory Opinions weren’t all properly mapping to new 52 U.S.C. statutes”
## Under the hood
- Loaded 2018 regulations into eRegs


# April 4, 2018
## Added
- **API:** Created a new endpoint for state election offices
- **Help for Candidates and Committees:** Began publishing reporting examples for Separate Segregated Funds and Nonconnected PACs
- **Latest updates:** Uploaded and linked 1975 and 1976 [issues](https://transition.fec.gov/pages/fecrecord/fecrecord.shtml) of the FEC Record that were previously unavailable
 
## Changed
- **Contact Info:** Updated all pages with FEC’s new mailing address: 1050 First Street, NE Washington, DC 20463

## Fixed
- **General:** Repaired a URL for an image link that was causing the image for commissioners without a biography photo to display as a broken link
- **General:** Updated the styling of the card components on the campaign finance data landing page to be consistent with styles elsewhere on the site, and create a more unified viewing experience
- **General:** Fixed calendar “All filing deadlines,” “All outreach” and “All legal events” button filters so that it will filter all deadlines
- **Candidate profile pages:** Fixed broken links on candidate profile page when a candidate has more than one authorized committee
- **Candidate profile pages:** Fixed display error that was causing district 10 candidates to display as district 1
- **Finance Data:** Moved quarterly Form 5 filings to the “Regularly filed reports” section instead of the “24 and 48 hour reports” section 
- **Finance data:** Fixed RFAIs so that they appear correctly on committee and candidate profile pages 
- **Finance data:** Fixed exclude filters to be able to return values that are null
- **Finance data:** Added new schedule A ZIP code filters to limit to 5 digits only
- **Legal resources:** Fixed MUR pagination error when searching by respondent
## Under the hood
- Styled a new pagination component that can be used on the site in the future, and will allow for specific page numbers to be selected from a set
- All public repositories have been transferred from the 18F github organization to the fecgov github organization. This includes: openFEC, fec-cms, fec-proxy, fec-eregs, FEC, fec-pattern-library, fec-infrastructure, fec-testing, fec-epics, and fec-transition
- Enabled Cached Calls on production. This functionality will save all API data in a S3 cached-calls folder so that it can be retrieved from S3 when the database or server is unavailable
- Manifest inheritance and the host attribute have been deprecated in Cloud Foundry. We use manifests to deploy using CircleCI. The base manifest has been removed and its contents have been merged with each of the individual space manifests (dev, stage, and prod). This change was made on each of the applications we deploy: fec-eregs, fec-proxy, fec-cms, openFEC
- Created redirect for anyone hitting https://www.fec.gov/files/bulk-downloads/ so that they will be routed to the bucket directly instead of going through the proxy. This will allow the user to download large data sets without failure
- Upgraded API(openFEC repo) to python v3.6.5
- Added five test cases for audit search endpoints
- Improved performance for automatic MUR reloading
- Improved performance for schedule A ZIP code searching by adding new indexes

# March 7, 2018
## Added
- **Finance Data**: Added the coverage end date to the source reports column on election page tables so that candidate data can more be accurately compared across the same time periods
- **API:** Added the ability to filter search results by excluding values

## Fixed
- **General**: Quarterly and monthly filing deadlines are now included on the homepage “Events and deadlines” feed
- **General:** Fixed a bug that was causing numbers for ordered lists to not display
- **General:** Fixed a styling effect on card components that was causing adjacent content to abruptly shift position on page

## Under the hood
- Modified audit search API endpoint to allow users to see results filtered by primary category and then further refine those results by subcategory
- Removed an unused function and streamlined existing API “exclude” logic
- Improved site stability by making Redis automatically attempt to reconnect when a connection is lost


# February 20, 2018
## Added
- **General:** Added an emergency banner to notify users of limited availability due to government shutdown
 
## Changed
- **Leadership and structure:**  Updated homepage and leadership pages to reflect Commissioner Goodman’s departure

## Fixed
- **Finance data:** Fixed display of odd-year special elections 
- **Finance data:** Changed state dropdowns to order alphabetically by state name instead of abbreviation
## Under the hood
- Updated eRegs to most recent version
- Fixed Elasticsearch timeout issue with reindexing legal documents, which increased performance for AOs and MURs
- Removed old aggregate tables and related database objects and tests that are no longer being used  
- Fixed multi column sort bug for openFEC API

# January 25, 2018
## Added
- **Help for candidates and committees:** New pages for corporations, labor organizations, trade associations, membership organizations and their separate segregated funds are now live. 
- **Campaign finance:** Added Types 3 and 4 Federal Election Activity (FEA) (Line 30(b)) to the filters available on the [browse disbursements](https://www.fec.gov/data/disbursements/)

## Fixed
- **Contact:** Corrected phone number in [Find your committee’s analyst](https://www.fec.gov/help-candidates-and-committees/question-rad/) message 
- **API:** Fixed /elections/search/ endpoint to return all congressional districts, so they appear correctly in the [Elections search](https://www.fec.gov/data/elections/) 
## Under the hood
- Improved backup of archived MURs for greater flexibility
- Improved monitoring of daily update processes
- Improved processing of aggregates
- Switched API to new aggregate tables
- Added and updated ZIP Codes to improve election page search

# January 17, 2018
## Added
- **API Documentation:** Added documentation for form type and report type
## Changed
- **Legal:** Updated Advisory Opinion and Matter Under Review documents to have permanent links
- **Finance data:** Updated logic to better handle Senate special elections
## Fixed
- **General:** Corrected typographical errors
## Under the hood
- Improved load testing
- Improved error handling

# January 3, 2018
## Added
- **Glossary:** Added definition of “Non-contribution account” to glossary
- **General:** Added GovDelivery envelope icon to footer
- **API:** Added Audit [endpoints](https://api.open.fec.gov/developers/) 

## Changed
- **Finance data:** Changed “election cycle” to “period” to more accurately reflect how we calculate financial summary information
- **Leadership and structure:** Updated Chair and Vice Chair of the Commission information to reflect 2018 leadership
- **API:** Changed 18F-fec@gsa.gov to APIinfo@fec.gov
## Fixed
- **Glossary:** Made typographical corrections
## Under the hood
- Fixed the AO landing page unit test case
- Removed remaining “tour” code
- Removed unused “between committees” template
- Added more automated testing scripts
- Updated minimum date in javascript tests for 2018

# December 20, 2017
## Added
- **Help for candidates and committees:** Added additional “How to report” examples focusing on [Statements of Candidacy](https://www.fec.gov/help-candidates-and-committees/filing-reports/registering-candidate/) and [Statements of Organization](https://www.fec.gov/help-candidates-and-committees/filing-reports/registering-committee/)
## Changed
- **Legal:** Redesigned the “Legal resources” [landing page](https://www.fec.gov/legal-resources/) to help users more easily find information 
- **Calendar:** Removed “all day” from calendar entry display
## Fixed
- **Finance data:** Changed the default time period to display the most recent financial data for all committee profile pages
- **Finance data:**  Corrected spelling error on search button
## Under the hood
- Added legal test (legal_test_data.py) data for all legal resources
- Added logging to the API to make debugging issues easier
- Removed icons no longer in use
- Resized a few existing icons to make them consistent with other icons
- Adjusted our icon build scripts so that icons that have been removed will no longer show up in the output files, and thus, won’t show up as options in the pattern library
- Moved legal news feed to its own template tag
- Changed the logic for determining future Senate elections to use a formula instead of a hard-coded set of dates

# December 6, 2017
## Added
- **General:** Added new glossary terms 
## Changed
- **Finance data:** So that the latest independent expenditures are shown first, the “24-Hour and 48-Hour Report” toggle option is now the default selected on page load, instead of “Regularly scheduled reports,” and the display order of the toggle now matches the default order 
[Example](https://www.fec.gov/data/independent-expenditures/)
## Fixed
- **Finance data:** Corrected a typo in the report type tooltip on the independent expenditure data table filters [Example](https://www.fec.gov/data/independent-expenditures/)
## Under the hood
- **Server logs:** Added more logging to periodic server tasks (Celery Beat) for better troubleshooting 
- **API developer interface:** Updated API developer interface (Swagger) tools
- **General:** Added security related attributes to session cookies for security/ATO compliance



# November 21, 2017
## Added
- **Help for candidates and committees:** Added additional “How to report” examples focusing on disbursements for [filing candidate reports](https://www.fec.gov/help-candidates-and-committees/filing-reports/#reporting-examples). Other types of reporting examples will be coming soon

## Changed
- **Database:** modified sql script to correct value used to determine if a candidate is active in a particular election
- **Elections data:** Replaced hard-coded Senate special election years with data-driven lookup so that future Senate specials will automatically appear in the dropdowns. [Example](http://www.fec.gov/data/elections/senate/AL/2018/)
- **Help for candidates and committees:** Moved [Campaign Guides](https://www.fec.gov/help-candidates-and-committees/guides/) to improve the pathways users take to find relevant guidance within “Help for candidates and committees” and so it’s easier to find all information from a stable URL
- **Help for candidates and committees:** Redesigned the "Help for candidates and committees" [landing page](https://www.fec.gov/help-candidates-and-committees/) to accommodate moving the Campaign Guides to their own section and to surface more commonly used information from within “Help for candidates and committees”
- **General:** Converted the “Introduction to campaign finance and elections” section on the homepage into a more concise and visual layout
- **General:** Created reusable pattern to add responsive images to the site with cross-browser/device support. Currently being used on new “Help for Candidates and Committees” landing page and the new “Introduction to campaign finance and elections” section of the homepage

## Fixed
- **General:** Fixed a broken link to the [Open FEC API](https://api.open.fec.gov/) in the website footer
- **General:** Added a missing space between the amendment status and the notice title on the “Commission meeting” feed
- **General:** Corrected time zone issue, allowing editors to control go-live/expiry date and time for banner announcement
- **Legal:** Fixed parsing of AOs to better detect statutory and regulatory citations [Example](https://www.fec.gov/data/legal/advisory-opinions/2016-24/)  


## Under the hood
- Updated link in API readme
- Resolved performance monitor errors related to time zones
- CSRF(cross-site request forgery) tokens are now marked as secure


# November 9, 2017

## Added
- **API:** Added advisory opinion “status” field to API indicating whether an advisory opinion is pending, withdrawn or final
## Changed
- **Finance data:** Committee profile pages now display political party in the “About the committee” section of the page 

## Fixed
- **Elections:** Updated Senate classes and upcoming election years with correct information
- **Finance data:** The “Filings” section on committee pages now displays the most recent raw eFilings, where before, no data was displaying 
- **Finance data:** Corrected an error that displayed the wrong data column for operating expenditures reported on Form 3X
- **Legal:** Fixed Archived MUR URL issue that caused MURs to display with an error 
- **Legal:** Repaired broken “Explore all advisory opinions” link from the button on the Advisory Opinions landing page 
- **Legal:** Removed the incorrect `/data` entity from the breadcrumb path for current and archived MUR pages 
- **Legal:** Fixed a bug in the logic that was causing some withdrawn advisory opinion requests to not display “Withdrawn” in the date issued column

## Under the hood
- Improved daily data transfer process
- Improved and updated continuous integration

# October 26, 2017

## Added
- **General**: Added new glossary terms
- **General**: Added “Contact” link in the About menu
- **Help for candidates and committees**: Created new “How to report” examples for [filing candidate reports](https://www.fec.gov/help-candidates-and-committees/filing-reports/#reporting-examples). Other types of reporting examples will be coming soon
- **Help for candidates and committees**: Added a [tool](https://www.fec.gov/help-candidates-and-committees/question-rad/) that allows authorized representatives to find and email their committee’s analyst. The tool provides an explanation for committees that are not yet assigned an analyst
- **Legal**: Added advanced Boolean search logic to the advisory opinion and MUR search systems  [Global legal search](https://www.fec.gov/legal-resources/), [MUR search](https://www.fec.gov/data/legal/search/enforcement/), [AO search](https://www.fec.gov/data/legal/search/advisory_opinions/)
- **API**: Added additional fields and filters to /totals/{committee-type} endpoint
## Changed
- **General**: Citations in glossary terms now link to source documents
- **General**: Removed the new site announcement banner and decommissioned the site orientation feature as part of the post-transition plan 
- **Finance data**: Changed cycle breakdown to reflect current 2 year cycle, 2017-2018
- **Latest updates**: Made it easier to find the newest news and announcements by removing meetings from the [latest updates](https://www.fec.gov/updates) feed
- **Legal**: Added additional embedded search modules that allow a quick start to search by MUR number or keyword from outside of the full search page. Also added a consistent link to the full search experience
- **Legal**: Updated information on MUR and AO messages to reflect the current state of legal search tools
## Fixed
- **Meetings**: Corrected a filter that prevented all hearings from being displayed in the [hearings](https://www.fec.gov/meetings/?tab=hearings) feed
- **Meetings**: Repaired broken links to draft Commission open meeting documents
- **General**: Corrected a typo on the contact page that previously misspelled “Teletypewriter”
- **About**: Replaced a missing image for the vacant seat on the [Leadership and structure](https://www.fec.gov/about/leadership-and-structure/) page
## Under the hood
- Made our most-used table (of current contribution limits) into a widget that can be embedded into multiple pages and updated globally, reducing risk of error
- It is now possible to preview the homepage banner announcements in Wagtail before publishing them
- It is now possible to set a time for expiration of the homepage banner
- Added the ability to upload documents for Commission meeting Sunshine Act Notices directly in the Wagtail meeting page template
- We can now create custom page titles in Wagtail that allow us to organize pages within the CMS.
- Updated Wagtail application timezone to America/New_York to accommodate user-friendly scheduling of page and banner announcement expiration
- OpenFEC-web-app and fec-style repositories are now merged into fec-cms
  - openFEC-web-app unit tests migrated to fec-cms
- Updated fec-cms developer documentation to account for post merge of apps
- Migrated continuous integration build scripts from Travis and to Circle CI


# August 24, 2017

## Added
- **Finance data:** Added state, office and party filters to the filings and reports page
- **General:** “About” menu with links to “News and updates,” “Commission meetings” and more
- **General:** Added a new Commission Meetings page that includes all open meetings, hearings and executive sessions
- **General:** Added many more glossary terms

## Changed
- **Finance data:** Redesigned [Campaign Finance Data](http://fec.gov/data) page to make it possible to search for individual contributions and compare candidates running in an election right from the page
- **Finance data:** When browsing reports and filings, document titles in the table now link to the webpage version of a given report (when available)
- **Finance data:** Senate candidates page defaults to 2018
- **Finance data:** Improve design of election page for more consistent browsing experience
- **Finance data:** Better link from candidate pages to election pages
- **Finance data:** Expanded download limits to increase the number of data rows that can be downloaded at one time
- **Finance data:** Data downloads are now .CSV files rather than zip files and are much faster and more reliable
- **Legal Resources:** Updated pages to remove notice about MUR archive not being included in MUR searches
- **General:** Redesigned homepage to provide easier navigation to the most visited sections of the site. The updated homepage more clearly highlights news and announcements, and events and deadlines. 
- **General:** Better domains for documents uploaded to CMS
- **General:** Added contact information for Information Division and Electronic Filing Office

## Fixed
- **Finance data:** Fixed an issue where new termination reports were incorrectly labeled as amendments
- **Finance data:** Fixed a bug where election pages sometimes didn’t display the correct number of congressional districts


# July 14, 2017

## Added
- **Legal resources.**  Added a column for “entity type” to the entities grid on advisory opinion pages - [example](https://www.fec.gov/data/legal/advisory-opinions/2017-04/)
- **Campaign Finance.** Added more transaction links to the candidate and the committee profile page financial summaries so that users can view the transactions that were itemized for each subtotal - [example](https://www.fec.gov/data/candidate/H8GA06195/)

## Changed
- **Legal resources.** Removed Amazon (AWS) URLs and replaced with fec.gov  URLs for legal documents - [example](https://www.fec.gov/files/legal/aos/83272.pdf)

## Fixed
- **Finance data:** Fixed an issue where F3X loan repayments were incorrect in financial summaries on the committee profile pages.


# July 3, 2017

## Added
- **Help for candidates and committees:** Added new guidance content for non-connected PACs.
- **Finance data:** Added the ability to enter an image number to pull up a specific page of a filing to the main search field on [fec.gov/data](https://fec.gov/data) (addresses [#4275](https://github.com/18f/fec/issues/4275)).
- - **Finance data:** Added the ability to filter by [receipt type](https://fec.gov/data/receipts) and [disbursement type](https://fec.gov/data/disbursements) (i.e. form line numbers) (addresses [#548](https://github.com/18f/fec/issues/548), [#3925](https://github.com/18f/fec/issues/3925) [#592](https://github.com/18f/fec/issues/592) and  [#4189](https://github.com/18f/fec/issues/4189)).
- **Finance data:** Added the ability to [filter receipts](https://fec.gov/data/receipts) by ZIP code of the contributor  (addresses [#437](https://github.com/18f/fec/issues/437) and [#4247](https://github.com/18f/fec/issues/4247)).
- **Finance data:** Added the ability to [view reports](https://fec.gov/data/filings) as HTML web pages (addresses [#4191](https://github.com/18f/fec/issues/4191) , [#138](https://github.com/18f/fec/issues/138) , and [#4129](https://github.com/18f/fec/issues/4129)).
- **Legal resources:** Added the ability to filter [Matters Under Review](http://fec.gov/data/legal/search/enforcement) by MUR number and respondent name.
- **Legal resources:** PDFs for legal resource documents now have nice fec.gov URLs instead of a long string of random characters.
- **Latest updates:** Added [historic Sunshine Act notices](https://fec.gov/updates/?&category=E&update_type=meetings) for executive sessions before 2017.
- **General:** Added permanent redirect for beta.fec.gov domain to www.fec.gov domain (addresses [#1067](https://github.com/18f/fec/issues/1067)).

## Changed
- **Legal resources:** When [browsing AOs](https://fec.gov/data/legal/search/advisory-opinions), search results are now shown as tags above the results.
- **Finance data:** When toggling between processed and raw data, any applied filters are retained.
- **Finance data:** When [searching elections](https://fec.gov/data/elections), the district map will only show up for the current election cycle, and the districts have been updated with the latest redistricting maps. (addresses [#4139](https://github.com/18f/fec/issues/4139) and [#4136](https://github.com/18f/fec/issues/4136))
- **Finance data:** Added a column for “Beginning image number” to the main [filings data table](https://fec.gov/data/filings)
- **Finance data:** Added coverage dates to the reports tables on committee pages (Addresses [#3943](https://github.com/18f/fec/issues/3943))
- **Finance data:** RFAIs now show “Not applicable” in the version columns (Addresses [#3942](https://github.com/18f/fec/issues/3942))
- **General:** When browsing *Help for candidates and committees*, *Latest updates*, and other sections, PDFs will now open in the browser by default

## Fixed
- **Finance data:** Improved the quality and consistency of schedule A, B and E data
	- Amended schedule A and B transactions will replace previous versions so older ones will longer be included in results (Addresses [#2481](https://github.com/18f/fec/issues/2481) and [#4266](https://github.com/18f/fec/issues/4266))
- **Finance data:** Fixed an issue where candidate or committee names that matched a search term wouldn’t show up in the typeahead suggestions
- **Finance data:** Fixed an issue where form 5 and form 24 data was missing from [independent expenditures](https://fec.gov/data/independent-expenditures)
- **Finance data:** Fixed an issue where filings before 2015 would occasionally have negative page numbers (addresses [#4202](https://github.com/18f/fec/issues/4202) and [#4232](https://github.com/18f/fec/issues/4232))
- **Finance data:** Fixed an issue where a special election candidate had inflated total receipts numbers ([#4236](https://github.com/18f/fec/issues/4236) and [#4290](https://github.com/18f/fec/issues/4290))
- **Legal resources:** Fixed character encoding on legal resource data that was causing unusual characters to show up in text (Addresses [#4262](https://github.com/18f/fec/issues/4262))
- **Latest updates:** Fixed an issue where searching for [latest updates](https://fec.gov/updates) by text wouldn’t return the proper results


# June 14, 2017

## Added
- **Help for candidates and committees:** Added new guidance content for [political party committees](https://www.fec.gov/help-candidates-and-committees/)
- **Finance data:** Raw electronic filings submitted within the last two days will now be shown on the “Filings” tab of a committee’s page in order to give users the most up-to-date information. (In response to https://github.com/18F/FEC/issues/4211)
- **Finance data:** Added the total amount of independent expenditures for and against a candidate, the total amount of communication costs for and against a candidate, and the total amount of electioneering communications that mention a candidate to the candidate profile pages
- **Legal resource:** Added a field to enter an advisory opinion number directly on the [advisory opinion landing page](https://www.fec.gov/data/legal/advisory-opinions/)

## Changed
- **Finance data:** Updated candidate and committee pages for greater consistency and organization:
	- The “Individual contributions” tab is now “Raising” and includes the amount of total receipts as well as breakdowns of individual contributions.
	- The “Disbursements” is now the “Spending” tab and includes the total amount of disbursements made by the committee as well as the previous breakdowns and subtotals. In the case of relevant committees, “Independent expenditures”, “Electioneering communication” and “Communication costs” are now included on the “Spending” tab rather than their own tabs, in order to give a complete picture of all spending done by a committee. 
	- All transaction data table pages now show the coverage dates that the data is for.
	- By default, the “All transactions” view of individual contributions and disbursements is open first.
- **Legal resources:** When searching [advisory opinions](https://www.fec.gov/data/legal/search/advisory-opinions/?type=advisory_opinions), checking “Show only pending requests” now removes the “Final opinion” filter in order to show all pending AOs automatically
- **Legal resources:** On an individual advisory opinion page, the documents are sorted in reverse-chronological order
- **Site navigation:** Added a prominent shortcut link to *[Individual contributions](https://www.fec.gov/data/receipts/individual-contributions/)* in the Campaign finance data menu in the main site navigation in order to make it easier for people to find the page.
- **Home:** Meeting agendas are no longer included in the “What’s happening section of the home page, which were duplicating “Upcoming events”. Now, upcoming meetings will only be included in “Upcoming events”, though meeting agendas will continue to be available on Latest updates

## Fixed
- **Finance data:** Fixed an issue where certain candidate and committee financial summary figures would be incorrect
- **Finance data:** Fixed an issue where coverage dates on candidate and committee financial summaries would be wrong or missing
- **Finance data:** Fixed an issue where candidates running in 2017 did not show up in the [top raising and spending lists](https://fec.gov/data)
- Fixed links on *[Advanced data](https://fec.gov/data/advanced)* that were targeting earlier pages from betaFEC that longer exist


# June 1, 2017

## Added
- **Finance data:** Authorized committee pages now show the district, state and political party of their related candidate. (In response to [#4118](https://github.com/18F/FEC/issues/4118))

## Changed
- **Finance data:** When browsing [receipts](https://fec.gov/data/receipts) and [disbursements](https://fec.gov/data/disbursements), the time period filter is now in the top, open panel for greater visibility. On receipts and [individual contributions](https://fec.gov/data/receipts/individual-contributions), the “Contributor name or ID” filter is now in the top, open panel, and on disbursements, the “Recipient name or ID” filter is in the top, open panel.
- **Finance data:** When viewing more than 100,000 records, the link to the bulk data downloads is now presented as a message next to the export button, rather than as a tooltip.
- **Legal resources:** The universal [legal resources](https://fec.gov/legal-resources/) search now searches AOs by only the name, number, summary and text within the final opinion. Tip: to pull up a specific AO by number from the universal search, enclose it in quotation marks.
- **General:** Styled the button to start the site orientation tour.

## Fixes
**Finance data:** When an export results in a 500 server error, the download will now show a message alerting the user that it failed.
**Finance data:** When clicking a number in the financial summary of an earlier time period on a candidate or committee profile page, the time period is now passed to the itemized data table.
**Finance data:** On committee profiles, the filings table headers no longer appear sortable when they’re not actually sortable. (Fixes [#4155](https://github.com/18F/FEC/issues/4155))
**Finance data:** Removed nonfunctional export buttons on the candidate profile pages for contributions by state and contributions by size.
**Finance data:** Fixed an issue where table columns would be poorly sized in Firefox and Internet Explorer. (Fixes [#4153](https://github.com/18F/FEC/issues/4153))
**Finance data:** Older filings that do not have PDFs available will no longer show an empty link to a PDF. (Fixes [#4159](https://github.com/18F/FEC/issues/4159))
**Finance data:** The top raising and spending candidates list on *[Campaign finance data](https://fec.gov/data/)* now includes candidates running for office in 2017 as well as 2018 (Fixes [#4169](https://github.com/18F/FEC/issues/4169))
**General:** Fixed the link to [classic.fec.gov](https://classic.fec.gov) on 404 pages (Fixes [#4135](https://github.com/18F/FEC/issues/4135))
**General:** Fixed an issue where certain candidates or committees would not appear as search suggestions after typing their full names.
**General:** Fixed an issue where users could enter `<script>` tags in the a typeahead-enabled input.

# May 19, 2017

## Added
- **Latest updates:** Added meeting agendas to the [latest updates](https://beta.fec.gov/updates) feed and upcoming open meetings will now show up on the “What’s happening” section of the home page
- **General:** Added new social media preview images, with unique images each for campaign finance data, legal resources and help for candidates and committees 

## Changed
- **Finance data:** When navigating to *[Browse receipts](https://beta.fec.gov/data/receipts)* the “Unique only” filter is no longer checked by default. It is also now labeled “From unique individuals only” and is now inside the “Contributor information” panel
- **Home:** Replaced the link to the Citizen’s Guide brochure with a link to the video “A Citizen's Guide to Supporting Candidates”
- **Help:** Removed the link to *Submit a question to RAD* from the *Help for candidates and committees* menu, and added various pathways to the [general contact page](https://beta.fec.gov/contact-us) so that users can be routed to another office if it’s more appropriate.

## Fixed
- **Finance data:** Fixed a bug where the table of itemized disbursements on committee pages would include disbursements from all committees
- **General:** Added better CSS and Javascript minification for faster page load times
- **Home:** Fixed a bug where certain events would not show up on the “Upcoming events” section of the home page
- **Calendar:** Fixed a bug where the [calendar](https://beta.fec.gov/calendar) would incorrectly separate items on the same day
- **Calendar:** Fixed a bug on the [calendar](https://beta.fec.gov/calendar) where meetings with a start time but no end time would show up as “All day” events


# May 11, 2017
## Added
- **Finance data:** Added filters for state and district when [browsing House candidates](https://beta.fec.gov/data/candidates/house/) and for [state when browsing Senate candidates](https://beta.fec.gov/data/candidates/senate/?election_year=2016&cycle=2016&election_full=true)
- **Finance data:** Added filters for authorizing candidate to the [House and Senate reports page](https://beta.fec.gov/data/reports/house-senate/) and [Presidential reports page](https://beta.fec.gov/data/reports/presidential/)
- **Finance data:** Added filters for committee type to the [House and Senate reports page](https://beta.fec.gov/data/reports/house-senate/) and [PAC and party reports page](https://beta.fec.gov/data/reports/pac-party/)
- **Calendar:** Added filters [on the calendar](https://beta.fec.gov/calendar/) for Mid-Year and Year-End reporting deadlines
- **General:** Added links in the footer to the [FOIA page](https://beta.fec.gov/freedom-information-act/) and the [page of strategy, budget and performance reports](https://beta.fec.gov/about/reports-about-fec/strategy-budget-and-performance/)

## Changed
- **Finance data:** Changed the messages that display when no data is available for a particular candidate or committee in order to be more descriptive and explain why there may be no data
- **Finance data:** Removed the reaction boxes from under the charts on [beta.fec.gov/data](https://beta.fec.gov/data).
- **Finance data:** Changed the behavior of the election year filter when [browsing candidates](https://beta.fec.gov/data/candidates) so that it filters by the year the candidate filed to run for office, rather than the years in which the candidate’s committee has activity
- **Legal resources:** Changed advisory opinion documents without dates to show “Not dated” rather than “01/01/1900”
- **Legal resources:** The [advisory opinion search](https://beta.fec.gov/data/legal/search/advisory-opinions/) now shows a loading state when it’s loading data
- **Legal resources:** When searching across [legal resources](https://beta.fec.gov/data/legal/search), the results are now presented in the order that matches the order on the legal resources landing page
- **Home:** Changed the “Upcoming deadlines” card on the Help for candidates and committees section of the home page to link to the calendar, rather than show a deadline

## Fixed
- **Finance data:** When viewing data for previous cycles on a candidate page, the links to browse receipts and disbursements now retain the time period filter
- **Finance data:** When toggling time periods on the financial summary tab of a candidate page and then navigating to another tab, the time period now correctly populates the data on the other tables
- **Finance data:** When viewing a 4 or 6 year cycle on a candidate page, the coverage dates now accurately show the entire range
- **Finance data:** When viewing a 4 or 6 year cycle for a candidate running in a future election, the financial summary now displays data correctly
- **Finance data:** When viewing candidates running in odd-year special elections, itemized data now works correctly
- **Home:** Fixed a bug that prevented pinned items from showing up on the What’s happening feed
- **Home:** Fixed the links to YouTube videos for the *Help for candidates and committees* tabs


# April 28, 2017

## Added
- **General:** Added a site search that searches through candidates, committees, and other pages on the site
- **Legal resources:** Redesigned the display of [AO search results ](https://beta.fec.gov/data/legal/search/advisory-opinions/)to include more information to make it easier to find what you’re looking for
- **Legal resources:** Added the ability to [filter AOs](https://beta.fec.gov/data/legal/search/advisory-opinions/) by the name of other entities involved in an opinion, such as commenters and representatives
- **Legal resources:** Added links to the regulations and statutes that an AO cites on an AO page
- **Legal resources:** Added a table of entities involved in AOs to the AO pages, including commenters and representatives
- **Help for candidates and committees:** Added the ability for authorized representatives of committees to [look up their RAD analyst](https://beta.fec.gov/help-candidates-and-committees/question-rad)

## Changed
- **Finance data:** When searching from [beta.fec.gov/data](https://beta.fec.gov/data) , users no longer need to select “candidates” or “committees”; all results are presented together 
- **Finance data:** The [cumulative raised and spent charts](https://beta.fec.gov/data) now default to the 2017-2018 time period
- **Finance data:** Unverified filers no longer show up in the data
- **Finance data:** When [searching elections](https://beta.fec.gov/data/elections), districts with upcoming special elections now show the date of the next special election
- **Finance data:** Removed the links from “Total receipts” and “Total disbursements” in candidate and committee financial summaries
- **Finance data:** Removed the “Disbursements received from other committees” table on committee profiles and moved “Disbursements to committees” to the main “Disbursements” tab
- **Finance data:** The details panel when [browsing receipts](https://beta.fec.gov/data/receipts/) and disbursements now shows the form and line number that a receipt was reported on
- **Finance data:** Added “2017-2018” as an option for the [filings](https://beta.fec.gov/data/filings/) and [candidates](https://beta.fec.gov/data/candidates/) “Year” filters
- **Finance data:** When downloading [receipts](https://beta.fec.gov/data/receipts/), the contributor year-to-date aggregate now comes after the amount of the single transaction
- **Legal resources:** Added a more prominent link to the administrative fine calculator on the [administrative fines page](https://beta.fec.gov/legal-resources/enforcement/administrative-fines/)
- **General:** Added a link to the Inspector General page in the footer

## Fixed
- **Finance data:** Election pages for districts with special elections happening now show all candidates in the special election
- **Finance data:** The profile pages for candidates running for odd-year special elections now work
- **Finance data:** The district maps on election pages no longer overlap with the tabs
- **Finance data:** Candidate profiles now show the statements of candidacy filed for the selected election year
- **Finance data:** Fixed an issue where certain RFAIs were not properly labeled
- **Finance data:** Fixed an issue where “Total transfers” in a committee financial summary were not properly labeled
- **Legal resources:** When searching AOs, hitting “enter” in a filter field now applies the filter
- **Accessibility:** Fixed several broken ARIA labels for accessibility improvements
- **Home page:** Tips for Treasurers in the “What’s happening” section of the home page are now labeled properly
- **General:** Fixed a bug where the feedback widget would not work
- **General:** Fixed an issue where the site menu would not open in Safari


# April 14, 2017

## Added
- A new site tour that introduces users to [beta.fec.gov](https://beta.fec.gov/)
- **Legal resources**: Added links to the existing AO search and Enforcement Query System to *[Advisory Opinions](https://beta.fec.gov/data/legal/advisory-opinions)* and Enforcement search results pages
- **Legal resources**: Added pending Advisory Opinions to *[Advisory Opinions](https://beta.fec.gov/data/legal/advisory-opinions)*

## Changed
- **About**: Removed the “coming soon” button from the “Working with the FEC” section on *[About](https://beta.fec.gov/about)*

## Fixed
- Fixed an issue where the site menu wouldn’t work correctly on some mobile browsers

# April 7, 2017

## Added
- **Help for candidates and committees:** Replaced *Registration and reporting* with a new section that combines content about registration and reporting with guidance around compliance: [*Help for candidates and committees*](https://beta.fec.gov/help-candidates-and-committees/)
	- Added a section on the home page for this
- **New navigation:** A whole new site navigation menu with a simplified set of links for *Campaign finance data* and new sections for *Legal resources* and *Help for candidates* and committees
- **Legal resources:** Added the ability to [search AOs](https://beta.fec.gov/data/legal/search/advisory-opinions/) by citations
- **Legal resources:** New pages for [*Enforcement matters*](https://beta.fec.gov/legal-resources/enforcement/), [*Alternative Dispute Resolution*](https://beta.fec.gov/legal-resources/enforcement/alternative-dispute-resolution/) and [*Administrative fines*](https://beta.fec.gov/legal-resources/enforcement/administrative-fines/)
- **Campaign finance data:** Redesigned candidate pages to give complete financial summary information and more detailed data about raising and spending
- **Campaign finance data:** Redesigned the [*Advanced data*](https://beta.fec.gov/data/advanced) page and added links to legacy data pages=
- **Campaign finance data:** Added the ability to view financial totals for previous years on the [cumulative raising](https://beta.fec.gov/data#raising) and spending charts 
- **Campaign finance data:** Added filters for beginning image number on [*Filings*](https://beta.fec.gov/data/filings) and image number on [*Receipts*](https://beta.fec.gov/data/receipts) and [*Disbursements*](https://beta.fec.gov/data/disbursements)
- **About the FEC:** Added a new section for [*Reports about the FEC*](https://beta.fec.gov/about/reports-about-fec/)
- **General:** Added more links to the site footer

## Changed
- **Legal resources:** Changed the SERS description on [*Regulations*](https://beta.fec.gov/legal-resources/regulations)
- **Legal resources:** When searching [*Legal resources*](https://beta.fec.gov/legal-resources/) MURs now display in reverse chronological order, and regulations and statutes by title, chapter and subchapter
- **Campaign finance data**: Added missing fields to committee financial summaries, including beginning cash on hand, ending cash on hand and debts/loans owed to committee
- **Campaign finance data**: Added links from financial summaries to itemized transactions for certain subtotals
- **Campaign finance data**: Added itemized individual contributions and disbursements to committee pages

## Fixed
- Fixed an issue where “offsets to operating expenditures” on committee pages showed the wrong data
- Fixed an issue where certain candidates didn’t show up in search ([Issue #2210](https://github.com/18F/openFEC/issues/2210))
- Fixed a bug where links to committee pages would be broken ([Issue #1852](https://github.com/18F/openFEC-web-app/issues/1852))


# March 23, 2017
## Added
- Legal resources: Added several new pages to the Legal resources section, including
	- **[Regulations](https://beta.fec.gov/legal-resources/regulations)**, which links to various versions of 11 CFR, the existing SERS system, and public hearings
	- **[E&Js](https://beta.fec.gov/legal-resources/regulations/explanations-and-justifications/)**, with information about explanations and justifications for regulations
	- Court cases
	- **[Legislation](https://beta.fec.gov/legal-resources/legislation)**, with information about the history of campaign finance legislation

## Changed
- Updated the contact information on [Contact](https://beta.fec.gov/contact-us) to include more toll-free numbers and a general info@fec.gov email address	


# March 10, 2017

## Added
- **Finance data:** Added amendment status and version information to reports pages ([for example](https://beta.fec.gov/data/reports/presidential/?data_type=processed))
- **Finance data:** Added the ability to filter reports by their version and document status 

## Changed
-  **Legal resources:** [Advisory Opinions](https://beta.fec.gov/data/legal/search/advisory-opinions/) are now ordered in reverse-chronological order 
- **Home page:** Redesigned the “What’s happening” section of the [home page](https://beta.fec.gov/) for greater legibility 
- **General:** Improved typography spacing and styles throughout the site

## Fixed
-  **Legal resources:** Fixed a bug where paging through Advisory Opinions would lose the search query
-  **Legal resources:** Changed Advisory Opinions so that the count accurately reflects the number of AOs in a search
- **Finance data:** Fixed a bug on the [election lookup page](https://beta.fec.gov/data/elections) where presidential election dates were incorrect

# February 16, 2017

## Added
- **Campaign finance data**: New page for [itemized loans](https://beta.fec.gov/data/loans/)
- **Campaign finance data**: New page for itemized [party coordinated expenditures](https://beta.fec.gov/data/party-coordinated-expenditures/)
- **Campaign finance data**: Added the ability to [download reports](https://beta.fec.gov/data/filings/) as valid CSV files
- **Campaign finance data**: Added report ID number (FEC-####) to the “Version” column when browsing tables of filings
- **Latest updates**: Added “FEC Record” and “Tips for Treasurers” to the [latest updates](https://beta.fec.gov/updates) feed
- **API**: Added the ability to sort the `/filings/` endpoint by multiple parameters

## Changed
- **Campaign finance data**: Redesigned the committee page based on user feedback:
	- The page has a new layout that makes more efficient use of space
	- The financial summary is now easier to read and clearly displays nested totals and subtotals 
	- The filings table now groups filings by type and presents them in reverse-chronological order 
- **Campaign finance data**: Now committee pages default to the most recent cycle for which there is a report filed 
- **Campaign finance data**: Increased the color contrast on the [total raising and spending charts](https://beta.fec.gov/data) to improve legibility

## Fixed
- **Campaign finance data**: Fixed a bug where candidates would occasionally not show up when [browsing candidates](https://beta.fec.gov/data/candidates)
- **General**: Fixed a bug where the navigation menu on the side of a page wouldn’t work in certain browsers

# February 2, 2017

## Added
- **Campaign finance data**: Improved the display when browsing [filings](https://beta.fec.gov/data/filings/) to show when a document is the latest version of a filing or when it’s out of date (because it has been amended). The table now also specifies when a filing is an original or amendment.
- **Legal resources**: Added citations to [Advisory Opinion](https://beta.fec.gov/data/legal/advisory-opinions/) pages that show which previous AOs an AO cites and which later AOs cite this AO.

## Changed
- **Campaign finance data**: Links in the main navigation to Presidential reports, House and Senate reports, and PAC and Party reports no longer automatically filter to only unamended reports

## Fixed
- **Campaign finance data**: Requests for Additional Information (RFAIs) on the [filings](https://beta.fec.gov/data/filings/) page no longer give an option to download a .fec file, as they do not exist in that file format.
- **Campaign finance data**: Fixed a bug on certain data table pages that prevented the filter panel from opening and closing.
- **Campaign finance data**: Fixed a bug on data table pages where entering a filter term with double-quotations would cause the filter to not work as expected.
- **Registration and reporting**: Fixed a bug that was causing thumbnails of committee guides to not show up correctly on certain pages.
- **Home page**: Fixed a bug where the “More about the FEC” link wouldn’t work correctly

# January 19, 2017
## Added
- **Finance data**: Added the ability to view raw data from efilings for:
	- [Itemized receipts](https://beta.fec.gov/data/receipts/?data_type=efiling) 
	- [Itemized disbursements](https://beta.fec.gov/data/disbursements/?data_type=efiling)
	- [Itemized independent expenditures](https://beta.fec.gov/data/independent-expenditures/?data_type=efiling)
- **Legal resources**: Additional advanced filters for [advisory opinions](https://beta.fec.gov/data/legal/search/advisory-opinions/)) so that users can now refine their search within certain document types, view pending AOs, and search by requestor name and requestor type
- **API**: Added endpoint for raw itemized receipts from efilings: `/schedules/schedule_a/efile/`
- **API**: Added endpoint for raw itemized disbursements from efilings: `/schedules/schedule_b/efile/`
- **API**: Added endpoint for raw independent expenditures from efilings: `/schedules/schedule_e/efile/`

## Changed
- **API**: Made under-the-hood improvements to provide users with more accurate data
- **Home**: Shortened the text on the home page hero section and added a link to “About the FEC”

## Fixed
- **Finance data**: Fixed a bug where filters appeared to be loading when first visiting a page

# January 4, 2017
## Added
- **Legal resources**: Added a new page outlining the process of filing a complaint with the FEC and how the FEC handles these complaints: [beta.fec.gov/legal-resources/enforcement/complaints-process](https://beta.fec.gov/legal-resources/enforcement/complaints-process)
- **Home page**: Added a section for “Citizen information” 
- **About the FEC**: Added a landing page for “[About the FEC](https://beta.fec.gov/about)”. Additional sections will be added in future releases.
- **API**: Added a new endpoint for raw schedule E data from efilings at: `/schedules/schedule_e/efile/`

## Changed
- **Finance data**: Improved the UX for toggling between raw and processed filings at [beta.fec.gov/data/filings](https://beta.fec.gov/data/filings):
	- Relabeled the “efiling data” to “raw data”
	- Separated the “Data type” toggle from the rest of the filters for greater clarity
	- Changing the data type now shows a message explaining the different type of data and hides all filters that are not available for the selected data type
- **Finance data**: Changed the style of sidebar links on the [Advanced Data page](https://beta.fec.gov/data/advanced) and added links to reporting requirements for different types of committees

## Fixed
- **Finance data**: Fixed an issue so that when a candidate has no financial data associated with them, their name is included in the message that’s displayed (thanks to open source contributor [@busterroni](https://github.com/busterroni) for the fix)
- **Home page**: “learn more” links now scroll the page down, rather than jumping to the section
- **Legal resources**: Fixed an issue where the candidate and committee suggestions were incorrectly showing up when searching through legal researches

# December 22, 2016
## Added
- **General**: Added a new home page organizing FEC information into three primary sections, campaign finance data, registration and reporting and legal resources.
- **Legal resources**: Added a new page explaining the [Advisory Opinion process](https://beta.fec.gov/legal/advisory-opinions/process)
- **Legal resources**: Added new filtering functionality to allow users to refine their [Advisory Opinions searches](https://beta.fec.gov/data/legal/search/advisory-opinions/) by number, name and date
- **Legal resources**: Added a list of recent Advisory Opinions to [beta.fec.gov/data/legal/advisory-opinions](https://beta.fec.gov/data/legal/advisory-opinions/)
- **API**: Added a new field to the /filings/ and /reports/ endpoints called `amendment_chain` which lists all filings in an amendment chain

## Fixed
- **Calendar**: Fixed a bug where modifying filters on the [calendar](https://beta.fec.gov/calendar/) didn’t change the URL
- **Campaign finance data**: Fixed a bug that caused incorrect numbers on the [cumulative raising and spending charts](https://beta.fec.gov/data/)

# December 7, 2016
## Campaign finance data
- Improved the underlying data quality for [beta.fec.gov/data/filings](https://beta.fec.gov/data/filings)

## Legal resources
- Added a search for [Enforcement Matters](https://beta.fec.gov/data/legal/enforcement/) that includes all Matters Under Review from 1999 and later
- Improved the flexibility of legal resource searches so that variations of searched keywords show up in results (for example, “embezzling” returns matches of “embezzle” and “embezzles”)
- Fixed an issue where the “Legal resources” item in the main navigation menu wasn’t highlighted when on these pages

## General improvements
- Made minor changes to links in header and footer menus for consistency in navigation across different aspects of the site
- Made under-the-hood improvements to the FEC content management system

# November 9, 2016

## Campaign finance data
- Updated the total raising and spending charts on [beta.fec.gov/data](https://beta.fec.gov/data) to use live data, giving users an up-to-date picture of the total amount raised and spent in federal elections
- Updated results on [beta.fec.gov/data/filings](https://beta.fec.gov/data/filings) and reports pages to show if a report was filed electronically or on paper

## Legal resources
- Updated the Legal Resources search so that document types with results are displayed above document types without results
- Improved search effectiveness (search stemming)
- Added missing “previous section” pager icon to eRegulations
Made assorted styling changes to improve readability of document templates

## Press section
- Added a new section for the FEC Press Office — [beta.fec.gov/press](https://beta.fec.gov/press) — that includes a section of resources for journalists
- Added a new Latest Updates section that includes press releases and Weekly Digests from the FEC Press Office: [beta.fec.gov/updates](https://beta.fec.gov/updates)

## API
- Added a new `means_filed` property on `/filings/` and `/reports/` responses to identify if a filing was submitted electronically or by paper
- Added a new endpoint for large cumulative finance totals by entity type at `/v1/totals/entity-receipts/` and `/v1/totals/entity-disbursements/`
- Fixed a bug that would prevent users from being able to paginate through large data sets on itemized endpoints, like the schedule A and schedule B endpoints

# October 26, 2016

## Campaign finance data
- Created new data visualizations:
	- [beta.fec.gov/data/raising](https://beta.fec.gov/data/raising) charts top raising candidates, PACs and party committees
	- [beta.fec.gov/data/spending](https://beta.fec.gov/data/spending) charts top spending candidates, PACs and party committees
- Added .fec file download capability to financial reports on:
	- [beta.fec.gov/data/filings](https://beta.fec.gov/data/filings)
	- [beta.fec.gov/data/reports/presidential](https://beta.fec.gov/data/reports/presidential)
	- [beta.fec.gov/data/reports/house-senate](https://beta.fec.gov/data/reports/house-senate)
	- [beta.fec.gov/data/reports/pac-party](https://beta.fec.gov/data/reports/pac-party)
- Added coverage period information to the financial totals listed on individual candidate pages
- Fixed a bug that caused the the tooltip on the data table export button to show up in the wrong location
- Fixed a bug that stopped the independent expenditure page from loading when the 24- and 48-hour report filter was applied
- Made under-the-hood improvements to ensure better site stability

## API
- Added URLs for .fec files for reports available at `/filings/` and all `/reports/` endpoints

## Legal resources
- Fixed searching of AOs to only search final opinion and closeout letter documents


# October 12, 2016
## Campaign finance data
- Improved the itemized independent expenditure page:
    - Made independent expenditure data more timely by improving its data source
    - Added independent expenditures from Form 5
    - Added independent expenditures from 24- and 48-hour reports
- On committee pages, added the ability to export results from receipt and disbursement tables
- On candidate, committee and election pages, added the ability to view different number of results per page on aggregate tables

## Legal resources
- We’re not shipping anything new this week but we’re hard at work on new features that are coming soon

## Styles
- Redesigned and refactored our heading template to provide a more visually consistent experience across pages


# September 28, 2016
## Campaign finance data
- Made the following items exportable:
  - Reports data pages (for example, https://beta.fec.gov/data/reports/presidential)
  - eFilings (on reports and filings pages)
- Added committee names to exported files of itemized receipts, disbursements and independent expenditures
- Enhanced summary charts on https://beta.fec.gov/data, adding data through August 31, 2016
- Improved the ending date filters so that clicking on a month now selects the last day of that month
- Fixed a bug where on small screens the filters created an extra gutter on the side of the screen

## Legal resources
- We’re not shipping anything new this week but we’re hard at work preparing more content

## Additional content
- We’re not shipping anything new this week but we’re hard at work preparing more content

## General improvements
- Fixed an issue where closing the site glossary forced the user to the top of the page
- Added a slight delay to the opening of the navigation menu, to prevent users from opening it inadvertently

## API
- Added itemized [debts](https://api.open.fec.gov/developers/#!/debts) (schedule D) at `/schedules/schedule_d/`

# September 14, 2016 release notes
## Campaign finance data
- Improved date filters to make choosing month ranges easier when filtering data
- Fixed print styles so pages are still readable when printed or saved to PDF
- Renamed “Other spending” tab on candidate and elections pages to “Spending by others to support/oppose” to increase clarity

## Legal resources
- We’re not releasing anything this week, but we’re hard at work on new features that are coming soon

## API
- Added itemized [party coordinated expenditures](https://api.open.fec.gov/developers/#!/party-coordinated_expenditures) (schedule F) at `/schedules/schedule_f/`
- Added [itemized loans](https://api.open.fec.gov/developers/#!/loans) (schedule C) at `/schedules/schedule_c/`

# August 31, 2016 release notes
## Campaign finance data
- Added new pages for browsing report summaries:
  - Presidential reports: beta.fec.gov/data/reports/presidential
  - House and Senate reports: beta.fec.gov/data/reports/house-senate
  - PAC and party committee reports: beta.fec.gov/data/reports/pac-party
- Added filters to report summary pages for filtering by total financial figures
- Added raw eFiling data to report summary pages
- Improved readability on filings page by removing columns used only for financial reports (now visible on the reports pages)
- Added new text filters to allow filtering by multiple values for the same field, such as contributor city and employer
- Added new styles for financial range filters to improve readability and usability
- Fixed a bug where unitemized contributions were being included in the totals shown for contributions from a state
- Made behind-the-scenes improvements to ensure better quality and more consistent data on the [electioneering communications data page](https://beta.fec.gov/data/electioneering-communications)
- Made several minor improvements to clean up the display of information:
	- Added “payee” to the [independent expenditures data page](https://beta.fec.gov/data/independent-expenditures)
	- Re-arranged columns on the [receipts](https://beta.fec.gov/data/receipts) and [individual contributions](https://beta.fec.gov/data/receipts/individual-contributions) pages so that contributor name is the first column
	- Removed old form types from the form type filter on the [filings data page](https://beta.fec.gov/data/filings)
	- Fixed the order of authorized committees on the candidate page header so the most recent is on top
	- Added years for future elections to election cycle filters
	- Removed the district field from Senate and presidential candidate page headers
	- Added a column to [receipts data table](https://beta.fec.gov/data/receipts) for the election type (e.g. primary vs. general)

## Legal resources
- Added the statutes administered by the FEC to universal search
- Added PDFs to full text of statutes administered by the FEC
- Improved the display of regulation search results on mobile

## Registration and reporting
- We’re not releasing anything this week, but we’re hard at work on new features that are coming soon

## API
- Added real-time [eFiling data](https://api.open.fec.gov/developers/#!/efiling) for report summaries
- Added the ability to filter report summaries by different fields


# August 17, 2016 release notes

## Campaign finance data
- Added the ability to view efiling data in real time on [beta.fec.gov/filings](https://beta.fec.gov/filings)
- Added a new visualization to [beta.fec.gov/data](https://beta.fec.gov/data) to show the cumulative amount of money raised in the election over time, improving the earlier chart by implementing a standard unit of time and improved interactivity
- Redesigned the data table filter layout to increase usability on small and large screens
- Refined loading and success states for type-ahead and dropdown filters:
  - Checkboxes from dropdowns and type-ahead filters can now be completely removed after unchecking them
  - Checkboxes from type-ahead filters now show the loading state in the correct place
- Made behind-the-scenes improvements to ensure better quality and more consistent itemized data

## Legal resources
- Added advisory opinions to universal search
- Added advisory opinion canonical pages
- Links to advisory opinion searches, canonical pages and individual documents are now permanent so can be shared directly to others.

## API
- Added real-time efiling data for filings at `/efile/filings`

# August 3, 2016 release notes

## Campaign finance data
- Enhanced the data filter interaction design in various ways:
	- Individual filters indicate when data is loading so that users better understand what the system is doing
	- Once data has been loaded, filters display a message with the number of results added or removed as a result of that filter
	- Filter accordion headers now show the number of applied filters for greater legibility
- Fixed a bug where closing the filter panel didn’t expand the data table to use the full space
- Improved mobile styles on beta.fec.gov/data
- Improved the way the filter panel on data pages works on mobile devices
- Added a link to the source filings for committee financial summaries
- Fixed a bug where candidates were loading out of order on election pages

## Registration and reporting
- Improved the design of registration essentials checklists to better communicate the hierarchical relationship of items

## Legal resources
- We’re not releasing anything this week, but we’re hard at work on new features that are coming soon

## Calendar
- Added tooltips to calendar categories to better communicate what each category represents

***

# July 27, 2016 release notes

## Campaign finance data
- Improved the data source for itemized receipt and disbursement data so that records will be updated more quickly and data will be more accurate
- Fixed a bug where tooltips on bar charts were off center
- Added the ability to filter presidential candidates by those who have received presidential public funds
- Replaced all instances where donation buckets were labeled “Under $200” with “$200 and under”
- Updated typeahead suggestions in search bars to highlight the text that matches the search term
- Rearranged the order of columns in the .csv files when downloading data to make them more readable
- Minor changes to improve accessibility of the filters
- Minor language changes to increase consistency throughout

## Registration and reporting
- Added glossary definitions for "overnight delivery service" and "postmarked"
- Refined and unified content for electronic filers and paper filers

***

# July 7, 2016 release notes

## Campaign finance data
- Increased the speed and accuracy of financial totals with under-the-hood data improvements
- Added top raising and spending candidates, PACs and party committees to beta.fec.gov/data
- Improved the design of data tables:
  - Arranged and sized columns to get a better view of the data
  - No longer truncate long text in cells
  - Right-aligned currency for easier comparison
  - Updated the visual design to make tables easier to read
- On committee pages, adjusted the the filings table to only shows the "independent expenditures" column if it's for a committee that can make independent expenditures
- On tables with mini-bars in the cells, made the scale of the bars constent across pages, rather than resetting to the max of that page
- Improved the design of the financial summary accordions on committee pages
- Added introductory text explaining what's available in each data set on beta.fec.gov/data/advanced
- Fixed a bug that casued the mobile menu to be missing items at times

## Legal resources
- Added a new, searchable section with the 2016 edition of Title 11 of the Code of Federal Regulations

## Registration and reporting
- Added registration and reporting essentials for nonconnected committees
- Linked beta.fec.gov/registration-and-reporting to calendar filing deadlines for each type of registrant

## Calendar
- Added links to the fec.gov report notices for filing deadlines

## Glossary
- Added definitions for Hybrid PACs, Leadership PACs, Lobbyist/Registrant PACs and Super PACs

## API
- Added a new endpoint to find the Reports Analysis Division analyst for a particular committee ID
- Added a new endpoint to view financial totals for all PACs: `/totals/pac`
- Added a new endpoint to view financial totals for all party committees: `/totals/party/`
- Upgraded data source for candidate and committee totals

***

# June 28, 2016 Release Notes

## Campaign finance data
- You can now download itemized receipts and disbursements
- We've added additional campaign finance summary information and transaction-level data. You'll now find receipt data prior to 2011 including contributions over $500 from 1979 to 1988, contributions over $200 from 1989 to 2005 and all receipts since 2005. You'll find spending data prior to 2011 including non-operating expenses since the late 1970s and all disbursements since 2005.
- beta.fec.gov/data now includes charts showing the total amount spent and raised by different groups in the 2016 election
- Users can register feedback for each chart on beta.fec.gov/data with a new reaction widget
- Renamed the "Committee name or ID" filter on beta.fec.gov/data/communication-costs to "Spender name or ID" for greater clarity and accuracy

## General
- Updated the home page to include current information about the latest features and what's coming soon
- We will now link release notes from the home page for each release
- Various under-the-hood changes are in effect to improve the ease of deployment

