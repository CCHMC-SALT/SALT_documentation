# SALT Publishing Guide

> How-to guide for publishing from CCHMC onto the Situational Awareness Learning Tool (SALT) Posit Connect sever

## Login to Posit Connect

1.  Go to [dev.salt.cchmc.org](https://dev.salt.cchmc.org)
2.  In the top-right corner, click on the "login" button.
    a.  This should send you to a familiar-looking CCHMC login page; enter your credentials as normal
3.  This should bring you to a page that looks something like this: ![content landing page](figs/content_landing_page.png)

## Git-backed Deployment

At SALT, we are utilizing git-backed deployment for publishing. This best-practice technique ensures that your reports and dashboards are always updated and proper version control is enacted. We encourage publishers to use the following workflow:
    i. In your project, create a "dev" branch to deploy from
    ii. Deploy the "dev" branch to Posit Connect as private
    iii. Once you're happy with the deployment, merge your "dev" branch to "main"
    iv. Deploy your "main" branch publicly
    v. Iteratively merge in future "dev" branches to update your "main" deployment

### In your project
1. In your project repository on GitHub, create a branch off of "main" called "dev"
2. Install the R package called ["{rsconnect}"](https://rstudio.github.io/rsconnect/)
    a. While in top-level folder your project, run the command `rsconnect::writeManifest()`. This will compile a file called "manifest.json" that Posit Connect will read to host your project on the server. See more information [here](https://rstudio.github.io/rsconnect/reference/writeManifest.html)
### On the SALT Posit Connect Server
1. On the "Content" tab of Posit Connect, click the blue "Publish" button and select "Import from Git" from the dropdown menu
2. In the text box, paste the URL of your Git repository (on GitHub, select "Code" -> copy for the correct URL)
3. Select your branch
    a. If this is your first time publishing this project, select your "dev" branch
    b. If you have already privately deployed your dev branch, approved it and merged it in, select your "main" branch
4. Title your content. For clarity, if this is a "dev" branch, please title your content as "dev_[your_title]"
5. Select "Deploy Content"



    
