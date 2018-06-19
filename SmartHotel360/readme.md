# Accelerating DevOps 

Agile software delivery is key because it helps organizations innovate faster and gets new software in the hands of consumers sooner. This requires new, more productive ways of working for enterprise IT teams. Development teams have already undergone several “transformations” in recent years, from the siloed waterfall approach to agile methodology and now DevOps. Software is the true differentiator in the age of digital transformation, and many companies are using DevOps to ensure their software meets the standard.

In this demo, we will walk you through how SmartHotel 360, a fictitious hotel, uses DevOps practices to fuel their digital transformation journey by accelerating software and services delivery

## Prerequisistes
* Team Services Account
* Azure Account

## Agile Planning

The SmartHotel360 team works off of a backlog of requirements or “user stories” in VSTS. The backlog is prioritized so the most important user stories are at the top. The product owner owns the backlog and adds, changes, and reprioritizes user stories based on the customer’s needs. 

1. Click on the Plans tab under the Work hub and click on the delivery plan.
    DevOps is about working together and having visibility into all the work that is being worked on. Using the Delivery Plans tool, we can help drive cross-team visibility and alignment by tracking status on an iteration-based calender. Users on our teams can tailor their delivery plans to include any team or backlog view (such as epics, features, or requirements for any given team). Especially for us at BikeSharing360, we are able to see how our work fits in with the other work that the mobile team is completing in their iteration.

1. Click on the Backlogs tab below the Work hub and click on Epics on the left side of the panel.

    Talk track: We can view the epics for the project that the teams are working on. We can even drill down to the hierarchy of our epics that relate to features, user stories (requirements/product backlog items), and tasks.

1. Click on Features on the left side of the panel, below Epics.

    Talk track: We can also view features for the project in the same manner.

Click on **Backlogs** on the left side of the pane, below Features. 

    > Talk track: We can also view our user stories for the project and the cumulative flow diagram and velocity chart. 

    <img src="images/vsts-backlogs.png" />

1. Click on the **Board** tab next to the **Backlog** tab (above the backlog of user stories.)

    > Talk track: We can visualize all of the work that is flowing through our system using the Kanban board.

1. Click on the "Iteration 1" node (current) below the Backlogs node. 

    > Talk track: In our current iteration, the first user story to complete in our backlog is "[public web] Generate usage reports". Let's go into the task board to assign it to ourselves and start working on it. 

1. Click on the **Board** tab next to the **Backlog** tab then drag and drop the "Development" task from the New state into the Active state to begin work. It should assign the task automatically to you. 

    > Talk track: I'm going to work on the development of the generate usage reports user story, so I'm going to change the state of the task to active to work on it. 

1. Click on the "..." on the right side of the "Development" task and click on the "Create branch" button. 

    > Talk track: We can create branches in our Git repository right from our task so that task is immediately associated with that development work. 

1. Type in "ReportName" as the name of the branch, select the appropriate Git repository that has the BikeSharing360 code in it, as well as the master branch to base the new branch off of, then click on the "Create branch" button. 

    > Talk track: Now we have a new branch that is dedicated to our work on that task that our team can also access if needed. 

