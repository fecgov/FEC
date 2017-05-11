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

