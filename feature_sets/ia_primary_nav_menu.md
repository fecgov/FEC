# IA & Primary nav feature set

- To help users navigate to the different site sections
- To show the structure of the site and what it makes available

![assets/nav.png](assets/nav.png)

## key:

:red_circle:           | Relatively severe, insurmountable experience issue, failures endemic. Recommend that action is taken (`red_circle`)
:--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:large_orange_diamond: | Moderate experience issue; reasons for failure or success are complicated, inconsistent and/or may be addressed by other fixes (`large_orange_diamond`)
:white_circle:         | Minor or nonexistent experience issue, or unclear finding, no action indicated (`white_circle`)
decision bullet format | `- [needs action indicator]` Problem: "Users thought this happened, or expected this, when really this" then if :red_circle: Fix/hypothesis statement: "we think that by making this X do Y, it will improve" or if :large_orange_diamond: Why to address this later (any dependent issues or pre-fix fixes) or if :white_circle: The thing we were looking for in testing / Recap of why no action : Inconclusive test / Not enough data / Good enough!`[Assigned in GitHub issue #]` `[tested date link]` `[demo gif link]`

## navigation / information architecture / hierarchy

- :red_circle: PROBLEM: Users get lost when moving between the candidate profile pages and financial data that the user associates with those candidates. That data is already legally (and hierarchically on the site) linked to committees (and advanced data tables such as receipts and disbursements). E.g.: "How much has Bernie Sanders raised in big dollar donations?" [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`
- :red_circle: PROBLEM: Users routinely seek out filing deadline information by going first to the registration and reporting, rather than calendar where this information is. This finding is robust across a few weeks of testing. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) [issue: 1721](https://github.com/18F/openFEC/issues/1721)

  - :wrench: Create prominent pathways from registration and reporting to calendar deadlines

  - :wrench: Clarify interlinkages between candidate and candidate data; enhance committee links to candidate --- particularly apparent in mobile. The fix?: Collapse some information in mobile that appeared overlooked by testers today

  - :wrench: Interlinkages between candidate and candidate data (whether the candidate data is in the committee or candidate advanced data table )

  - :wrench: (?) Visual difference between a link that take you to a profile page, and links that take you to a data table

## mega menu

- :red_circle: PROBLEM: User did not navigate to individual contributions. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) [issue: 1722](https://github.com/18F/openFEC/issues/1722)

  - :wrench: Integrate recognizable phrases between receipts and donor lookup
  - :wrench: create prominent separate linked donor look-up tool

- :large_orange_diamond: PROBLEM: User expected to see a search box right away on the mobile view. Something they could type into. Did not know the visual cues for the menu in mobile view. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

- :large_orange_diamond: mega menu taking over full screen size is problematic [tested 5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md) [issue: Style 313](https://github.com/18F/fec-style/issues/313)[:tv:](assets/megamega.gif)

## mobile menu

- :large_orange_diamond: PROBLEM: User did not understand the hamburger icon was the trigger for the menu. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

  - :wrench: Hamburger menu might not be effective for various users different levels of computer literacy/less text and mobile savvy users.

- :red_circle: PROBLEM: One tester noted that she couldn't find her way from the candidates' date filter screen to the home screen. Even though it was only one user, our team believes this will be good design practice

  - :wrench: Add home as a discrete link on the mobile menu. [tested 6-9](https://github.com/18F/FEC/blob/master/test_scripts/2016-6-9.md) :construction: `to be issued`

## Keep an eye on

feature                    | note
:------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
nav item for donor look up | "individual contributions" was slightly confusing, it might make sense to change to "contributions from individuals" [5/19/2016](https://github.com/18F/FEC/blob/master/test_scripts/2016-5-19.md)
nav item for donor look up | language - getters versus givers. contributions from individuals.
