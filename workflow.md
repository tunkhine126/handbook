# Workflow

### The Do's

 - Divide work to be done into Sprints.
 - Select [Sprint] length of either 1 or 2 weeks, max.
 - Define type of Sprint as either a [Feature Sprint] or a [Housekeeping Sprint].
 - Plan before each [Sprint].
 - Own your [Pull Requests].
 - Reflect after each [Sprint].
 - Start Sprints on Tuesdays.
 - Deploy on Mondays.
 - Name branches appropriately.


### The Don'ts

 - **NO** Friday deployments.
 - **NO** failing tests on master.

---

## Pull Requests

 - Feature should live on a branch.
 - Task branches should build off and pull requests compared against the feature-branch.
 - Task branches should get merged into the feature-branch, then feature-branch merged into master.
 - Final pull request should be against master, once feature is complete.

### Branches
#### Naming Structure
```
Feature Branch: engineer/feature
Task Branch:    engineer/feature/task
```

#### Naming Examples
```
Feature Branch: mjl/refactor-fundraising
Task Branch:    mjl/refactor-fundraising/public-campaign-view
```

---
## Sprints
Influenced by [Scrum](https://www.amazon.com/Scrum-Doing-Twice-Work-Half/dp/1847941109/ref=sr_1_2?s=books&ie=UTF8&qid=1523450369&sr=1-2), we work in Sprints. Whether a new product or an existing feature, the work gets divided into 1 or 2 week chunks based on the estimated complexity. Working in Sprints creates a nature start and stop point for planning and reflection.

### Sprint Types
Supporting existing products while building new features requires a give and take. To make sure we're still available to the rest of the team while allowing room for Deep Work, we've chosen to treat certain Sprints differently. We have Feature Sprints and Housekeeping Sprints.

#### Feature Sprint
The focus of a feature sprint is development, first and foremost. While we would never neglect the needs of fellow team members, the schedules of those working on Feature Sprints should be deliberately kept clear of distraction wherever possible.

#### Housekeeping Sprint
The focus of housekeeping sprints is maintaining the existing code base and planning future feature sprints. In a perfect world, an engineer would roll off a Feature Sprint and onto a Housekeeping Sprint where they would be available for deployment related bugs and issues while they scope and plan the next Feature Sprint.

Housekeeping Sprints carry with them the assumption of a few "evergreen tasks":
- Support Deployment
- Documentation
- Training
- Architecture Evaluation

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job.)
   [Pull Requests]: <#pull-requests>
   [Sprint]: <#sprints>
   [Feature Sprint]: <#feature-sprint>
   [Housekeeping Sprint]: <#housekeeping-sprint>

