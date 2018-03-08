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

