# Advanced Data Tables

These tables are meant to provide expert users with the ability to browse and filter candidates, committee, receipts and disbursements, filtering by a range of dimensions. Meant for more advanced users.

![Image of data tables](assets/advanced-data-tables-key.png)

## key:

:red_circle:           | needs action now (`red_circle`)
:--------------------- | :-------------------------------------------------------------------------------------------------------------------------
:large_orange_diamond: | needs action later (`large_orange_diamond`)
:white_circle:         | no actions at this time (`white_circle`)
decision bullet format | `- [needs action indicator]` `[tested date link]` documented decision overview `[documented issue link]` `[demo gif link]`

## filtering and searching 2, 5

### autocomplete & type-ahead

#### tested dates, decisions & issues

- :white_circle: [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md), [5/26/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-26.md) users used search button, enter, and selecting an item from the pop-up to trigger search. [1594](https://github.com/18F/openFEC/issues/1594), [1652](https://github.com/18F/openFEC/issues/1652) [:tv:](assets/right_to_rise.gif)
- :large_orange_diamond: search icon may confuse, but not as much as drop down icon.

  - [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md) filter input boxes that function differently should indicate that they do (this may be sufficiently accomplished by the presence of the free-text search prompt appearing in the contextual menu)

### filtering

#### tested dates, decisions & issues

- :red_circle: [6/9/2016]() users felt like blah [issue]()
- :red_circle: [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md) many users interpreted the filters as "or" as opposed to an "and", only some of the users comprehended what was happening after the search results were shown [1653](https://github.com/18F/openFEC/issues/1653) [:tv:](assets/gates-sample.gif)
- :white_circle: [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md) sticky filter panel more likely to be seen

## Results Listing 3

### sorting

- :large_orange_diamond: [5/12/2016]() before attempting filter tasks, many users seek to sort on name first. Seems they are using sorting as a "fuzzy" filter that lets them see things that are close to their desired term. This may be a coping mechanism for data which is inevitably imperfect. [1652](https://github.com/18F/openFEC/issues/1652)

## Keep an eye on

feature                    | note
:------------------------- | :------------------------------------------------
employer text box          | expressed desire for including multiple employers
`received from` checkboxes | default should have both checked?

## Initial directional research

to be added
