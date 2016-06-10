# Advanced Data Tables

These tables are meant to provide expert users with the ability to browse and filter candidates, committee, receipts and disbursements, filtering by a range of dimensions. Meant for more advanced users.

![Image of data tables](assets/advanced-data-tables-key.png)

## key:

:red_circle:           | Relatively severe, insurmountable experience issue, failures endemic. Recommend that action is taken (`red_circle`)
:--------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:large_orange_diamond: | Moderate experience issue; reasons for failure or success are complicated, inconsistent and/or may be addressed by other fixes (`large_orange_diamond`)
:white_circle:         | Minor or nonexistent experience issue, or unclear finding, no action indicated (`white_circle`)
decision bullet format | `- [needs action indicator]` Problem: "Users thought this happened, or expected this, when really this" then if :red_circle: :wrench: Fix/hypothesis statement: "we think that by making this X do Y, it will improve" or if :large_orange_diamond: Why to address this later (any dependent issues or pre-fix fixes) or if :white_circle: The thing we were looking for in testing / Recap of why no action : Inconclusive test / Not enough data / Good enough!`[Assigned in GitHub issue #]` `[tested date link]` `[demo gif link]`

## Filtering and searching :two:, :five:

### Autocomplete and type-ahead

#### Tested dates, decisions, and issues

- :red_circle: PROBLEM: Once users have added filters they did not close the panel, it was not clear that the filter panel could be closed. This led users to think they had to reset the filters in order to add more. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

  - :wrench: Make sure the process(order/placement) of using filters and tags : a. Feels like it's part of the same tool, and b. reflects the process that users would go through in using it [desktop & mobile]

- :red_circle: PROBLEM: Users did not necessarily understand that the results were updating upon changing filters, as this was happening off-screen with no discernable alert.[tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

- :red_circle: PROBLEM: On desktop (as well as mobile, see above) users did not necessarily see when a small results set was shown from their position down screen. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

  - :wrench: Differentiate between results state and no-results state and an error state

- :red_circle: PROBLEM: Users interpreted the call to action on the page as export data, as it is the largest button. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

  - :wrench: In mobile: Add a reminder that results/updates are happening as filters are selected
  - :wrench: Keep the export button, but make it less sticky (a non-sticky version of the blue bar)
  - :wrench: De-emphasize the export this data button ---> as an icon, floating in the top right
  - :wrench: Make the filter panel modal take up the full screen to open & close.
  - :wrench: Make it more obvious how to get out of the filter panel and apply the filters at any point

- :large_orange_diamond: PROBLEM: Some users struggled editing pre-filled date text or text they had entered in the date fields. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

  - :wrench: Alter way for users enter information in date fields

- :white_circle: [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md), [5/26/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-26.md) users used search button, enter, and selecting an item from the pop-up to trigger search. [1594](https://github.com/18F/openFEC/issues/1594), [1652](https://github.com/18F/openFEC/issues/1652) [:tv:](assets/right_to_rise.gif)

- :large_orange_diamond: search icon may confuse, but not as much as drop down icon. [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md)

  - :wrench: filter input boxes that function differently should indicate that they do (this may be sufficiently accomplished by the presence of the free-text search prompt appearing in the contextual menu)

### Filtering

#### Tested dates, decisions, and issues

- :red_circle: many users interpreted the filters as "or" as opposed to an "and", only some of the users comprehended what was happening after the search results were shown [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md) [issue: 1653](https://github.com/18F/openFEC/issues/1653) [:tv:](assets/gates-sample.gif)
- :white_circle: sticky filter panel more likely to be seen [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md)

## Results listing :three:

### Sorting

- :large_orange_diamond: Before attempting filter tasks, many users seek to sort on name first. Seems they are using sorting as a "fuzzy" filter that lets them see things that are close to their desired term. This may be a coping mechanism for data which is inevitably imperfect. [5/12/2016] [issue: 1652](https://github.com/18F/openFEC/issues/1652)

## Keep an eye on

feature                    | note
:------------------------- | :------------------------------------------------
employer text box          | expressed desire for including multiple employers
`received from` checkboxes | default should have both checked?

## Initial directional research

to be added
