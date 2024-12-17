(deploy)= 
# How to Deploy Your Website

### Workshop Repo VS Workshop Website

EXPLAIN GHP PAGES INSTEAD

Let's recap.

You currently have all the files we need to build and develop your website (all included in the basic workshop template), locally on your own laptop. You want to make changes to these files, so that you can add content for your workshop! We make these changes locally. We also "build" (convert our files into HTML pages) locally. Yet we 

Now, you have made a repository that holds what GitHub needs to make our website (the basic workshop template). Essentially, the template has already been configured so that the html files that make up our website go into a folder called `docs`. We need to tell GitHub to look at the `docs` folder to find our website files and make it available to see online (a.k.a deploy it). This is what we mean when we say CBW uses GitHub pages to deploy our website.

```{admonition} Distinction
GitHub (ex. https://github.com/cbw-dev/jupyterbook-template) holds your repo, which has version control for all your files! <br> The deployed website (ex. https://cbw-dev.github.io/jupyterbook-template/) has the workshop online.
```

1. In the top navigation bar, select **Settings**.
![Base repo, pointing at settings](../img/git-instruct/github-settings.png)

2. Then, go to the **Pages** sidebar option.
![Selecting pages from the settings page](../img/git-instruct/github-select-pages.png)

3. "Deploy from a branch" is already selected, which is what we want. We must **change the branch from "none" to "main"**. Select the "None" dropdown button and select "main".
![Select main as the branc](../img/git-instruct/github-deploy-main.png)

4. Then, change the folder from `/ root` to `/docs`. Then **press save**.
![Select /docs as the branch](../img/git-instruct/github-deploy-docs.png)
    
    Great! Now we're waiting on the page to build and deploy, which should take less than a minute.
  
## Check Your Deploy and See your Website! {#check-deploy}
        
To see updates, go to the **Actions** page (found along the top navigation bar. This will help you understand how the deploy is working, and if it succeeded or failed.

![Image showing the different possibilities of deploy a github page](../img/git-instruct/github-pages-actions-explained.png)\

You can click <u>**pages build and deployment**</u> for updates.

![where to click for pages build and deployment information](../img/git-instruct/pages-build-and-deployment.png)

<br>
A **successful deploy** will have a green checkmark next to it. You can inspect the 3 steps: build, report-build-status, deploy. Once it's done deploying, **you can find the website at the link provided under the "deploy" step**!

![successful deploy](../img/git-instruct/successful-deploy.png)\

A **failed deploy** will have a red cross next to it. Clicking through the steps can help you determine what went wrong in the deploy.

> Warning: A website can build properly, but may not deploy properly! It is a good idea to check after making big changes.

![failed deploy](../img/git-instruct/failed-deploy.png)\

#### A Very Specific Build and Deployment Warning {-}

![two consecutive deploy warnings](../img/git-instruct/exclamation-point-deploy-warning.png)\

This is a very specific (and unlikely) warning. It occurs when 1 deploy hasn't finished, but another deploy began. THIS IS NOT A CONCERN. This is a warning message you do not have to worry about!