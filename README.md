# Code coverage report for Go and TypeScript

## Prerequisites
#### TypeScript
* yarn
* package.json must contain a script `yarn test:coverage` which generates a report in `"jest --coverage"` style
* runs in node 16.x environment

## Description

**Code coverage comment not posted on PRs from forks.** That information can still be gleaned from the output of the previous step in the run.

This workflow does the following for caller pull requests:

* Checks out caller's PR's code
* Checks out caller's code on main
* Calculates test coverage for each
* Leaves a comment on the PR with a test coverage report with the difference between PR coverage vs main coverage
* When commits are added to the PR, the existing comment should be updated with an up-to-date coverage report
