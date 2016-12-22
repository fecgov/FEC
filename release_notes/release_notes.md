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

