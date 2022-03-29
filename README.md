# Code coverage report for Go and TypeScript

## Prerequisites
#### TypeScript
* yarn
* package.json must contain a script `yarn test:coverage` which generates a report in `"jest --coverage"` style
* runs in node 17.x environment

#### Go
* runs in go 1.16.1 environment

## Description

This workflow does the following for caller pull requests:

* Checks out caller's PR's code
* Checks out caller's code on main
* Calculates test coverage for each
* Leaves a comment on the PR with a test coverage report with the difference between PR coverage vs main coverage
* When commits are added to the PR, the existing comment should be updated with an up-to-date coverage report
