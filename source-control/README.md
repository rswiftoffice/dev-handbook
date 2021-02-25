# Collaborating on code

We use git to work on code together. Git is a version control tool that lets us track changes to a repository.

When using [GitHub](https://github.com/), you should try to follow our best practices.

## Sections within Source Control

* [Merge Strategies](contributing/merge-strategies.md)
* [Branch Naming](contributing/naming-branches.md)
* [Versioning](versioning/readme.md)

## Goal

* Following industry best practice to work in distributed teams which encourage contributions from all across Swift Office
* Improve code quality by enforcing reviews before merging into main branches
* Improve traceability of features and fixes through a clean commit history

## General Guidance

Consistency is important, so agree to the approach as a team before starting to code. Treat this as a design decision, so include a design proposal and review, in the same way as you would document all design decisions

## Creating a new repository

When creating a new repository, the team should at least do the following

* Agree on the **branch**, **release** and **merge strategy**
* Define the merge strategy ([linear or non-linear](./contributing/merge-strategies.md))
* Lock the default branch and merge using [pull requests (PRs)](../code-reviews/pull-requests.md)
* Agree on [branch naming](./contributing/naming-branches.md) (e.g. `user/your_alias/feature_name`)
* Establish [branch/PR policies](../code-reviews/pull-requests.md)
* For public repositories the default branch should contain the following files:
  * [LICENSE](../resources/templates/LICENSE)
  * [README.md](../resources/templates/README.md)
  * [CONTRIBUTING.md](../resources/templates/CONTRIBUTING.md)
