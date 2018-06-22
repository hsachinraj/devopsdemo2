# Accelerating DevOps 

Agile software delivery is key because it helps organizations innovate faster and gets new software in the hands of consumers sooner. This requires new, more productive ways of working for enterprise IT teams. Development teams have already undergone several “transformations” in recent years, from the siloed waterfall approach to agile methodology and now DevOps. Software is the true differentiator in the age of digital transformation, and many companies are using DevOps to ensure their software meets the standard.

In this demo, we will walk you through how SmartHotel 360, a fictitious hotel, uses DevOps practices to fuel their digital transformation journey by accelerating software and services delivery

## Prerequisistes
* Team Services Account
* Azure Account

## Agile Planning

The SmartHotel360 team works off of a backlog of requirements or “user stories” in VSTS. The backlog is prioritized so the most important user stories are at the top.  Portfolio or product owners can create their vision, roadmap, and goals for each release, monitor progress across their portfolio of projects, and manage risks and dependencies. 

1. The SmartHotel development has multiple feature teams - web, mobile. Each team has its own backlog to plan, prioritize, and track their work.Each team can specify how they work - for instance,they can choose the WIs they manage, their working days and how they manage bugs, iterations, etc.,

1. All feature teams at SmartHotel360 use Scrum and work in sprints. A series of sprints is setup for all teams. While each team can choose their own sprints and sprint intervals, all feature teams follow the same sprint cycle consistently across teams.

1. The product owner owns the backlog and adds, changes, and reprioritizes user stories based on the customer’s needs. They create high-level requirements (Epic) which are then mapped to low-level features and user stories. Each user story is then assigned to the respective teams.

1. Each feature team's view of the backlog only includes those work items assigned to their area path, For example, when a member of the SmartHotel/Web team logs in they will only see work items assigned to their team. Here we show parents which provides a few of the features and epics to which the backlog items belong. 

    >Items that are owned by other teams appear with hollow-filled bars. For example, Mobile feedback and Text alerts belong to the Mobile Management team.
 
1. While the hierarchical team and backlog structure works well to support autonomous teams to take ownership of their backlog, it also supports assigning work to teams from a common backlog. During a sprint or product planning meeting, product owners and development leads can review the backlog and assign select items to various teams.

1. While Backlogs provide a list view of work items, **Boards** display work items as cards so that it is easy to visualize the flow of work items. VSTS supports two types of boards—Kanban and task. Kanban boards are sprint-independent, and you monitor the flow through the cumulative flow chart. 

1. Task boards track tasks defined for a sprint and you monitor the flow via the sprint burndown chart

1. When a team member starts to work on a work item, the item is assigned to himself. If that work item needs a code change, they create a **new branch** from the work item. Not only this allows team members to isolate code changes and raise a pull request for users to collaborate on code, it also  supports traceability, providing visibility into all the branches, commits, pull requests, and builds related to the work item.

1. SmartHotel360 teams use **Git** for version control. Every change is made in a separate branch. When the change is committed and pushed, a pull request is created so other people can review the changes and provide feedback. Once the feedback are incorporated and the changes are approved, they are merged with the master branch

1. SmartHotel teams also make use of **branch policies** to  enforce code quality and change management standards and also to protect their important branches such as master. Every changes is reviewed by the entire team and need a minimum number of reviewers to approve the changes without rejection

1. Team members collaborate on code changes using comments - say, to make suggestions, reply to previous comments, and point out problems with the proposed changes, etc.,

1. Teams also use the **build validation** policy as an additional protection. When a build validation policy is enabled,  a new build is queued when a new pull request is created or when changes are pushed to an existing pull request targeting this branch. The build policy then evaluates the results of the build to determine whether the pull request can be completed.

1. Once the reviewers approve the changes and the build is successful, the pull request is completed and the changes are merged with the base branch.

## Continuous Integration and Delivery

SmartHotel Teams practice Continuous Integration (CI)  to automate the merging and testing of code. Implementing CI helps them to catch bugs early in the development cycle, which makes them less expensive to fix. Teams also execute automated tests execute as part of the CI process to ensure quality. Artifacts are produced from CI systems and fed to release pipelines to drive frequent deployments. 

1. SmartHotel teams have different build definitions for each type of application - say a build definition for a public website, one for backend services, one for internal booking system, etc.

1. A build definition is a representation of the automation process that the team wants to run to build and test their application. The automation process is a collection of tasks. Out of the box, VSTS comes with hundreds of tasks for building and testing any type of application including .Net, Java, Node, Android, Xcode, and C++ applications.  In addition to that, there are several hundreds of extension created by our partners on the marketplace that can be downloaded and used.

1. SmartHotel Teams use **Hosted agents**, wherever possible, to build and deploy code. These are agents running on Microsoft Azure. Microsoft provides hosted Windows, Linux and MacOS agents. When they need more control and/or need an interactive agent for things such as running automated testing, they use **Private agents** which are self-hosted.

1. 



