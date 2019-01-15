# Workflow

### The Do's

 - Divide work to be done into [Cycles]/Sprints.
 - Select [Sprint] length of either 1 or 2 weeks, max.
 - Define type of Sprint as either a [Feature Sprint] or a [Housekeeping Sprint].
 - Plan before each [Sprint].
 - Own your [Pull Requests].
 - Reflect after each [Sprint].
 - Start Sprints on Tuesdays.
 - Deploy on Mondays.
 - Name branches appropriately.
 - <a href="https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History" target="_blank">Keep your git history clean</a> (ie rebase often).


### The Don'ts

 - **NO** Friday deployments.
 - **NO** failing tests on master.
 - **NO** [Pull Requests] without personally manual testing & necessary unit tests.

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
## Cycles
TODO: Add in cycle workflow details here

## Sprints
Influenced by [Scrum](https://www.amazon.com/Scrum-Doing-Twice-Work-Half/dp/1847941109/ref=sr_1_2?s=books&ie=UTF8&qid=1523450369&sr=1-2), we work in Sprints. Whether a new product or an existing feature, the work gets divided into 1 or 2 week chunks based on the estimated complexity. Working in Sprints creates a natural start and stop point for planning and reflection.

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

---
## Deployments

### Pre-Production
There is a process for seeing a line of code from start to finish. Whether a content change or a new feature, the process protects the work of fellow engineers and the end user of the products we build.

1. #### Local Development
    Prior to getting started, the lastest version of master should be pulled from Github. Local development should always be performed on a [Branch].

2. #### Pull Request
    Pull Requests allow for other engineers to give us feedback on our work and ensure the ever improving quality of the code we write.

    When you're done, the changes should work on your machine before passing it along. Here are a few questions to determine if it's ready for a Pull Request.
    - Are all appropriate tests written?
    - Have I seen it work in browser?
    - Does this represent a complete feature?

3. #### Review App
    _Thanks [Heroku]!_  

    [Review Apps](https://devcenter.heroku.com/articles/github-integration-review-apps) within the [New Story Pipeline](https://dashboard.heroku.com/pipelines/bfd5df14-35aa-4ec3-a0db-3de361e5ba6b) allow us to QA individual pieces of functionality on siloed environments. Before it goes to staging, it should work in isolation first. Each Review App is automatically created once a PR is built on Github. 

4. #### Staging QA
    Things change between development environment and Heroku. Whether is third-party keys, runtime limits, or specific data in the database, our Staging Environment is the closest possible glimpse at how the code will behave on Production.

    Manually testing changes is the final step before deployment to Production, ie [The Main Event].

### Production Deployment - The Main Event
  The road to a production deployment is deliberate. Gone are deployments straight from a local environment. In favor of speed, reactiveness, and accounting for a single engineer, this worked in the early days. Of course 'worked' is relative considering the fact that breaking changes were regularly pushed to production and there was zero test coverage. As we've grown and matured as a team of engineers, we've come to embody one of [New Story Values](https://newstorycharity.org/vision/): Improve through learning and feedback.

  Holding ourselves to an ever increasing standard of excellence, what got us to where we are today is not what will get us through the next season of growth. Production deployments are our culminating event. Like an artist at a debut, a musician on stage, or a parent on Christmas morning... we have poured our energy and passion into creating something worth sharing.

  A few thoughts summarize Production deployments.
  - It is not a trivial occurrence.
  - Team buy in and excitement is our responsibility.
  - Every engineer owns and supports deployments.

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job.)
   [Pull Requests]: <#pull-requests>
   [Pull Request]: <#pull-requests>
   [Heroku]: <https://dashboard.heroku.com/teams/newstory/overview>
   [Branch]: <#branches>
   [Cycles]: <#cycles>
   [Sprint]: <#sprints>
   [Feature Sprint]: <#feature-sprint>
   [Housekeeping Sprint]: <#housekeeping-sprint>
   [The Main Event]: <#production-deployment---the-main-event>

