# Data Overview Page

Feature set overview `![name of key image of feature set](assets/feature-set-key.png)`

## key:

:red_circle:           | Relatively severe, insurmountable experience issue, failures endemic. Recommend that action is taken (`red_circle`)
:--------------------- | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:large_orange_diamond: | Moderate experience issue; reasons for failure or success are complicated, inconsistent and/or may be addressed by other fixes (`large_orange_diamond`)
:white_circle:         | Minor or nonexistent experience issue, or unclear finding, no action indicated (`white_circle`)
decision bullet format | `- [needs action indicator]` Problem: "Users thought this happened, or expected this, when really this" if :large_orange_diamond: Why to address this later (any dependent issues or pre-fix fixes) or if :white_circle: The thing we were looking for in testing / Recap of why no action : Inconclusive test / Not enough data / Good enough!`[Assigned in GitHub issue #]` `[tested date link]` `[demo gif link]` then if any Fix/hypothesis statements exist: :wrench: "we think that by making this X do Y, it will improve" or

## feature set feature group `[feature set feature group number from image]`

### Graph Overview Notes

- User failed to find or see the date of the `in-progress date` fast enough to satisfy their experience.

  - :wrench: Increase prominence of when the data in each chart has been most recently updated
  - :wrench: to clarify or indicate when data was last updated use timestamp or other feature that communicates timeliness

### Graphic visualization style

- :white_circle: :large_orange_diamond: On the Totals Graph, Diagonal lines (grey lines over colored bars) may be hard for users to read.
- :large_orange_diamond: Testing participant noted the time periods are not the same in each chart of the graph. She didn't notice this right off the bat, but said this is kind of "misleading."

  - possible :wrench: Make sure we consistently frame time periods the same way as we report data.

### Graphic interaction style

- :large_orange_diamond: Problem: Users first interpreted the graph as the total raised each month instead of a cumulative total up to the month selected. Users consistently articulated needing a better indication of what they were looking at before having to interact with the graph. One user expressed that the table data did not immediately register as specifically correlating to the month the vertical line is on, until the user interacted with the arrows and moved it to a new month. Once that happened, the user saw the association. [tested 8/4/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-08-04.md)
 - :wrench: Adding some shading to the left side of the vertical dotted line might help users understand that the total is a cumulative total up to the month selected. Also adding more interactivity to be able to change the month or quarter by dragging the vertical line may help.

- :large_orange_diamond: Problem: The majority of the participants did not understand or were unsure of what the dotted line represented. [tested 8/4/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-08-04.md)
 - :wrench: Many users wanted to be able to drag the dotted line, thus adding a short explanation on hover/click to the vertical dotted line may help.

- :white_circle: One user struggled to understand how the interactivity of the graph "next month" or "previous month" buttons or dotted line worked. Others were successful with both buttons. Keep an eye on expected interactivity on hover and/or click as the graph interaction may be improved on the live site. [tested 8/4/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-08-04.md)

- :white_circle: The users successfully understood what the dots meant on the line graph, however, it did take a few minutes to process and understand. All users communicated that they understood different filers had different filing schedules.  [tested 8/4/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-08-04.md)

- :large_orange_diamond: Problem: Largely, users did not understand why the top two lines extended the length of the graph while the bottom two lines stopped half way. Another observation was that none of the users seemed to notice that the bottom line was shorter until it was brought to their attention.[tested 8/4/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-08-04.md)
 - :wrench: When users move the vertical dotted line, there should be an indication on the numbers on the right hand side that Party Committees and others have no data because they have not filed yet for the selected time period. Also, extending the incomplete line with a dotted line for the time period with unavailable data may be useful.

## Initial directional research

to be added
