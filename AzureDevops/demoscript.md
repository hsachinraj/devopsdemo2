# Demo Script for Demomate

VSTS is the ultimate DevOps solution into Azure.  With the new Azure DevOps Project we make it very simple to build your pipeline into Azure. The DevOps Project sets up everything you need for developing, deploying, and monitoring your application.

 In this demo, we're going to see how you can use Azure DevOps Project to automate the setup of an entire Continuous Integration (CI) and Continuous Delivery (CD) pipeline to Azure. 

To create an Azure DevOps Project, we go into the Azure portal and create a new resource and choose **DevOps Project**. The first thing you will be asked is what language do you want to use - .NET, Java, Node, PHP, or Python? We can even have static web apps.  Now, for this demo let's go ahead and choose Node. 

Next, it's going to ask you to select the application framework you  want to use. You can use Express, Sails, or a Simple Node.js app. You will select Simple Node for this demo.  Select Next To continue. Next, you will need to choose the type of infrastructure you want to deploy.  Do you want to use Web App for Containers or do you want to use Web App?  Now, for this demo let's go ahead and choose **Web App for containers**

Finally, you will have to specify what instance of Visual Studio Team Services do you want to use. If you do not have one, you can simply select to create a brand new one. Specify a name and choose a subscription. Click done when you have completed that and bam! that's literally all you need to do.  

Sit back, relax, and just let Azure build up your DevOps Projects. It's basically going to do a few things.  First, it's going to create the infrastructure up in Azure to host the sample Node.js app in App Service. Next, it will create a team project in Team Services, and then add sample code in a source control.  Next, it will create a CI/CD pipeline and kick off the build and the release pipeline, deploying the sample app into the infrastructure it just provisioned. 

The build will download the latest code from source control. It will compile everything. It will run unit test even.  And then it will package everything up for deployment.  And if the build was successful, it will trigger release management, where release management will then download those build artifacts and deploy the artifacts into Azure. And the beauty of it all is it just does all of this in the cloud for you. There's no machines for you to build. There's no installation or configurations to do.  Everything just works. And when it's all done you get a portal that looks like this, where from one screen you can see everything that was deployed. You're able to see that we have code that’s been deployed and we have deep links as well that will take you directly into Team Services into the repository. 

You will also see the infrastructure that has been deployed out into Azure.  So, in this case this is App Service up in Azure, as well as Application Insight has been setup and configured to monitor your application.

## Part 2: Exploring the project in-depth

 Let's take a look at the code and pipeline created in VSTS. Select the **Project HomePage** link to to open the VSTS project page. Select **Code** and you will see the repo where the sample app has been uploaded. Navigate to the build and you'll see the build def created. Click **Edit**to see what is inside the build definition. You will see the build pipeline containing tasks that makes sense for the technology that you picked. And same with release. Select **Releases** from the Build tab and you will see a CD pipeline created and configured to pick the deployment artifact from the build and deploy it to the target you chose. In this case, a node app deployed to Azure app service for container. When the build and release is successful, you should be able to see the application running - [back on the Azure portal, select the application endpoint]

Now this is great and fantastic for a sample application - But what if you wanted to customize this to deploy your code? That's actually very easy to do and let us see how you can do that.

Go back to the code repo again. As this is a Git repo, you will need to clone the this repo to your local machine. Select **Clone** and copy the link.  Open a command line, type *git clone* and paste the text you just copied to clone the repo. And once it's done cloning, you can open an explorer window to see the cloned code. 

Delete the code. We will get the actual code of our application

>**Note** The PartsUnlimited code from https://github.com/Microsoft/PartsUnlimitedE2E/ is used. You can download and extract the code from this link - https://github.com/Microsoft/PartsUnlimitedE2E/archive/dacpac.zip. 

Return back to the command line.  Go ahead and add everything, then commit and push your code back into VSTS. 

Now once the code hits VSTS, it's going to kick off a build as it is set to be a continuous integration - that is to run every time when the code is updated. 

Go to the VSTS poral and look at builds, you'll see that a new build has been kicked off. In most cases, the build should work without any changes but in some cases you might need to customize. Again this is very easy, select **Edit** and then you can customize by adding or removing tasks or change the properties.  Out of the box, VSTS comes with hundreds of tasks that you can just use. In addition to that, there are over 500 build and release tasks created by our partners that you can just download and start using. 

When the build is finished a release gets triggered - the release will pick up those bits and deploy the application all the way out into Azure.  Customizing the Release is very similar to customizing the build pipeline. In addition you could approvals - say for instance, you want to obtain an approval from one or more person before the deployment starts or after it is finished.

Wait for the release to finish and then go back to the app again. Select the endpoint, and you should see you code now deployed!

## 


## Summary
**Azure DevOps Project** makes it incredibly easy for you to get started with scaffolding an ,  just a couple of clicks to go from nothing at all into a full end-to-end DevOps Projects. Now we are the only cloud vendor that makes it so incredibly easy to go from nothing to this full DevOps pipeline where it's ready for you just to jump in and start editing code. Now currently we support .NET, of course, Java, Node, PHP, and Python. But we have a lot more languages that are coming as well as support for VMs. Now if you want to learn more, please go to the link. http://aka.ms/devops-projects  where our docs will walk you through everything you need to know. Thank you very much.  
