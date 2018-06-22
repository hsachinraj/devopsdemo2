# Getting started with Visual Studio Team Services 

## Overview

overview of vsts goes here

Visual Studio Team Services provides everything a development team needs, from agile planning to version control, testing, build and deploy, to turn ideas into working software. It works for any application, any language and any platform

## What's covered in this lab?

 In this lab, you will see 
* Agile planning
* Version control and collaborate on code changes 
* Plan and execute testing
* Continuously build and deploy applications

## Pre-requisites for the lab

1.  **Microsoft Azure Account**: You will need a valid and active Azure account for the Azure labs. If you do not have one, you can sign up for a [free trial](https://azure.microsoft.com/en-us/free/){:target="_blank"}
    
     * If you are a Visual Studio Active Subscriber, you are entitled for a $50-$150 credit per month. You can refer to this [link](https://azure.microsoft.com/en-us/pricing/member-offers/msdn-benefits-details/) to find out more including how to activate and start using your monthly Azure credit.
     * If you are not a Visual Studio Subscriber, you can sign up for the FREE [Visual Studio Dev Essentials](https://www.visualstudio.com/dev-essentials/)program to create **Azure free account** (includes 1 year of free services, $200 for 1st month).
1. **Visual Studio Team Services** Account

## Setting up the project

We will use [Visual Studio Team Services Demo Generator](http://vstsdemogenerator.azurewebsites.net) to create a project with sample data needed for following this lab. 

1. Go to [Visual Studio Team Services Demo Generator](http://vstsdemogenerator.azurewebsites.net) and sign in with your credentials

1. Select the VSTS account that you want to use. Provide a project name and select the **SmartHotel 360** template.

1. Select any extension(s) that needs to be installed and enabled in your account

1. Click **Create Project** to start creating the project. Once the project is created, the URL to the project will be displayed. Select that to navigate to the project.

## Overview of the new UI design

If you have used VSTS before, you may notice that VSTS has now a new look. We have revamped the UI across the product to give you an optimal experience. You will find all the projects and teams and also your favorite items on the home page.

1. Select the project that you just provisioned.

1. This will open the summary page for the project where you will see the readme file that describes the project. Typically, VSTS would default to the readme file in the root of your default repository. If the project description is in another file, or in an another repository or in Wiki (and not in a readme file), you can specify that by selecting the **change** button.

1. On the right side, you will a visual summary of activities performed in the project - like number of work items created/changed, number of commits, PR and also build and release summary. 

1. Select **Dashboard** from the left side nav. Dashboards provide easy-to-read, real-time information about your project in one glance without having to drill down into different parts of the project. You can customize the dashboard - you can create as many dashboards as you want and change what you want to see in each dashboards. There are so many widgets that's available for you to select.

1. The last thing in the overview section is **Wiki**. You can use your team project wiki to share information such as  project objectives, epics, specs, release notes, best practices, or other content with all your team members. 

## Agile Planning with VSTS

We will now move to **Work** hub. With VSTS, teams can plan and track the progress of your project user stories, features, bugs, etc.  Out of the box, VSTS supports different process templates including Scrum, Agile and CMMI. You can use it as-is or customize the template to fit your process - that includes adding new fields, status, workflows, etc.,

1. Select **Backlogs** - You can start planning your project by quickly adding user stories or requirements, bugs or defects, tasks, etc., to your product backlog. You use work items to share information, assign work to team members, track dependencies, organize work, and more. 

1. Once you have defined the product backlog, you can order them and create a prioritized list of work. To reorder your backlog, you simply have to drag the work items.

1. As you start working on the work items, you will need to track the status of each item. VSTS makes it easy with **boards** that allows you to visualize the flow of work items. If you are working from the Stories (Agile) or Backlog items (Scrum) pages, you have access to the product backlog and Kanban board. When you work from a sprint page, you have access to the sprint backlog and task board.

1. VSTS provides extensive customization capabilities to the boards. You can add new or edit existing columns. You can define what work items should appear in the board. You can also use style rules and tag rules to highlight cards based on their property values or tags.

