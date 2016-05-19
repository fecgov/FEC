# May 19, 2016 Usability Test.

raw notes: <http://mur.al/bLxMBeX5>

## Tasks:

AO 1 <https://gsa.invisionapp.com/share/9Q710V45R#/screens/152290006_AOs_Landing>

Typeahead search on data site <https://beta.fec.gov/data/receipts/?max_date=04-13-2016>

Cloze Test: <https://beta.fec.gov/registration-and-reporting/independent-expenditures/> <https://docs.google.com/document/d/1-0mc-kd-jCZnMM4ZEEu3vpxCN-QYn3JX6egJdkVO4c4/edit#heading=h.vk6cigldvzxn> AO 2 <https://gsa.invisionapp.com/share/9Q710V45R#/screens/152290010> <https://gsa.invisionapp.com/share/9Q710V45R#/screens/152290007>

Mega-menu interaction <https://fec-feature-proxy.18f.gov>

Results of AO search <https://github.com/18F/fec-eregs/issues/70>

## Introduction Script:

Hi, I'm **_**, and I'm working on the Federal Election Commission website redesign. We're asking people to try using the website and take a look at some of the designs we're working on today, to see if everything works as intended. This session should take about 25 - 30 minutes.

The first thing I want to make clear right away is that we're testing out the site, not you. You can't do anything wrong here. In fact, this is probably the one place today where you don't have to worry about making mistakes.

So this may feel a little weird, but as you use the site, I'm going to ask you as much as possible to try to think out loud: say what you're looking at, what you're trying to do, and what you're thinking. This is be a huge help to us.

Also, please don't worry that you're going to hurt our feelings. We're doing this to improve the site, so we need to hear your honest reactions.

If you have any questions as we go along, just ask them. I may not be able to answer them right away, since we're interested in how people do when they don't have someone sitting next to them to help. But if you still have any questions when we're done I'll try to answer them them. Sound ok? (credit: Krug)

Script: Give us a quick 1 minute your background. What do you know about the FEC? What does the FEC do?

### Task 1:

Advisory Opinion pages

Link 1: <https://gsa.invisionapp.com/share/9Q710V45R#/screens/152290006_AOs_Landing>

Are you familiar with Advisory Opinions? (If no, read this) An Advisory Opinion is when a campaign or committee asks the FEC to determine if something they are interested in doing is legal. Once the FEC decides, other campaigns and committees look at the Advisory Opinion as guidance. I'd like to have you take a look at a page and tell me about it. You'll notice some of the content is placeholder text, but I'd like to hear what you think the text would be about. Load page Talk me through this page. What is it? What do you see? What can you do? If you wanted to find an advisory opinion about, say, "filing", can you do that? (If they haven't talked about the left column...) What's going on in that gray column on the left? Task 2 : Typeahead Link: fec-feature-proxy.18f.gov/data/receipts/?max_date=04-13-2016

Script: First, we'd like you to take a look at this page (share link). Could you look up all receipts to the group "Right to Rise." Could you filter those receipts to people with the last name of Smith? Now how about people named John Smith? Now how about "Jet PAC"

### Task 3:

Content Test: Independent Expenditure I'd like you to read this page. You don't have to read it aloud. Let me know when you're done. <https://beta.fec.gov/registration-and-reporting/independent-expenditures/> Great, now remembering that we're testing the page and not you, I'd like you to fill out this link: <https://docs.google.com/document/d/1-0mc-kd-jCZnMM4ZEEu3vpxCN-QYn3JX6egJdkVO4c4/edit#heading=h.vk6cigldvzxn>

### Task 4:

AO Task 2 Link 1: <https://gsa.invisionapp.com/share/9Q710V45R#/screens/152290010>

Script: What is this page about? What is this Advisory Opinion about? Where can you go from here? [Go to link 2]

Link 2: <https://gsa.invisionapp.com/share/9Q710V45R#/screens/152290007> [Note: You can toggle between the two views by clicking the "AO" in the title.]

Script: What is different now? What is this Advisory Opinion about?

### Task 3 :

Mega-Menu Navigation Link: <https://fec-feature-proxy.18f.gov> Use the site to find independent expenditures data. Use the site to find fundraising data for candidates for House.

## Wrap-up Script:

Before we wrap up, do you have any questions or comments for our team?

Content Tests = = = = = 4/21 Synthesis Task 1\. Typeahead Observed: Both users used additional filters (individual/committee) without prompting. Both users understood how to type into search box.

Takeaways: More obvious change state could be helpful when any results change, not just a long load. We'd like to consider possible A/B test on filter functionality (does it expand results or narrow results?).

Task 2\. Legal search Observed: Both users had hesitancy clicking. But both confidently identified legal resources in top nav as the main section for AOs.

Saw one preference for search and another preference for "AO" in main body. Both found at least one path to AOs from the legal resources landing page. Second user found both avenues.

Takeaways: We can consider tightening up the search and header areas (this is our most prime real estate, and it could be bumping important informations below the fold). Unclear whether reticence to scroll is an artifact of testing itself.

Should legal resources search find both content and legal data? (Yes, probably).

Task 3 and 4\. Advisory opinion mockups Observed: When we asked users what a page was about, they used the landing page as their only source of information. Strong preference for version B (with summary). Summary does seem to give people a better sense of what AO is about.

Takeaways: Pull out the summary, so it's more prominent. Two-column layout may present a false choice.

What else do we want to bump up? Entities?

Additionally, in the header area, requester is not sufficiently prominent.
