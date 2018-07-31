# Default Contributor License Agreement 

## Welcome
We're glad you're thinking about contributing to an FEC open source project! If you're unsure about anything, ask us — or submit the issue or pull request anyway. The worst that can happen is that we’ll politely ask you to change something. 

We love all friendly contributions, and we welcome your ideas about how to make the FEC's online presence more user friendly, accessible, and elegant. 

To ensure a welcoming environment for our projects, our staff follows the FEC Code of Conduct [pending]; contributors should do the same. Please also check out the [FEC Open Source Policy](https://github.com/fecgov/FEC/blob/master/OPEN-SOURCE-POLICY.md). 

If you’d prefer, you can also reach us by [email](mailto:opensource@fec.gov).

## Public domain
By submitting a pull request, you agree to comply with the policies on our license page.

This document is about how to contribute to FEC projects. This process looks a bit different depending on whether you’re a member of the public, an FEC employee, or a member of a specific team. Here’s what you can find in this doc:

- Public contributions
- FEC contributions 
    - Branches
    - Front end architecture
    - Standards and benchmarks
- Public domain

### Issues
We use GitHub issues to track user issues and team tasks. Whenever possible, we follow this outline:
 
1. Goal: a quick blurb explaining the bug or what the issue should accomplish. What is the user need?
2. Completion criteria: how we’ll know that this issue has been completed
3. Tasks to completion:
    - [ ] Use 
    - [ ] Markdown
    - [ ] Checklists 
4. Dependencies (optional): What other issues out there need to be completed before you can do this one? Include links to tickets with the dependency.
5. For development issues, include:
Unknown tasks or dependencies that need investigation
[The boilerplate tasks for each development issue](https://gist.github.com/theresaanna/86be7e29214a7f31ab73)

### Commit messages
- Good commit messages start with a verb, like “adds” or “changes” or “removes.” 
- Be sure to talk about the nature of the change you're making. Explain why the change is needed, rather than simply describing the bug or task it addresses. 
- If your commit resolves an issue, reference it in the commit messages. For example “fixes #555.” Read more GitHub guidance on [closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).
- We encourage you to follow the [50/72 format](http://stackoverflow.com/questions/2290016/git-commit-messages-50-72-formatting).

### Pull requests
- Anyone may informally review a pull request and make comments or suggestions. 
- When a pull request is ready for review, label it `plz-review`. 
- Include a summary of all work and changes.
- Use `cc @username` to notify a specific team member to review a pull request.


## Public contributions
Thank you for contributing to an FEC open source project. If you're unsure about anything, just send us an [email](mailto:opensource@fec.gov) with your question or submit an issue https://github.com/fecgov/FEC.

We want to ensure a welcoming environment for all of our projects. Our staff follow the FEC Code of Conduct [pending] and all contributors should do the same.

We encourage you to read the project's contribution agreement (you are here), its [license](https://github.com/fecgov/FEC/blob/master/LICENSE.md) and its [readme](https://github.com/fecgov/FEC/blob/master/README.md).

If you see an error or have feedback, the best way to let us know is to file an issue.
- To contribute a specific change to the project, outside contributors will need to fork this repo.

## FEC contributions
There is a team actively working on this project. You can find us in Slack or FEC email.

## Branches
Any FEC team member should be able to make a branch of the project and submit a Pull Request (PR). 

The master, staging, and production branches are protected. Only administrators of the repo can push directly to those branches. FEC staff who think they don't have the correct permissions should ask in Slack or FEC email.

## Submitting pull requests
If you submit your PR from the Github website or via the Github Client app include any issues your PR addresses. If the PR changes are not associated with an issue, please leave a brief message detailing what was wrong with the application before, and how it *should* be.

If the nature of the PR is visual, please replace all instances of BRANCH_NAME with the name of the branch that is being merged.

Complete the PR message by detailing all fixes and tagging GitHub users who should review the work, with a note about what they should be reviewing. In general:
- If you are not an admin or member of the FEC team, tag someone who you would like to review and merge your PR
- If you are an admin for the repo or a member of the FEC team, you are responsible for merging your own PRs after they have been reviewed and approved by someone else on the team
- If you have been asked to review a PR, leave a clear message indicating your approval, either through the formal PR review feature or by commenting (at the very least, with a note saying LGTM, or "Looks good to me")
- If your PR includes many small, incremental commits, consider squashing them
- Don’t merge until linters pass, unless you have discussed with reviewers and approved exceptions

## Front end architecture
See project [README](https://github.com/fecgov/FEC/blob/master/README.md) for details. 

## CSS
See project [README](https://github.com/fecgov/FEC/blob/master/README.md) for details.

## Images
See project [README](https://github.com/fecgov/FEC/blob/master/README.md) for details.

## JavaScript
See project [README](https://github.com/fecgov/FEC/blob/master/README.md) for details.

## Standards and benchmarks

## Device and browser support
The user interface should support all versions of Internet Explorer still supported by Microsoft, as well as recent versions of Chrome, Safari, and Firefox
When applicable the user interface should be mobile responsive

## Performance
See project [README](https://github.com/fecgov/FEC/blob/master/README.md) for details.

## Public domain
For detailed license information, see our default license.

All contributions to this project will be released under the CC0 dedication. By submitting a PR, you are agreeing to comply with this waiver of copyright interest.
