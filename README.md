# SALT Publishing Guide

> How-to guide for publishing from CCHMC onto the Situational Awareness Learning Tool (SALT) Posit Connect sever

## Login to Posit Connect

1. Go to [dev.salt.cchmc.org](https://dev.salt.cchmc.org)
2. On the landing page, scroll down and click on the link to register with SALT  
    a. This will link to a brief REDCap survey where you can enter your basic information and agree to the SALT use terms  
    b. A SALT admin will create a user account with your CCHMC email that you can use for access
3. Once you have been confirmed to have access, back at the SALT landing page, in the top-right corner, click on the "login" button.  
    a. This should send you to a familiar-looking CCHMC login page; enter your credentials as normal  
4.  This should bring you to the SALT Posit Connect dashboard: ![content landing page](figs/content_landing_page.png)

## Git-backed Deployment

For SALT, content is deployed using the git version control system and GitHub, which allows for continuous integration and testing of data content. To publish to SALT using a git repository on GitHub:
    
1. In your project, create a "dev" branch to deploy from

2. Deploy the "dev" branch to Posit Connect as private

3. Once you're happy with the deployment, create a pull request of your "dev" branch and request a review from a SALT admin; merge into "main"

4. Deploy your "main" branch publicly; delete "dev" deployment

5. Iteratively merge in future "dev" branches to update your "main" deployment


### In your RStudio project

1. Use [`rsconnect::writeManifest()`](https://rstudio.github.io/rsconnect/) in R to add or update a [`manifest.json` file](https://rstudio.github.io/rsconnect/reference/writeManifest.html)

### On GitHub

1. If your project is not on GitHub, add it to the [CCHMC-SALT](https://github.com/orgs/CCHMC-SALT/repositories) organization. For more information on GitHub generally, read [here](https://docs.github.com/en/get-started/quickstart/hello-world) and for a great tutorial on using GitHub with R and RStudio, check out this [book](https://happygitwithr.com/)
    a. If you already have a project elsewhere on GitHub, email a SALT admin (andrew.vancil@cchmc.org or cole.brokamp@cchmc.org) to request that they fork your project into the CCHMC-SALT organization
2. Commit and push your manifest.json file that you created above to GitHub
3. In your original repository, create a branch called "dev"
4. In the forked repository (at CCHMC-SALT), open an issue to ask the SALT admin to sync the fork to your original repository
    a. If updating content, make the changes on your original repository and then open an issue to request the sync
    
### On the SALT Posit Connect Server
1. On the "Content" tab of Posit Connect, click the blue "Publish" button and select "Import from Git" from the dropdown menu
2. In the text box, paste the URL of your CCHMC-SALT Git repository (on GitHub, select "Code" -> copy for the correct URL)
3. Select your branch
    a. If this is your first time publishing this project, select your "dev" branch
    b. If you have gone trough the approval process, select your "main" branch; For more information on this, see the section below entitled "Production Deployment"
4. Select your root folder. This will be the folder where your `manifest.json` was written and stored
6. Title your content. For clarity, if this is a "dev" branch, please title your content as "[dev]_{your_title}"
6. Select "Deploy Content"

### Production Deployment
1. After you have successfully deployed your "dev" branch and are happy with how it presents online, return to your project's original GitHub repository and create a pull request for your "dev" branch
2. Open an Issue on the CCHMC-SALT version and request a review from a SALT admin, either Andrew Vancil (andrew-vancil) or Cole Brokamp (cole-brokamp)
    a. Once approved, the admin will merge your branch into main
3. Return to the SALT Posit Connect interface and follow the steps listed above, but this time select the "main" branch when prompted
4. Delete your "[dev]_{your_title}" deployment. Alternatively, you may choose to keep your [dev] branch active for further development, but it may incur operating costs

## Publishing Options
Once your content is deployed, you have further options to control access, the web address, report scheduling, and more. For more information, please follow the links to the documentation here for  [access](https://docs.posit.co/connect/user/content-settings/#content-access), [web address](https://docs.posit.co/connect/user/content-settings/#custom-url), and [scheduling](https://docs.posit.co/connect/user/scheduling/)
    

## Tags
For tracking purposes, a SALT admin will create a tag for your project/group. This will primarily be used for usage monitoring, but may be used to determine costs of hosting the object. Simply click the box relevant for your content

## Troubleshooting
Checking the [log](https://docs.posit.co/connect/user/content-settings/#content-logs) is often the best place to start troubleshooting. Here, you will find error messages that can help you figure out why your document may not be displaying how you would like it to. To find the log, click on the symbol at the top of your content control panel that looks like a little notebook. In here, you will be able to see both the posit connect log and a log that looks like your typical R console from each deployment instance. Explore these to find your error messages and begin troubleshooting. Further troubleshooting tips [here](https://docs.posit.co/connect/user/troubleshooting/).

For more information on git-backed deployment, please see the documentation [here](https://docs.posit.co/connect/user/git-backed/).

For additional help, please reach out to Cole Brokamp at [cole.brokamp\@cchmc.org](mailto:cole.brokamp@cchmc.org){.email} or Andrew Vancil at [andrew.vancil\@cchmc.org](mailto:andrew.vancil@cchmc.org){.email}




