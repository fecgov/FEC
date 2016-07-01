# July 7, 2016 Release Notes

## Campaign finance data
- Under-the-hood data improvements to increase the speed and accuracy of financial totals
- Added top raising and spending candidates, PACs and party committees to the beta.fec.gov/data
- Improved the design of data tables: 
  - Columns are arranged and sized to get a better view of the data
  - Cells no longer truncate long text
  - Currency is now right-aligned for easier comparison
  - Updated the visual design to make it easier to read the tables
- On committee pages, the filings table only shows the "independent expenditures" column if it's a committee that can make independent expenditures
- On tables with mini-bars in the cells, the scale of the bars now stays constent across pages, rather than resetting to the max of that page
- Improved the design of the financial summary accordions on committee pages
- Added text to beta.fec.gov/data/advanced to explain the different data sets
- Fixed a bug where the mobile menu would be missing items at times

## Legal resources
- A new, searchable legal resources section was added that includes the latest annual edition of the Code of Federal Regulations Title 11.  We are working to add Statutes and Advisory Opinions in a later release.

## Registration and reporting
- Each registrant-type row on beta.fec.gov/registration-and-reporting now includes a link to the filing deadlines for that type

## Calendar
- Filing deadlines now include links to the report notices page on fec.gov
- Links to reporting pages for reporting dates

## API
- Added a new endpoint to find the Reports and Analysis Division analyst for a particular committee ID
- Added a new endpoint to view financial totals for all PACs: `/totals/pac`
- Added a new endpoint to view financial totals for all party committees: `/totals/party/`
- Upgraded data source for candidate and committee totals
