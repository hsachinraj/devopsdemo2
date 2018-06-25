# Accelerating DevOps 

Agile software delivery is key because it helps organizations innovate faster and gets new software in the hands of consumers sooner. This requires new, more productive ways of working for enterprise IT teams. Development teams have already undergone several “transformations” in recent years, from the siloed waterfall approach to agile methodology and now DevOps. Companies that have adopted DevOps principles are disrupting industries, innovating faster and leaving their competitors in the dust.

In this demo, we will walk you through how SmartHotel 360, a fictitious hotel, uses DevOps practices to fuel their digital transformation journey by accelerating software and services delivery

## Agile Planning

The SmartHotel360 team practices agile development. They follow scrum methodology with a 2 weeks sprint cycle. The SmartHotel development team works off of a backlog of requirements ( aka  “user stories”) . The backlog is prioritized so the most important user stories are at the top. The product owner owns the backlog and adds, changes, and reprioritizes user stories based on the customer’s needs.

1. The SmartHotel development has multiple feature crew teams - web, mobile and as well as customer crew teams. Teams are autonomous and choose how they want to work - they can choose the WIs they manage, their working days and how they manage bugs, iterations, etc.

1. All feature teams at SmartHotel360 use Scrum and work in sprints. A series of sprints is setup for all teams. While each team can choose their own sprints and sprint intervals, all feature teams follow the same sprint cycle consistently across teams.

1. The product owner owns the backlog and adds, changes, and reprioritizes user stories based on the customer’s needs. They create high-level requirements (Epic) which are then mapped to low-level features and user stories. Each user story is then assigned to the respective teams.

1. Each feature team's view of the backlog only includes those work items assigned to their area path, For example, when a member of the SmartHotel/Web team logs in they will only see work items assigned to their team. Here we show parents which provides a few of the features and epics to which the backlog items belong.

    >Items that are owned by other teams appear with hollow-filled bars. For example, Mobile feedback and Text alerts belong to the Mobile Management team.

1. While the hierarchical team and backlog structure works well to support autonomous teams to take ownership of their backlog, it also supports assigning work to teams from a common backlog. During a sprint or product planning meeting, product owners and development leads can review the backlog and assign select items to various teams.

1. While Backlogs provide a list view of work items, **Boards** display work items as cards so that it is easy to visualize the flow of work items. VSTS supports two types of boards—Kanban and task. Kanban boards are sprint-independent, and you monitor the flow through the cumulative flow chart.

1. Task boards track tasks defined for a sprint and you monitor the flow via the sprint burndown chart

1. When a team member starts to work on a work item, the item is assigned to himself. If that work item needs a code change, they create a **new branch** from the work item. Not only this allows team members to isolate code changes and raise a pull request for users to collaborate on code, it also  supports traceability, providing visibility into all the branches, commits, pull requests, and builds related to the work item.

## Git Version Control

1. SmartHotel360 teams use **Git** for version control. Every change is made in a separate branch. When the change is committed and pushed, a pull request is created so other people can review the changes and provide feedback. Once the feedback are incorporated and the changes are approved, they are merged with the master branch

1. SmartHotel teams also make use of **branch policies** to  enforce code quality and change management standards and also to protect their important branches such as master. Every changes is reviewed by the entire team and need a minimum number of reviewers to approve the changes without rejection

1. Team members collaborate on code changes using comments - say, to make suggestions, reply to previous comments, and point out problems with the proposed changes, etc.,

1. Teams also use the **build validation** policy as an additional protection. When a build validation policy is enabled,  a new build is queued when a new pull request is created or when changes are pushed to an existing pull request targeting this branch. The build policy then evaluates the results of the build to determine whether the pull request can be completed.

1. Once the reviewers approve the changes and the build is successful, the pull request is completed and the changes are merged with the base branch.

## Continuous Integration and Delivery

SmartHotel Teams practice Continuous Integration (CI)  to automate the merging and testing of code. Implementing CI helps them to catch bugs early in the development cycle, which makes them less expensive to fix. Teams also execute automated tests execute as part of the CI process to ensure quality. Artifacts are produced from CI systems and fed to release pipelines to drive frequent deployments.

1. SmartHotel teams have different build definitions for each type of application - say a build definition for a public website, one for backend services, one for internal booking system, etc.

1. A build definition is a collection of tasks required to run to build and test their application. Out of the box, VSTS comes with hundreds of tasks for building and testing any type of application including .Net, Java, Node, Android, XCode, and C++ applications.  In addition to that, there are several hundreds of extension created by our partners on the marketplace that can be downloaded and used.

1. SmartHotel Teams use **Hosted agents**, wherever possible, to build and deploy code. These are agents running on Microsoft Azure. Microsoft provides hosted Windows, Linux and MacOS agents. When they need more control and/or need an interactive agent for things such as running automated testing, they use **Private agents** which are self-hosted.

1. An another important aspect of DevOps is continuous testing. SmartHotel teams embed automated tests at every phase  of the lifecycle helps to ensure high-quality, reliable software. They run unit tests as part of their Continuous integration build. This helps teams to catch bugs very early on in the development cycle and minimize the cost of fixing them. VSTS supports many unit testing frameworks such as NUnit, XUnit, MSTest, Jasmin, JUnit, etc.

1. Teams also enable **Code Coverage**  to determine if the committed code changes are tested by unit tests. Additionally to speed test executions,teams turn on **Run only impacted tests** option which  only runs the relevant tests, rather than all tests, required to validate the committed code.

1. Only when the code passes all the tests and code coverage rules, the build is considered successful and picked by up release service for deployment. SmartHotel uses VSTS Release service which provides a streamlined experience to deploy the apps to one of Azure's many services, from Azure Web App to Container Registry, SQL Database, Kubernetes Service, etc.

1. Teams use VSTS to fully automate the deployment pipeline from creating the infrastructure, configuring, deploying and validating the deployment. Applications are deployed through multiple environments such as dev, staging before they are deployed to production

1. SmartHotel Teams practice **Infrastructure as Code**, another key DevOps practice that teams use to automatically provision and manage infrastructure. Since they have a diverse portfolio of applications, they need to deploy multiple tools - sometimes even open-source tools such as Terraform. VSTS gives them the flexibility to choose the tool they want to use, including third-party OSS tools.

1. Teams control the start and completion of the deployment process to environments with **approval and gates**. Each environment in a release definition is configured with pre-deployment and post-deployment conditions that can include waiting for users to manually approve or reject deployments, and checking with other automated systems until specific conditions are verified.

1. A deployment starts only when the necessary approvals are granted and when a deployment is in progress, just like the Build service, outputs at real-time are displayed in the log console.

## Traceability and Dashboard

Share progress and status with your team using configurable team dashboards. Dashboards provide easy-to-read, easy access, real-time information. At a glance, you can make informed decisions without having to drill down into other parts of your team project site.

Use your team project wiki to share information with other team members.