# Structure of a Sprint

The purpose of this document is to:

- Provide a structure way to allow delivery teams to start their sprint properly.
- Organize content in the playbook for quick reference and discoverability.
- Extensible hierarchy to allow teams to share deep subject matter expertise.

## Scrum Team Composition

The typical Scrum team size is five to nine people (with seven being the ideal—one product owner, one scrum master, and five developers). 

Unlike traditional development structures, Scrum teams don’t have a structural hierarchy. Instead, they are self-managing and cross-functional. All team members are equally important and together have all the skills and knowledge necessary to deliver a working product.

While everyone has an equal voice, there are three distinct roles within the Scrum team structure.

### Product Owner

The Product Owner is responsible for maximizing the value of the product resulting from work of the Development Team. How this is done may vary widely across organizations, Scrum Teams, and individuals.

The Product Owner is the sole person responsible for managing the Product Backlog. Product Backlog management includes:
• Clearly expressing Product Backlog items;
• Ordering the items in the Product Backlog to best achieve goals and missions;
• Optimizing the value of the work the Development Team performs;
• Ensuring that the Product Backlog is visible, transparent, and clear to all, and shows what
the Scrum Team will work on next; and,
• Ensuring the Development Team understands items in the Product Backlog to the level
needed.

The Product Owner may do the above work, or have the Development Team do it. However, the Product Owner remains accountable.

The Product Owner is one person, not a committee. The Product Owner may represent the desires of a committee in the Product Backlog, but those wanting to change a Product Backlog item’s priority must address the Product Owner. For the Product Owner to succeed, the entire organization must respect his or her decisions. The Product Owner’s decisions are visible in the content and ordering of the Product Backlog. No one can force the Development Team to work from a different set of requirements.

### Scrum Master

### Scrum Delivery Team

## The first week of a project

### Before starting the project

- [ ] [Discuss and start writing the Team Agreements](agile-development/team-agreements/README.md). Update these documents with any process decisions made throughout the project
  - [Working Agreement](agile-development/team-agreements/working-agreements/README.md)
  - [Definition of Ready](agile-development/team-agreements/definition-of-ready/README.md)
  - [Definition of Done](agile-development/team-agreements/definition-of-done/README.md)
  - [Estimation](agile-development/sprint-planning/estimation/readme.md)
- [ ] [Set up the repository/repositories](source-control/README.md#creating-a-new-repository)
  - Decide on repository structure/s
  - Add [README.md](resources/templates/README.md), [LICENSE](resources/templates/LICENSE), [CONTRIBUTING.md](resources/templates/CONTRIBUTING.md), .gitignore, etc
- [ ] [Build a Product Backlog](agile-development/backlog-management/README.md)
  - Set up a project in your chosen project management tool (ex. Azure DevOps)
  - [INVEST](https://en.wikipedia.org/wiki/INVEST_(mnemonic)) in good User Stories and Acceptance Criteria

### Day 1

- [ ] [Plan the first sprint](agile-development/sprint-planning/readme.md)
  - Agree on a sprint goal, and how to measure the sprint progress
  - Determine team capacity
  - Assign user stories to the sprint and split user stories into tasks
  - Set up Work in Progress (WIP) limits
- [ ] [Decide on test frameworks and discuss test strategies](automated-testing/README.md)
  - Discuss the purpose and goals of tests and how to measure test coverage
  - Agree on how to separate unit tests from integration, load and smoke tests
  - Design the first test cases
- [ ] [Decide on branch naming](source-control/contributing/naming-branches.md)
- [ ] [Discuss security needs and verify that secrets are kept out of source control](continuous-delivery/secrets-management/recipes/azure-devops/secrets-per-branch.md)

### Day 2

- [ ] [Set up Source Control](source-control/readme.md)
  - Agree on [best practices for commits](source-control/readme.md#commit-best-practices)
- [ ] [Set up basic Continuous Integration with linters and automated tests](continuous-integration/README.md)
- [ ] [Set up meetings for Daily Scrum Meeting and decide on a Process Lead](agile-development/daily-scrum-meeting/README.md)
  - Discuss purpose, goals, participants and facilitation guidance
  - Discuss timing, and how to run an efficient daily scrum meeting
- [ ] [If the project has sub-teams, set up a Scrum of Scrums](agile-development/scrum-of-scrums/README.md)

### Day 3

- [ ] [Agree on code style](code-reviews/README.md) and on [how to assign Pull Requests](code-reviews/pull-requests.md)
- [ ] [Set up Build Validation for Pull Requests (2 reviewers, linters, automated tests)](code-reviews/README.md) and agree on [Definition of Done](agile-development/team-agreements/definition-of-done/readme.md)
- [ ] [Agree on a Code Merging strategy](source-control/contributing/merge-strategies.md) and update the [CONTRIBUTING.md](resources/templates/CONTRIBUTING.md)
- [ ] [Agree on logging and observability frameworks and strategies](observability/README.md)

### Day 4

- [ ] [Set up Continuous Deployment](continuous-delivery/README.md)
  - Determine what environments are appropriate for this solution
  - For each environment discuss purpose, when deployment should trigger, pre-deployment approvers, sing-off for promotion.
- [ ] [Decide on a versioning strategy](source-control/versioning/README.md)
- [ ] Agree on how to [Design a feature and conduct a Design Review](design-reviews/README.md)

### Day 5

- [ ] Conduct a Sprint Demo
- [ ] [Conduct a Retrospective](agile-development/retrospectives/readme.md)
  - Determine required participants, how to capture input (tools) and outcome
  - Set a timeline, and discuss facilitation, meeting structure etc.
- [ ] [Refine the Backlog](agile-development/backlog-management/refinement/readme.md)
  - Determine required participants
  - Update the [Definition of Ready](agile-development/team-agreements/definition-of-ready/readme.md)
  - Update estimates, and the [Estimation](agile-development/sprint-planning/estimation/readme.md) document
